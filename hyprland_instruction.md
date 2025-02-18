# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # Cấu hình chính
        animation = windowsIn, 1, 4, easeOutExpo, slide
        animation = windowsOut, 1, 4, easeInExpo, slide
        animation = windowsMove, 1, 3, default, popin 10%
        
        animation = layersIn, 1, 2.5, default, fade
        animation = layersOut, 1, 2.5, default, fade
        
        animation = fadeIn, 1, 2, default
        animation = fadeOut, 1, 2, default
        animation = fadeSwitch, 1, 1.5, default
        animation = fadeShadow, 1, 1.5, default
        animation = fadeDim, 1, 2, easeOutExpo
        animation = fadeLayersIn, 1, 2, linear
        animation = fadeLayersOut, 1, 2, linear
        
        animation = border, 1, 3, easeOutQuad
        animation = borderangle, 1, 30, once
        
        animation = workspaces, 1, 4, easeInOutExpo, slidefadevert 10%
        animation = specialWorkspace, 1, 3.5, easeInOutExpo, slidefadevert 10%
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

