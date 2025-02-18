# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # ===== Định nghĩa Bezier Curves (tùy chỉnh) =====
        bezier = easeOutQuart, 0.25, 1, 0.5, 1
        bezier = easeInOutSine, 0.37, 0, 0.63, 1
        bezier = modernBounce, 0.18, 0.99, 0, 1.15

        # ===== Windows Animations =====
        # Cân bằng giữa mượt mà và phản hồi
        animation = windowsIn, 1, 0.85, easeOutQuart, slide      # 850ms
        animation = windowsOut, 1, 0.85, easeOutQuart, slide     # 850ms
        animation = windowsMove, 1, 0.65, easeInOutSine, slide   # 650ms

        # ===== Layers Animations =====
        animation = layersIn, 1, 0.7, easeOutQuart, slide   # 700ms
        animation = layersOut, 1, 0.7, easeOutQuart, fade    # 700ms

        # ===== Fade Animations =====
        animation = fadeIn, 1, 0.5, easeInOutSine       # 500ms
        animation = fadeOut, 1, 0.4, easeInOutSine      # 400ms
        animation = fadeSwitch, 1, 0.25, easeInOutSine   # 250ms
        animation = fadeShadow, 1, 0.25, easeInOutSine  # 250ms
        animation = fadeDim, 1, 0.35, easeInOutSine     # 350ms

        # ===== Border Animations =====
        animation = border, 1, 1.2, default  # 1.2 giây
        animation = borderangle, 1, 3.5, default, loop # 3.5 giây

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 0.7, easeOutQuart, slidefade 70% # 700ms
        animation = specialWorkspace, 1, 0.7, easeOutQuart, slidefade 70% # 700ms
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

