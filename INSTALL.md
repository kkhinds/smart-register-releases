# Installing Smart Register on Windows

A step-by-step guide for first-time users. Read once, install once — after
that, the app updates itself.

If you get stuck, jump to **[Troubleshooting](#troubleshooting)** at the
bottom.

---

## What you're installing

**Smart Register** is a Windows desktop application for the SJPI Class
Register. It runs entirely on your laptop. Your data stays on your
computer; nothing is sent anywhere unless you choose to share a backup.

The installer is **not digitally signed** yet. This means Windows will show
a blue or yellow warning the first time you run it. That's normal — the
section below walks you through it.

You only need to do this **once**. After installation, opening Smart Register
from the Start Menu works like any other app.

---

## Step 1 — Download the installer

1. Open this page in your web browser:
   **https://github.com/kkhinds/smart-register-releases/releases/latest**

2. Scroll down to the **Assets** section.

3. Click the file named:

   `Smart-Register-Setup-1.x.x.exe`

   (The `1.x.x` part is the version number, for example `1.17.9`. Always
   pick the file ending in `.exe`.)

4. Your browser will download the file. Save it somewhere you can find —
   the **Downloads** folder is fine.

**Do not** download files named `.blockmap` or `latest.yml`. Those are
support files the app uses automatically once installed.

---

## Step 2 — Run the installer

1. Open your **Downloads** folder.

2. **Double-click** `Smart-Register-Setup-1.x.x.exe`.

### What you'll see — the blue "Windows protected your PC" screen

Because the installer isn't signed yet, Windows shows a blue dialog with:

> **Windows protected your PC**
>
> Microsoft Defender SmartScreen prevented an unrecognized app from
> starting. Running this app might put your PC at risk.
>
> [ Don't run ]

**This is expected.** The file is safe — it just hasn't been registered
with Microsoft.

Look for the small text that says **"More info"** near the top of the
dialog. Click it.

The dialog will expand and reveal an extra button at the bottom:

> [ Run anyway ]    [ Don't run ]

Click **Run anyway**.

> **If you don't see "More info":** The text is small and easy to miss —
> it's directly above or below the "Windows protected your PC" heading.
> If the dialog only has "OK" or "Don't run", close it and re-download
> the installer (the file may be incomplete).

### Windows account control (UAC) prompt

Windows may show a second dialog asking:

> **Do you want to allow this app to make changes to your device?**

Click **Yes**.

---

## Step 3 — Walk through the installer

A small wizard window opens.

1. **Choose installation folder** (if asked) — the default is fine.
   Click **Next**.

2. **Choose Start Menu folder** (if asked) — the default is fine.
   Click **Next**.

3. **Choose components** (if asked) — leave everything ticked.
   Click **Install**.

4. Wait a few seconds while files copy.

5. The wizard says **"Smart Register has been installed on your
   computer"**. Tick **"Run Smart Register"** if it isn't already, then
   click **Finish**.

You're done. Smart Register is now in your Start Menu.

---

## Step 4 — Open the app for the first time

- Press the **Windows key** on your keyboard.
- Type `Smart Register`.
- Click the app in the search results.

The first time it opens, it will create its data folder automatically.
Optionally pin it to your Taskbar so it's one click away every day:

- Right-click the Smart Register tile in the Start Menu.
- Choose **Pin to taskbar**.

---

## Updates — you don't have to do anything

Smart Register checks for updates in the background every time you open
it. When a new version is available, it downloads silently and installs
the next time you close the app.

You'll see a **What's new** popup the first time you open the new
version, listing what changed.

You will **not** see the "Windows protected your PC" screen again for
updates.

---

## Where your data is stored

By default, Smart Register stores everything in:

```
C:\Users\<your-username>\AppData\Roaming\sjpi-class-register\data\
```

If you want your data on OneDrive or Google Drive so it syncs across
machines:

1. Open Smart Register.
2. Go to **Settings** (sidebar, bottom-left).
3. Find **Storage location** → **Choose folder…**
4. Pick a folder inside your OneDrive / Google Drive directory.
5. Smart Register copies your data there and uses it from then on.

---

## Troubleshooting

### "Windows protected your PC" has no "More info" link

Re-download the installer. The download may have been interrupted and
Windows is treating the file as definitely-bad rather than
unrecognised.

### My antivirus quarantined the file

This happens with some aggressive antivirus products because the
installer is unsigned. Two options:

1. **Add Smart Register to your antivirus exclusion list** (recommended).
   Each antivirus does this differently — search your antivirus name +
   "exclusion" online. Add the path:
   `C:\Users\<your-username>\AppData\Local\Programs\Smart Register\`

2. **Restore the file from quarantine** and re-run the installer.

### The installer crashes or hangs

1. Right-click the installer → **Run as administrator**.
2. If still no luck, restart your PC and try again.
3. If still no luck, please send a screenshot of any error message to
   the SJPI IT contact along with your Windows version (Windows key →
   type `winver` → screenshot).

### How do I uninstall?

1. Press the Windows key → type `Add or remove programs` → open it.
2. Search the list for **Smart Register**.
3. Click it → **Uninstall**.

Your data folder is **not** deleted by the uninstaller. To remove it
manually:

```
C:\Users\<your-username>\AppData\Roaming\sjpi-class-register\
```

### I'm on a school laptop with restricted permissions

Some school-managed laptops block any unsigned `.exe` from running, even
with "Run anyway". In that case you'll need your IT department to either:

- Whitelist the installer, or
- Install it for you using an administrator account.

Show them this page to explain what they're looking at.

---

## Quick reference card (printable)

| Step | What to do |
|------|------------|
| 1 | Go to https://github.com/kkhinds/smart-register-releases/releases/latest |
| 2 | Download `Smart-Register-Setup-1.x.x.exe` |
| 3 | Double-click the downloaded file |
| 4 | Blue "Windows protected your PC" → click **More info** → **Run anyway** |
| 5 | UAC prompt → **Yes** |
| 6 | Installer wizard → keep clicking **Next**, then **Install**, then **Finish** |
| 7 | Press Windows key → type `Smart Register` → open it |
| 8 | Pin to Taskbar for daily use |

That's it. From this point on, Smart Register opens like any other
program and updates itself in the background.
