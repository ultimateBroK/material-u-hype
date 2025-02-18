# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # == Định nghĩa các đường cong Bezier ==
        bezier = easeInOut, 0.37, 0, 0.63, 1  # Mượt mà, cân bằng
        bezier = overshot, 0.13, 0.99, 0.29, 1.1 # Vượt quá một chút, tạo cảm giác nảy
        bezier = quickOut, 0, 0.75, 0.4, 1 # Nhanh dần ở cuối

        # == Cấu hình cho cửa sổ (windows) ==
        animation = windowsIn, 1, 5, easeInOut, slide
        animation = windowsOut, 1, 5, easeInOut, slide
        animation = windowsMove, 1, 5, easeInOut, slide

        # == Cấu hình cho lớp (layers) ==
        animation = layersIn, 1, 6, easeInOut, slide
        animation = layersOut, 1, 5, quickOut, fade
        animation = layersMove, 1, 5, easeInOut, slide

        # == Cấu hình cho độ mờ (fade) ==
        animation = fadeIn, 1, 7, easeInOut, fade
        animation = fadeOut, 1, 7, easeInOut, fade
        animation = fadeSwitch, 1, 4, quickOut # Nhanh chóng khi chuyển cửa sổ
        animation = fadeShadow, 1, 4, quickOut
        animation = fadeDim, 1, 4, easeInOut
        animation = fadeLayersIn, 1, 5, easeInOut
        animation = fadeLayersOut, 1, 5, quickOut

        # == Cấu hình cho viền (border) ==
        animation = border, 1, 10, default  # Thay đổi màu viền mượt mà
        animation = borderangle, 1, 30, default, loop # Nếu dùng gradient border

        # == Cấu hình cho workspace ==
        animation = workspaces, 1, 5, easeInOut, slidefade 70% # Mượt và có hiệu ứng mờ
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

