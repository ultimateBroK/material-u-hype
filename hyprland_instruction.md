# Hyprland setup (step by step) with Archlinux

## Install Archlinux

	loadkeys en
	
	ping google.com (check internet connection)

	archinstall
> Easy step :) do it by yourself, once done, reboot

## Install Hyprland and some basic applications
 	
> Install yay
	
	yay -S hyprland

> Install basic applications

	sudo pacman -S kitty firefox fastfetch wine nano nemo viewnior wofi waybar dunst thunar hyprpaper grim slurp cliphist polkit-gnome ibus-bamboo ttf-fira-code ttf-jetbrains-mono

- Terminal: kitty
- Browser: firefox
- System-info: fastfetch 
- Running Windows programs: wine  
- Editor: nano 
- File manager: thunar (or nemo) 
- Image viewer: viewnior
- Launcher: wofi
- Status bar/Widget bar: waybar
- Notification daemon: dunst
- Wallpaper setter: hyprpaper
- Screenshot tool: grim (screenshot), slurp (select area and screenshot)
- Clipboard manager: cliphist
- Input method: ibus-bamboo
- Font: ttf-fira-code, ttf-jetbrains-mono
- Polkit agent: polkit-gnome

> For NVIDIA, AMD GPU
	
	# NVIDIA
	sudo pacman -S nvidia-dkms nvidia-utils egl-wayland nvidia-settings

	# AMD
	sudo pacman -S xf86-video-amdgpu
	
> 

## Hyprland Configuration

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # ===== Định nghĩa Bezier Curves (tùy chỉnh) =====
        bezier = easeOutQuart, 0.25, 1, 0.5, 1  # Mượt mà, chậm dần về cuối
        bezier = easeInOutSine, 0.37, 0, 0.63, 1 # Chuyển tiếp mềm mại
        bezier = modernBounce, 0.18, 0.99, 0, 1.15   # Hiệu ứng "nảy" nhẹ nhàng
        #bezier = linear, 0, 0, 1, 1


        # ===== Windows Animations =====
        animation = windowsIn, 1, 4, easeOutQuart, slide
        animation = windowsOut, 1, 3, easeOutQuart, slide
        animation = windowsMove, 1, 4, easeInOutSine, slide

        # ===== Layers Animations =====
        animation = layersIn, 1, 4, easeOutQuart, slide
        animation = layersOut, 1, 3, easeOutQuart, fade

        # ===== Fade Animations =====
        animation = fadeIn, 1, 4, easeInOutSine
        animation = fadeOut, 1, 3, easeInOutSine
        animation = fadeSwitch, 1, 3, easeInOutSine
        animation = fadeShadow, 1, 3, easeInOutSine
        animation = fadeDim, 1, 3, easeInOutSine

        # Fade cho Layer, tránh config chồng chéo, và gây ra lỗi.
        animation = fadeLayersIn, 1, 4, easeOutQuart
        animation = fadeLayersOut, 1, 3, easeOutQuart

        # ===== Border Animations =====
        animation = border, 1, 5, default
        animation = borderangle, 1, 15, default, loop

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 4, easeOutQuart, slidefade 70%
        animation = specialWorkspace, 1, 4, easeOutQuart, slidefade 70%
    }

