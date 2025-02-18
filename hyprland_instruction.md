# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # ===== Định nghĩa Bezier Curves =====
        # GNOME thường dùng easeInOutCubic hoặc tương tự.
        bezier = easeInOutCubic, 0.645, 0.045, 0.355, 1.0  # Chuẩn easeInOutCubic
        bezier = easeOutQuart, 0.25, 1, 0.5, 1 # Đã dùng
        bezier = modernBounce, 0.18, 0.99, 0, 1.15 # Đã dùng


        # ===== Windows Animations =====
        # Tốc độ tương tự GNOME
        animation = windowsIn, 1, 0.3, easeInOutCubic, slide    # 300ms
        animation = windowsOut, 1, 0.25, easeInOutCubic, slide   # 250ms
        animation = windowsMove, 1, 0.25, easeInOutCubic, slide  # 250ms

        # ===== Layers Animations =====
        animation = layersIn, 1, 0.3, easeInOutCubic, slide  # 300ms
        animation = layersOut, 1, 0.2, easeInOutCubic, fade   # 200ms

        # ===== Fade Animations =====
        animation = fadeIn, 1, 0.2, easeInOutCubic        # 200ms
        animation = fadeOut, 1, 0.15, easeInOutCubic       # 150ms
        animation = fadeSwitch, 1, 0.1, easeInOutCubic    # 100ms
        animation = fadeShadow, 1, 0.15, easeInOutCubic   # 150ms
        animation = fadeDim, 1, 0.2, easeInOutCubic       # 200ms

        # ===== Border Animations =====
        animation = border, 1, 1.0, default  # 1 giây
        animation = borderangle, 1, 3.0, default, loop # 3 giây

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 0.35, easeInOutCubic, slidefade 70%  # 350ms
        animation = specialWorkspace, 1, 0.35, easeInOutCubic, slidefade 70% # 350ms
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

