# Hyprland setup (step by step) with CachyOS

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

**Touchpad and Gesture**

    touchpad {
        natural_scroll = yes  # Cuộn tự nhiên (như trên macOS/điện thoại)
        disable_while_typing = yes # Vô hiệu hoá touchpad khi gõ phím
        clickfinger_behavior = yes # Click bằng 1, 2, 3 ngón (left, right, middle)
        tap-to-click = yes        # Chạm để click
        drag_lock = yes #Giữ thao tác kéo thả (drag)
        scroll_factor = 1.0 # Điều chỉnh tốc độ cuộn (1.0 là mặc định)
    }

    gesture {
        workspace_swipe = yes   # Bật vuốt để chuyển đổi workspace
        workspace_swipe_fingers = 3 # Sử dụng 3 ngón để vuốt
        workspace_swipe_distance = 300 # Khoảng cách vuốt tối thiểu (pixels)
        workspace_swipe_invert = no # Vuốt sang trái để chuyển sang workspace bên phải
        workspace_swipe_min_speed_to_force = 30 #Tốc độ vuốt tối thiểu
        #workspace_swipe_cancel_ratio = 0.5 # Tỉ lệ hoàn tác (nếu vuốt không đủ)
        #workspace_swipe_create_new = yes # Vuốt để tạo workspace mới (nếu ở cuối danh sách)

        workspace_swipe_direction_lock = yes # Khoá hướng vuốt
        workspace_swipe_direction_lock_threshold = 10 #Ngưỡng khoá hướng
    }