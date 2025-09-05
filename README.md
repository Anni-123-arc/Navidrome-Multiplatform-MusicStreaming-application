# 🎶 Navidrome Multiplatform Music Streaming Application 🚀

Welcome to the **Navidrome Music Streaming Platform**!\
This project lets you self-host your music 🎵, stream it from anywhere
🌍, and control it via **reverse proxy (NGINX)** and **secure tunneling
(ngrok)**.

------------------------------------------------------------------------

## 📂 Project Structure

Here's what the repository looks like:

    navidrome/
    │── data/                 # Stores application data (do not commit 🚫)
    │── docker-compose.yml    # Docker Compose setup to run Navidrome, Nginx & Ngrok
    │── music/                # Your music library 🎧
    │── nginx/                # Nginx reverse proxy configuration
    │── .env                  # Environment variables (contains ngrok token)

------------------------------------------------------------------------

## ⚡ Features

✅ Host your own music server with **Navidrome**\
✅ Use **Nginx** as a reverse proxy 🛡️\
✅ Expose it securely with **ngrok tunnel** 🌐\
✅ Keep secrets safe inside a **.env file** 🔑

------------------------------------------------------------------------

## 🛠️ Setup Guide

Follow these steps to clone and run the project:

### 1️⃣ Clone the repository

``` bash
git clone https://github.com/Anni-123-arc/Navidrome-Multiplatform-MusicStreaming-application.git
cd Navidrome-Multiplatform-MusicStreaming-application
```

### 2️⃣ Create `.env` file

Inside your project root, create a file named `.env` and add your
**ngrok token**:

    NGROK_AUTHTOKEN=your_ngrok_token_here

👉 Never commit `.env` to GitHub (already in `.gitignore`)!

### 3️⃣ Start the services 🚀

``` bash
docker compose up -d
```

This will start: - Navidrome (music server) 🎶\
- Nginx (reverse proxy) 🔄\
- Ngrok (secure tunnel) 🌍

### 4️⃣ Access your music 🎧

-   **Local access:** <http://localhost:4533>\

-   **Ngrok public URL:** Check logs with

    ``` bash
    docker logs ngrok
    ```

    You'll see a forwarded URL like `https://xyz.ngrok-free.app` 🎉

------------------------------------------------------------------------

## 🔄 How Reverse Proxy + Ngrok Work

-   **Nginx (Reverse Proxy)** 🛡️ → Forwards requests from the outside
    world to Navidrome running inside Docker.\
-   **Ngrok (Tunnel)** 🌐 → Creates a secure public URL that connects
    directly to your local Nginx → Navidrome server.

So the flow looks like this:

🌍 Internet → Ngrok URL → Nginx (Reverse Proxy) → Navidrome 🎶

------------------------------------------------------------------------

## 🎉 That's it!

Now you have your own **self-hosted Spotify alternative** running with
**Docker, Nginx, and ngrok**.\
Enjoy your music anywhere! 🎧✨

------------------------------------------------------------------------

💡 **Pro tip:** Want to add this project to your resume? Highlight:\
- Docker & Docker Compose\
- Reverse Proxy with Nginx\
- Secure tunneling with ngrok\
- Environment variable management (.env)

🔥 Rock on with Navidrome! 🤘
