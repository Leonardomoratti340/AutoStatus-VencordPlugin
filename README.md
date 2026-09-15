# AutoStatus for Vencord 🕒

A custom Vencord plugin that automatically changes your Discord status (Online, Idle, Do Not Disturb, Invisible) based on custom schedules. Perfect for freelancers, students, or anyone who wants to automate their "working hours" presence.

## ✨ Features
* **Custom Timeframes:** Set exact start and end times (e.g., 09:30 to 18:00).
* **Custom Statuses:** Choose which status to apply during the timeframe, and which one to revert to outside of it.
* **Native API Integration:** Uses Discord's native REST API for fast and reliable status updates without UI desync issues.
* **Fully Configurable:** Easily adjust all settings directly through Vencord's built-in settings UI.

## 📦 Installation

To use this plugin, you need to have [Vencord](https://vencord.dev/) installed.

### Option 1: Via Vencord User Plugins (Recommended)
Vencord allows you to load external plugins directly if you build it from source.
1. Clone the Vencord repository: `git clone https://github.com/Vendicated/Vencord.git`
2. Navigate to the `src/plugins` folder.
3. Clone this repository inside it: `git clone https://github.com/Leonardomoratti340/AutoStatus-VencordPlugin`
4. Rebuild Vencord: `pnpm build`
5. Reload Discord (`Ctrl + R`).

### Option 2: Manual Injection
If you are developing or modifying the plugin:
1. Copy the `index.ts` file from this repository.
2. Paste it into a new folder named `autoStatus` inside Vencord's `src/plugins/` directory.
3. Run `pnpm build` in the Vencord root folder.

## ⚙️ Configuration
Once installed and enabled, go to **User Settings > Plugins** in Discord and search for `AutoStatus`.
Click the **gear icon** ⚙️ next to the plugin switch to configure:
* **Start Time / End Time:** Use the `HH:MM` format (24-hour clock).
* **Active Status:** The status applied *during* your specified timeframe.
* **Default Status:** The status applied *outside* your specified timeframe.

## 🛠️ Development & Contributing
Contributions, issues, and feature requests are welcome! 
If you want to modify the polling rate (currently set to check every 60 seconds), you can adjust the `setInterval` in `index.ts`.

---
*Developed with ❤️ by [Leonardo Moratti aka Foxy_340](https://github.com/Leonardomoratti340) - Freelance IT Consultant & Full-Stack Developer.*