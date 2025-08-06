##  PM2 Commands

PM2 is a process manager for Node.js applications. Below are common commands used to manage your server with PM2.

---

### ✅ To Start the Server

```bash
pm2 start entryFile --name "serverName"
```

Example:

```
pm2 start server.js --name "my-app"
```

⛔ To Stop the App

Example:
```
pm2 stop my-app
```

🔄 Restart the App

Example:
```
pm2 restart my-app
```

❌ Delete the App from PM2

Example:
```
pm2 delete my-app
```
---

## How to Enable Auto-Start in PM2

1. Generate a startup script
   ```
   pm2 startup
   ```
This will print a command (based on your OS), something like:
sudo env PATH=$PATH:/home/username/.nvm/versions/node/v18.17.1/bin pm2 startup systemd -u username --hp /home/username

2. Copy and run the command it shows
3. Save the currently running apps
   ```
   pm2 save
   ```
   This ensures PM2 remembers which apps to auto-start on boot.
