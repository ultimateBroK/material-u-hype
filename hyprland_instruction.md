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
        # Tăng thời gian để chuyển động chậm hơn
        animation = windowsIn, 1, 1.0, easeOutQuart, slide      # 1000ms (1 giây)
        animation = windowsOut, 1, 1.0, easeOutQuart, slide     # 1000ms (1 giây)
        animation = windowsMove, 1, 0.8, easeInOutSine, slide   # 800ms

        # ===== Layers Animations =====
        animation = layersIn, 1, 0.8, easeOutQuart, slide   # 800ms
        animation = layersOut, 1, 0.8, easeOutQuart, fade    # 800ms

        # ===== Fade Animations =====
        animation = fadeIn, 1, 0.6, easeInOutSine       # 600ms
        animation = fadeOut, 1, 0.5, easeInOutSine      # 500ms
        animation = fadeSwitch, 1, 0.3, easeInOutSine   # 300ms
        animation = fadeShadow, 1, 0.3, easeInOutSine  # 300ms (Nếu có đổ bóng)
        animation = fadeDim, 1, 0.4, easeInOutSine     # 400ms (Điều chỉnh nếu có dim_inactive)

        # ===== Border Animations =====
        animation = border, 1, 1.5, default # 1.5 giây (Tốc độ thay đổi màu border)
        animation = borderangle, 1, 4.0, default, loop # 4 giây (Nếu dùng gradient border)

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 0.8, easeOutQuart, slidefade 70% # 800ms
        animation = specialWorkspace, 1, 0.8, easeOutQuart, slidefade 70% # 800ms
    }
    
**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

