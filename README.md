# 🎮 Ultimate Guide: PC Game Streaming to your WebOS TV with Sunshine and Moonlight

Welcome to the future of gaming! This guide will walk you through the process of setting up **Sunshine** (the streaming host on your PC) and **Moonlight** (the client on your WebOS TV) to stream your favorite PC games directly to your television. Get ready for a seamless, high-quality, big-screen gaming experience!

---

## Part 1: WebOS TV Setup (Installing Moonlight)

The WebOS TV requires a special process to install third-party applications like Moonlight. This involves enabling Developer Mode and using a desktop application to manage the installation.

### Step 1: Create an LG Developer Account

Before you begin, you need an account to enable developer features on your TV.

1.  Navigate to the LG WebOS TV Developer website: [https://webostv.developer.lge.com/](https://webostv.developer.lge.com/)
2.  Create a new account or log in to your existing one.

### Step 2: Enable Developer Mode on your TV

This step unlocks the ability to install custom applications.

1.  On your WebOS TV, go to the **LG Content Store** (App Store).
2.  Search for and install the **"Developer Mode"** application.
3.  Open the **Developer Mode** app from your TV's home screen.
4.  Log in using the LG Developer account you created in Step 1.
5.  Once logged in, switch the **`Dev Mode Status`** and **`Key Server`** toggles to **ON**.
6.  **Crucial**: Note down the **PASSPHRASE** displayed in the Developer Mode app. You will need this later for authentication.

> **⚠️ Session Refresh Note:** Developer Mode sessions are temporary. You will need to refresh your session time periodically, as the TV will erase all developer-installed content when the session expires.

### Step 3: Install the WebOS Dev Manager on your Computer

You need a desktop application to connect to your TV and install the Moonlight app.

1.  Visit the webOS Brew website: [https://www.webosbrew.org/](https://www.webosbrew.org/)
2.  Scroll down and click the link to **`Manage your TV with your computer and smartphone`**. This will redirect you to the `dev-manager-desktop` GitHub repository.
3.  On the GitHub page, go to the **Releases** section (usually on the right-hand panel) and download the latest version of the `webOS Dev Manager` for your operating system (Windows, macOS, or Linux).
4.  Install the downloaded file.

### Step 4: Configure the WebOS Dev Manager

1.  Open the installed application, which is named **`webOS Dev Manager`**.
2.  In the Connection Mode, select **`Use Developer Mode`**.
3.  A setup modal will appear. Proceed to the **Setup Device** section.
4.  **Device Name**: Choose a friendly name for your TV (e.g., "Living Room TV").
5.  **Address**: Enter your TV's **IP Address**.
6.  **Authentication**: Enter the **PASSPHRASE** you saved from Step 2. This field is **case-sensitive**.

> **💡 Pro Tip:** The `webOS Dev Manager` can also be used to refresh your Developer Mode session on the TV via the **Info** tab, saving you a trip to the TV's app!

### Step 5: Install Moonlight

1.  In the `webOS Dev Manager`, navigate to the **Apps** section and select the **Available** tab.
2.  Find the **Moonlight** application in the list.
3.  Click on **Details** and then **Install** it onto your TV.

> **❗ Important:** Your WebOS TV must remain **ON** and connected to the network for the `webOS Dev Manager` to successfully connect and install the app.

---

## Part 2: Gaming PC Setup (Installing Sunshine)

Sunshine is the open-source host software that runs on your gaming PC, capturing your screen and sending the video stream to your TV.

### Step 1: Download and Install Sunshine

1.  Visit the official Sunshine GitHub repository: [https://github.com/LizardByte/Sunshine](https://github.com/LizardByte/Sunshine)
2.  Download and install the appropriate version for your Operating System (Windows, Linux, etc.).

### Step 2: Initial Configuration and Login

1.  Open the Sunshine application.
2.  You will be prompted to complete a basic configuration, which includes setting up a username and password for the web interface.
3.  After this initial setup, your browser will be redirected to a `localhost` URL (e.g., `https://localhost:47990`) where you will log in with the credentials you just created. This is the Sunshine web interface.

> **🛠️ Dependency Check:** If Sunshine prompts you to install any missing dependencies (such as **ViGEmBus** for virtual controller support), follow the instructions to install them and then restart the Sunshine server.

### Step 3: Configure Your Games

Sunshine automatically detects some applications, like Steam Big Picture, but you can add custom shortcuts for non-Steam games (e.g., Epic Games, GOG, etc.).

1.  In the Sunshine web interface, navigate to the **Applications** section.
2.  To add a custom game or application, you will need to create a **URI** (Uniform Resource Identifier) shortcut. This allows Moonlight to launch the game directly.
3.  For detailed documentation and examples on creating URIs for various platforms and games, consult the official Sunshine documentation: [https://docs.lizardbyte.dev/projects/sunshine/latest/md_docs_2app__examples.html](https://docs.lizardbyte.dev/projects/sunshine/latest/md_docs_2app__examples.html)

> **Example URI (Windows Steam Game):**
>
> ```
> steam://rungameid/464920
> ```

---

## Part 3: Connecting and Streaming

With both the host (Sunshine on PC) and client (Moonlight on TV) installed, you are ready to connect and play!

### Step 1: Pair Your Devices

1.  Go back to your WebOS TV and open the **Moonlight** application.
2.  If your TV and PC are on the same local network, your gaming PC should appear instantly in the list.
3.  If it does not appear, you can manually add it by clicking the **Add** button and entering your PC's local IP address.
4.  Moonlight will display a PIN on your TV screen. Enter this PIN into the prompt that appears on your PC (in the Sunshine web interface or a desktop notification) to complete the pairing process.

### Step 2: Optimize Stream Settings

For the best experience, you can fine-tune the streaming quality in the Sunshine web interface.

1.  In the Sunshine web interface, go to the **Settings** section.
2.  **Resolution and Frame Rate**: A common high-quality setting is **`1440p60`** (1440p resolution at 60 frames per second), but you can adjust this based on your TV's capabilities and network bandwidth.
3.  **Video Bitrate**: Experiment with the video bitrate to find the sweet spot between image quality and network latency. Higher bitrates mean better quality but require a more stable network connection. Mine is default to 40000 kpbs (will try increase this later)

Once connected, simply select a game from the Moonlight interface on your TV, and Sunshine will launch it on your PC and begin streaming!

---

*Guide created by Bx (v20251217.1).*
