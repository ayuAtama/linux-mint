# Guide: Installing and Applying a Custom Cursor Theme in Linux Mint

## Overview

This guide outlines the process of copying a custom cursor theme directory into the local icons directory (`~/.icons`) and applying it via system settings in Linux Mint (Cinnamon desktop environment).

---

## Prerequisites

* A custom cursor theme folder (typically extracted from a `.zip` or `.tar.gz` archive)
* Basic familiarity with terminal usage
* Linux Mint with Cinnamon desktop

---

## Step 1: Prepare the Cursor Theme

Ensure your cursor theme is extracted and structured correctly. A valid cursor theme directory typically contains:

* A `cursors/` subdirectory
* An `index.theme` file

Example:

```
MyCursorTheme/
├── cursors/
└── index.theme
```

---

## Step 2: Copy Theme to Local Icons Directory

1. Open a terminal.

2. Navigate to the directory containing your cursor theme.

   **Clear path examples:**

   ```bash
   cd ~/Downloads/MyCursorTheme
   ```

   or if the theme is inside another folder:

   ```bash
   cd ~/Downloads/cursor-pack/MyCursorTheme
   ```

3. Copy the theme folder into the local icons directory:

   ```bash
   cp -r ~/Downloads/MyCursorTheme ~/.icons/
   ```

> **Note:**
> If `~/.icons` does not exist, create it first:
>
> ```bash
> mkdir -p ~/.icons
> ```

---

## Step 3: Apply the Cursor Theme

1. Open **System Settings**.
2. Navigate to **Themes**.
3. Go to the **Mouse Pointer** tab.
4. Select your newly installed cursor theme from the list.

---

## Step 4: Verify Application

* Move your mouse pointer to confirm the new cursor is active.
* If the theme does not appear:

  * Log out and log back in, or
  * Restart Cinnamon:

    ```bash
    cinnamon --replace &
    ```

---

## Troubleshooting

### Theme Not Showing

* Verify the folder structure is correct.
* Ensure the directory is placed in `~/.icons` or `/usr/share/icons`.

### Permissions Issues

* Ensure correct permissions:

  ```bash
  chmod -R 755 ~/.icons/MyCursorTheme
  ```

### System-wide Installation (Optional)

To install for all users:

```bash
sudo cp -r ~/Downloads/MyCursorTheme /usr/share/icons/
```

---

## Summary

The workflow consists of:

1. Extracting the cursor theme
2. Copying it to `~/.icons`
3. Selecting it via system settings

This method ensures a clean, user-level installation without requiring administrative privileges.
