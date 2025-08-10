# EVE UI Manager

A simple PowerShell utility for EVE Online players that lets you back up and restore your UI settings (`.dat` files) between your local system and a USB drive.

## 📦 What This Script Does

- **Backs up your current UI files** (`core_user_*.dat` and `core_char_*.dat`) into a `BackupUI` folder
- **Restores the latest backup** from your local system or USB
- **Saves the last backup to a USB drive** (if one is connected)
- **Loads a backup from USB** and saves it locally as well
- **Deletes all UI settings** (with confirmation)
- Automatically retains **only the 20 most recent backups**, or backups **no older than 14 days**

---

## 💾 Installation

1. **Download** this repository or clone it.
2. **Move the entire script folder** (containing `EVE_UI_Manager.ps1`) to your EVE UI settings directory, for example:

C:\Users\<YourName>\AppData\Local\CCP\EVE\<default_profile>\settings_Default\


*(This is where your `core_user_*.dat` and `core_char_*.dat` files are stored.)*

3. **Run the script** by double-clicking the shortcut (recommended: run as **Administrator**).

---

##▶️ How to Use

When you run the script, a small Win98-style window will appear with the following buttons:

| Button                          | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| **Save Current UI to All**       | Saves current `core_user_*` and `core_char_*` files to `BackupUI`.         |
| **Restore from Last BackupUI**   | Restores the latest local backup.                                          |
| **Save Last BackupUI to USB**    | Copies the last local backup to a USB drive.                               |
| **Load BackupUI from USB**       | Restores backup from USB and saves a copy locally.                         |
| **Clear All UI Settings**        | Deletes all UI `.dat` files (asks for confirmation).                       |

---

## 📝 Notes

- The script automatically detects the **last plugged-in USB drive** (removable type).
- Creates `EVE_UI_Backup` on USB if it doesn't already exist.
- New backups are saved in folders named like `YYYY-MM-DD_HH-MM-SS`.
- **Only run the script inside your EVE settings folder**, or it won’t find the required `.dat` files.

---

## 🔐 Privacy & Safety

This script does **not connect to the internet**, **does not collect data**, and only works with local and USB files.

---

## 💡 Pro Tip

If you play on multiple PCs, you can easily move your UI layout between them using the USB features of this tool.

---

## 🛠️ Requirements

- Windows 10 or 11
- PowerShell (built-in)
- Access to the EVE `.dat` files location
- Script execution enabled (if needed, open PowerShell as admin and run):


