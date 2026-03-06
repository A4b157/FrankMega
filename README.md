# 🚀 FrankMega - Easy File Downloads for Home Servers

[![Download FrankMega](https://img.shields.io/badge/Download-FrankMega-brightgreen)](https://github.com/A4b157/FrankMega)

Welcome to FrankMega, a simple tool that helps you download files on your home server using Docker. This guide walks you through downloading and running FrankMega on a Windows PC. No prior skills in programming or Docker are needed.

---

## 📋 What is FrankMega?

FrankMega is a service that runs on your home server. It helps you download files quickly and manage them easily. The program works inside something called Docker, which is a system that keeps apps safe and separate. If you have a home server or want to set up one, FrankMega can make downloading files easier for you.

---

## 🖥️ System Requirements

Before starting, check if your Windows PC meets these needs:

- Windows 10 or newer
- At least 4 GB of RAM
- At least 2 GB free storage for FrankMega and Docker
- A stable internet connection
- Docker Desktop installed on your PC (explained below)

---

## 🔧 Installing Docker

FrankMega runs inside Docker, so you need to first install Docker Desktop on your Windows machine.

1. Open your browser and visit [https://docs.docker.com/desktop/windows/install/](https://docs.docker.com/desktop/windows/install/)
2. Click on the "Download Docker Desktop for Windows" button.
3. When the file downloads, open it and follow the on-screen instructions.
4. After installation, restart your PC if asked.
5. Confirm Docker is running by looking for the whale icon in your system tray (bottom right corner).

Docker helps FrankMega run in an isolated environment, so it will not affect other parts of your PC.

---

## 🚀 Download and Setup FrankMega

To get FrankMega, visit the main project page and find the latest release.

[![Get FrankMega](https://img.shields.io/badge/Get-FrankMega-blue)](https://github.com/A4b157/FrankMega)

Follow these steps:

1. Click the badge above or open this link in your browser:  
   https://github.com/A4b157/FrankMega  
2. On the page, look for a section called “Releases” or “Download” on the right side or bottom of the page.  
3. Download the latest release files. If there is a file ending in `.zip` or `.tar`, download and extract it to a folder you can easily find, like your Desktop or Documents.  
4. Inside the extracted folder, look for a file named `docker-compose.yml`. This file tells Docker how to run FrankMega.

---

## 🛠️ Running FrankMega on Windows

Now that you have Docker and FrankMega files, you can start the service:

1. Open the Start menu and search for `PowerShell`. Right-click on it and choose "Run as administrator".  
2. In PowerShell, change to the folder where you saved the FrankMega files:  
   ```  
   cd C:\Users\YourName\Desktop\FrankMega  
   ```  
   Replace `YourName` and the path as needed.  
3. Start FrankMega in Docker by typing:  
   ```  
   docker-compose up -d  
   ```  
4. Docker will download FrankMega’s components and start the service. This may take a few minutes the first time.  
5. When it finishes, you will see a message saying containers are running.

---

## 🌐 Access FrankMega

After running, you can open FrankMega in your web browser:

- Open your favorite browser (like Chrome or Edge).
- Type `http://localhost:3000` in the address bar.
- Press Enter.
- You should see the FrankMega homepage where you can start downloading and managing files.

`localhost` means you are connecting to the FrankMega service running on your PC.

---

## 💡 Using FrankMega

Here are some tips to get started:

- Use the interface to add file download links.
- Manage which files you want to keep or remove.
- Check on active downloads anytime.
- Organize files in folders inside the service.
- Set limits on download speed if needed (check FrankMega settings).

All major features are accessible from the web interface.

---

## 🔄 Updating FrankMega

From time to time, updates improve FrankMega:

1. Stop FrankMega by running this in PowerShell in your FrankMega folder:  
   ```  
   docker-compose down  
   ```  
2. Download the latest release files again from the GitHub page.  
3. Replace or merge the old files with the new ones in your working folder.  
4. Start FrankMega again:  
   ```  
   docker-compose up -d  
   ```  

---

## 🚫 Stopping and Removing FrankMega

To stop the service:

- Open PowerShell as administrator.
- Navigate to your FrankMega folder.
- Run:  
  ```  
  docker-compose down  
  ```  
  
This stops FrankMega but keeps your downloaded files.

To remove downloaded files, delete them manually from your configured folders.

---

## ❓ Need Help?

If you face issues, try these steps:

- Make sure Docker runs properly with its whale icon visible.
- Check your internet connection.
- Confirm you are in the correct folder when running PowerShell commands.
- Restart Docker and try starting FrankMega again.
- Look for error messages in the PowerShell window.
- Visit the GitHub page for updates or more instructions:
  
  https://github.com/A4b157/FrankMega

---

## ⚙️ Advanced Settings (Optional)

If you want to change the default settings such as ports or download folders:

- Open the `docker-compose.yml` file with a plain text editor like Notepad.
- Look for sections named `ports` or `volumes`.
- Change values to fit your needs (for example, change the port from `3000` to another number if 3000 conflicts).
- Save the file.
- Restart FrankMega using the commands above.

Adjust settings carefully to avoid breaking the service.

---

## 📁 Where Downloads Are Stored

By default, FrankMega stores files inside a folder linked to Docker. This folder is defined in the `docker-compose.yml` file. It might look like this:

```
volumes:
  - ./downloads:/app/downloads
```

This means all downloaded files are saved in a folder named `downloads` inside the FrankMega folder on your PC.

You can access your files directly here or use the service to manage them.

---

## 🛠️ Troubleshooting Common Problems

- **Docker not starting:** Ensure your system supports virtualization in BIOS and that it is enabled.
- **FrankMega not appearing at localhost:** Check if Docker containers are running with `docker ps` command.
- **Port 3000 already in use:** Change the port in `docker-compose.yml` or stop the app using the port.
- **Files not saving:** Make sure the downloads folder has write permissions.
- **PowerShell permission errors:** Always run PowerShell as administrator.

---

[![Download FrankMega](https://img.shields.io/badge/Download-FrankMega-brightgreen)](https://github.com/A4b157/FrankMega)