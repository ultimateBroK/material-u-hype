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
        # Các đường cong phổ biến, dễ sử dụng
        bezier = easeOutQuart, 0.25, 1, 0.5, 1   # Mượt mà, chậm dần về cuối
        bezier = easeInOutSine, 0.37, 0, 0.63, 1 # Chuyển tiếp mềm mại, cân bằng
        bezier = modernBounce, 0.18, 0.99, 0, 1.15 # (Tùy chọn) Hiệu ứng nảy, có thể bỏ qua

        # ===== Windows Animations =====
        # Cân bằng tốt giữa tốc độ và độ mượt
        animation = windowsIn, 1, 0.5, easeOutQuart, slide      # 500ms
        animation = windowsOut, 1, 0.4, easeOutQuart, slide     # 400ms
        animation = windowsMove, 1, 0.4, easeInOutSine, slide   # 400ms

        # ===== Layers Animations =====
        animation = layersIn, 1, 0.45, easeOutQuart, slide  # 450ms
        animation = layersOut, 1, 0.35, easeOutQuart, fade   # 350ms

        # ===== Fade Animations =====
        # Nhanh, nhưng không gây khó chịu
        animation = fadeIn, 1, 0.3, easeInOutSine       # 300ms
        animation = fadeOut, 1, 0.2, easeInOutSine      # 200ms
        animation = fadeSwitch, 1, 0.15, easeInOutSine   # 150ms
        animation = fadeShadow, 1, 0.2, easeInOutSine  # 200ms
        animation = fadeDim, 1, 0.3, easeInOutSine     # 300ms

        # ===== Border Animations =====
        animation = border, 1, 1.0, default  # 1 giây
        animation = borderangle, 1, 3.0, default, loop # 3 giây

        # ===== Workspaces Animations =====
        # Chuyển workspace mượt mà
        animation = workspaces, 1, 0.5, easeOutQuart, slidefade 70% # 500ms
        animation = specialWorkspace, 1, 0.5, easeOutQuart, slidefade 70% # 500ms
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

