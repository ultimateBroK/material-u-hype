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
        # TỐI ƯU HÓA: Chỉ định nghĩa các bezier curves MỘT LẦN và tái sử dụng.
        bezier = easeOutQuart, 0.25, 1, 0.5, 1  # Mượt mà, chậm dần về cuối
        bezier = easeInOutSine, 0.37, 0, 0.63, 1 # Chuyển tiếp mềm mại
        bezier = modernBounce, 0.18, 0.99, 0, 1.15   # Hiệu ứng "nảy" nhẹ nhàng
        # bezier = linear, 0, 0, 1, 1  # Không cần thiết, vì mặc định là linear.


        # ===== Windows Animations =====
        # TỐI ƯU HÓA: Sử dụng biến bezier đã định nghĩa, và đặt thời gian hợp lý
        animation = windowsIn, 1, 0.7, easeOutQuart, slide      # 700ms
        animation = windowsOut, 1, 0.7, easeOutQuart, slide     # 700ms
        animation = windowsMove, 1, 0.5, easeInOutSine, slide   # 500ms

        # ===== Layers Animations =====
        # TỐI ƯU HÓA:  fade cho layer KHÔNG NÊN dùng chung với fade thông thường.
        animation = layersIn, 1, 0.6, easeOutQuart, slide
        animation = layersOut, 1, 0.6, easeOutQuart, fade

        # ===== Fade Animations =====
        # TỐI ƯU HÓA: Đơn giản hóa và sử dụng thời gian hợp lý.
        animation = fadeIn, 1, 0.4, easeInOutSine       # 400ms
        animation = fadeOut, 1, 0.3, easeInOutSine      # 300ms
        animation = fadeSwitch, 1, 0.15, easeInOutSine   # 150ms
        animation = fadeShadow, 1, 0.15, easeInOutSine  # 150ms (Nếu có đổ bóng)
        animation = fadeDim, 1, 0.25, easeInOutSine     # 250ms (Điều chỉnh nếu có dim_inactive)

        # Fade cho Layer, tránh config chồng chéo, và gây ra lỗi. Đã tối ưu ở trên
        #animation = fadeLayersIn, 1, 6, easeOutQuart,
        #animation = fadeLayersOut, 1, 4, easeOutQuart,

        # ===== Border Animations =====
        animation = border, 1, 1.0, default # 1 giây (Tốc độ thay đổi màu border)
        animation = borderangle, 1, 3.0, default, loop # 3 giây (Nếu dùng gradient border)

        # ===== Workspaces Animations =====
        animation = workspaces, 1, 0.6, easeOutQuart, slidefade 70% # Chuyển đổi workspace mượt
        animation = specialWorkspace, 1, 0.6, easeOutQuart, slidefade 70% #Nếu có sử dụng special workspace
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

