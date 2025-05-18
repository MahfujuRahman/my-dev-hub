# Full Tutorial: Use Supervisor to Run a Notification Script Every 10 Seconds on Ubuntu

## 🌟 What You’ll Build

* A Bash script that sends a desktop notification every 10 seconds.
* Supervisor configuration to run and manage the script as a background service, auto-restarting if it crashes.

---

## ✅ Step 1: Create the Notification Script

```bash
nano notifier.sh
```

Paste this code:

```bash
#!/bin/bash

# Optional debug output
echo "Notifier started at $(date)"

while true
do
  echo "Sending notification at $(date)"
  notify-send "🔔 Laravel Queue" "Queue worker is running..."
  sleep 10
done
```

Save and exit (`CTRL + O`, `Enter`, `CTRL + X`).

Make it executable:

```bash
chmod +x notifier.sh
```

---

## ✅ Step 2: Test the Script Manually

```bash
./notifier.sh
```

You should see a desktop notification every 10 seconds.

Stop the script: `CTRL + C`

If `notify-send` is missing:

```bash
sudo apt install libnotify-bin
```

---

## ✅ Step 3: Install Supervisor

```bash
sudo apt update
sudo apt install supervisor
```

Enable and start the Supervisor service:

```bash
sudo systemctl enable supervisor
sudo systemctl start supervisor
```

---

## ✅ Step 4: Create Supervisor Configuration

Create a config file:

```bash
sudo nano /etc/supervisor/conf.d/notifier.conf
```

Paste the following:

```ini
[program:notifier]
command=/full/path/to/notifier.sh
directory=/full/path/to
autostart=true
autorestart=true
stderr_logfile=/var/log/notifier.err.log
stdout_logfile=/var/log/notifier.out.log
```

> Replace `/full/path/to` with your actual path. Example:
> `/home/mahfujur/notification/notifier.sh`

---

## ✅ Step 5: Reload and Start the Supervisor Program

```bash
sudo supervisorctl reread
sudo supervisorctl update
sudo supervisorctl start notifier
```

Check status:

```bash
sudo supervisorctl status notifier
```

---

## ⚠️ Troubleshooting & Common Fixes

### 1. `notify-send` doesn’t work (no notifications)

* Run from terminal manually: `./notifier.sh`
* If it works but not under Supervisor, add `DISPLAY=:0` to the config:
echo $DBUS_SESSION_BUS_ADDRESS

```ini
environment=DISPLAY=":0",DBUS_SESSION_BUS_ADDRESS="unix:path=/run/user/1000/bus"
```

### 2. Logs not created or blank

* Check permissions of `/var/log/`
* Make sure your script actually writes stdout/stderr

### 3. Wrong path in Supervisor config

* Absolute paths are required in `command` and `directory`
* Run `realpath notifier.sh` to get full path

### 4. Supervisor not running

* Check service status:

```bash
sudo systemctl status supervisor
```

Restart it if needed:

```bash
sudo systemctl restart supervisor
```

---

## 🚀 Auto-Start on Reboot

Supervisor handles this automatically if `autostart=true`. Just ensure:

```bash
sudo systemctl enable supervisor
```

---

## 📄 Useful Commands Summary

| Task            | Command                               |
| --------------- | ------------------------------------- |
| Reload config   | `sudo supervisorctl reread`           |
| Apply config    | `sudo supervisorctl update`           |
| Start program   | `sudo supervisorctl start notifier`   |
| Stop program    | `sudo supervisorctl stop notifier`    |
| Restart program | `sudo supervisorctl restart notifier` |
| View status     | `sudo supervisorctl status`           |
| View logs       | `tail -f /var/log/notifier.out.log`   |

---

## 🎉 You Did It!

You now have a persistent notification script that runs in the background and restarts itself using Supervisor!

For further automation, integrate logging or conditions for notifications.

---

**Author:** Mahfujur Rahman
**Created:** May 18, 2025
