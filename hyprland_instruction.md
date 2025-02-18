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
        bezier = easeOutQuart, 0.25, 1, 0.5, 1  # Mượt mà, chậm dần về cuối
        bezier = easeInOutSine, 0.37, 0, 0.63, 1 # Chuyển tiếp mềm mại
        bezier = modernBounce, 0.18, 0.99, 0, 1.15   # Hiệu ứng "nảy" nhẹ nhàng
        #bezier = linear, 0, 0, 1, 1


        # ===== Windows Animations =====
        animation = windowsIn, 1, 7, easeOutQuart, slide
        animation = windowsOut, 1, 7, easeOutQuart, slide
        animation = windowsMove, 1, 5, easeInOutSine, slide

        # ===== Layers Animations =====
        animation = layersIn, 1, 6, easeOutQuart, slide
        animation = layersOut, 1, 6, easeOutQuart, fade

        # ===== Fade Animations =====
        animation = fadeIn, 1, 8, easeInOutSine
        animation = fadeOut, 1, 6, easeInOutSine
        animation = fadeSwitch, 1, 3, easeInOutSine
        animation = fadeShadow, 1, 3, easeInOutSine #Nếu có đổ bóng
        animation = fadeDim, 1, 5, easeInOutSine  # Điều chỉnh nếu có dim_inactive

        # Fade cho Layer, tránh config chồng chéo, và gây ra lỗi.
        animation = fadeLayersIn, 1, 6, easeOutQuart,
        animation = fadeLayersOut, 1, 4, easeOutQuart,

        # ===== Border Animations =====
        animation = border, 1, 10, default # Tốc độ thay đổi màu border
        animation = borderangle, 1, 30, default, loop # Nếu dùng gradient border

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 6, easeOutQuart, slidefade 70% # Chuyển đổi workspace mượt
        animation = specialWorkspace, 1, 6, easeOutQuart, slidefade 70% #Nếu có sử dụng special workspace
    }