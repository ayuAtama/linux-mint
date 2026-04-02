### 1. Download the Catppuccin GTK Theme
The theme comes with different "accent" colors (like Mauve, Blue, Pink, or Green) so you can customize it exactly to your liking.

1. Go to the official Catppuccin GTK Releases page: [https://github.com/catppuccin/gtk/releases](https://github.com/catppuccin/gtk/releases)
2. Scroll down to the **Assets** section of the latest release.
3. Look for a `.zip` file that includes **Macchiato** and your preferred accent color. For example: `catppuccin-mocha-blue-standard+default.zip`.
4. Download the `.zip` file.

### 2. Install the Theme
You will need to place the extracted theme files into a hidden `.themes` folder in your Home directory.

1. Open your terminal.
2. Create the hidden themes directory (if it doesn't already exist) by running this command:
   `mkdir -p ~/.themes`
3. Open your File Manager, go to your **Downloads** folder, and extract the `.zip` file you downloaded.
4. Move the newly extracted folder (e.g., `catppuccin-mocha-blue-standard+default.zip`) into the `~/.themes` folder. 
   *(Note: To see hidden folders like `.themes` in your File Manager, press **Ctrl + H**).*

### 3. Apply the Theme in Linux Mint
Now that the theme is installed, you just need to tell Linux Mint to use it.

1. Press the Super (Windows) key, type **Themes**, and open the Themes application.
2. You will see several categories. Change the following to your new Catppuccin Macchiato theme:
   * **Window borders**
   * **Controls**
   * **Desktop** (If you are using Cinnamon, this changes the panel and menu colors).

### 4. Optional: Match Your Icons and Terminal
To get the complete aesthetic, you'll likely want your icons and terminal to match the Macchiato palette.

* **Icons:** The best match is usually the **Papirus** icon theme paired with the Catppuccin folder colors. You can find the installation script for Catppuccin Papirus folders on their GitHub here: [Catppuccin Papirus Folders](https://github.com/catppuccin/papirus-folders).
* **Terminal:** Linux Mint's default terminal can also be themed. Catppuccin has a dedicated port for GNOME Terminal (the default in Mint Cinnamon). You can find the one-line installation script here: [Catppuccin GNOME Terminal](https://github.com/catppuccin/gnome-terminal).