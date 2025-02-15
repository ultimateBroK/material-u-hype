Okay, here's a step-by-step guide to customizing your dotfiles, focusing on key areas and providing specific examples based on the codebase:

**1. Understanding the Structure**

*   **`.config/`**: This is where most of your customizations will live.  It contains configuration files for various applications.
*   **`install.sh` and update-dots.sh**: These scripts manage the installation and updating of your dotfiles.  Be careful when modifying these, as incorrect changes can break your system.
*   **scriptdata**: Contains scripts and data used by the installation process.  dependencies.conf lists the packages your system relies on.  functions contains helper functions used by other scripts.
*   **`README.md`**: Provides an overview of the project and links to other resources.

**2. Backing Up Your Existing Configuration**

Before making any changes, back up your existing configuration. The install.sh script has a backup function:

```sh
./install.sh
```

When prompted, choose to create a backup. This will save your current configuration in `$BACKUP_DIR` (defined in environment-variables). The `backup_configs` function in functions performs the backup.

**3. Customizing Hyprland**

*   **Keybinds:**
    *   Edit `~/.config/hypr/custom/keybinds.conf` to add or modify keybinds.  The main hyprland.conf sources this file.
    *   The get_keybinds.py script in hyprland is used to extract keybinds for the cheatsheet. If you change the keybind syntax, you might need to update this script.
    *   The cheatsheet itself is configured in main.js and keybinds.js.
*   **General Settings:**
    *   Edit `~/.config/hypr/custom/general.conf` to change settings like border width, rounding, and shadows.
*   **Rules:**
    *   Edit `~/.config/hypr/custom/rules.conf` to define rules for specific applications (e.g., floating, fullscreen).
*   **Executables:**
    *   Edit `~/.config/hypr/custom/execs.conf` to launch programs on startup.
*   **Environment Variables:**
    *   Edit `~/.config/hypr/custom/env.conf` to set environment variables.
*   **Colors:**
    *   Edit `~/.config/hypr/hyprland/colors.conf` to change the color scheme.

**4. Customizing AGS (Aylur's GTK Widget System)**

*   **Configuration Files:** Most AGS configuration is in ags.
*   **`user_options.js`:**  This file is intended for overriding default options.  Create or modify user_options.js to customize settings.  See user_options.js for available options.
*   **Widgets:**  AGS uses JavaScript for widgets.  Modify the files in modules to change the appearance and behavior of the bar, sidebars, and other elements.
*   **Styles:**  AGS uses SCSS for styling.  The `handleStyles` function in config.js compiles the SCSS files.  Modify the SCSS files in scss to change the look of your widgets.
*   **Color Scheme:** The color scheme is managed by the colorgen.sh script in color_generation. This script generates colors based on your wallpaper. The applycolor.sh script then applies these colors to various parts of the system, including Hyprland, GTK, and Qt.
*   **Custom Modules:** You can create your own custom modules. The music.js file in normal is an example of a custom module that displays music information.

**5. Customizing Other Applications**

*   Edit the configuration files in .config for applications like Fish, Zsh, Foot, Fuzzel, etc.

**6. Applying Changes**

*   **Hyprland:**  Run `hyprctl reload` to apply changes to your Hyprland configuration.
*   **AGS:**  Run `ags -r` to reload the AGS configuration.
*   **Other Applications:**  Restart the application to apply the changes.

**7. Updating Your Dotfiles**

*   Use the update-dots.sh script to update your dotfiles. This script will:
    1.  Fetch the latest changes from the Git repository.
    2.  Identify files that you have modified.
    3.  Prompt you to choose whether to keep your changes or replace them with the latest versions.
    4.  Apply the changes.

**Example Customizations**

*   **Change the bar height:**
    1.  Edit user_options.js
    2.  Add or modify the `bar.height` option:

    ```javascript
    const userConfigOptions = {
        'bar': {
            'height': 30,
        }
    }

    export default userConfigOptions;
    ```

    3.  Run `ags -r` to reload the AGS configuration.
*   **Add a new keybind:**
    1.  Edit `~/.config/hypr/custom/keybinds.conf`
    2.  Add a new keybind:

    ```conf
    bind = SUPER, Q, exec, kitty
    ```

    3.  Run `hyprctl reload` to apply the changes.
*   **Change the font:**
    1.  Edit qt5ct.conf
    2.  Modify the `general` and `fixed` font settings under the `[Fonts]` section.
    3.  Edit user_options.js
    4.  Modify the `font` setting under the `appearance` section.
    5.  Restart any applications that use these fonts.

**Important Considerations**

*   **`excludes` in update-dots.sh:**  The `excludes` variable in update-dots.sh lists files and directories that should not be updated.  Make sure that your customized files are in this list to prevent them from being overwritten.
*   **`user_options.js`:** Use user_options.js to override default settings. This makes it easier to update your dotfiles without losing your customizations.
*   **Testing:**  Test your changes thoroughly before committing them to your Git repository.
*   **Conflicts:**  Be aware of potential conflicts when updating your dotfiles.  The update-dots.sh script will help you resolve these conflicts, but it's important to understand how the script works.
*   **`.gitignore`:**  Make sure that you are not accidentally committing sensitive information (e.g., API keys, passwords) to your Git repository.  Use the .gitignore file to exclude these files.

By following these steps, you can effectively customize your dotfiles and create a personalized desktop environment. Remember to back up your configuration regularly and test your changes thoroughly.
