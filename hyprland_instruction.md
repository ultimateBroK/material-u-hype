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
        # Chậm hơn để thấy rõ hiệu ứng, nhưng vẫn mượt
        animation = windowsIn, 1, 1.2, easeOutQuart, slide     # 1200ms (1.2 giây)
        animation = windowsOut, 1, 1.2, easeOutQuart, slide    # 1200ms (1.2 giây)
        animation = windowsMove, 1, 0.9, easeInOutSine, slide  # 900ms

        # ===== Layers Animations =====
        animation = layersIn, 1, 1.0, easeOutQuart, slide  # 1000ms (1 giây)
        animation = layersOut, 1, 1.0, easeOutQuart, fade   # 1000ms (1 giây)

        # ===== Fade Animations =====
        animation = fadeIn, 1, 0.7, easeInOutSine      # 700ms
        animation = fadeOut, 1, 0.6, easeInOutSine     # 600ms
        animation = fadeSwitch, 1, 0.4, easeInOutSine  # 400ms
        animation = fadeShadow, 1, 0.4, easeInOutSine # 400ms
        animation = fadeDim, 1, 0.5, easeInOutSine    # 500ms

        # ===== Border Animations =====
        animation = border, 1, 1.5, default # 1.5 giây
        animation = borderangle, 1, 4.0, default, loop # 4 giây

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 0.9, easeOutQuart, slidefade 70% # 900ms
        animation = specialWorkspace, 1, 0.9, easeOutQuart, slidefade 70% # 900ms
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

