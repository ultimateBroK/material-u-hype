# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # ===== Bezier Curves =====
        # Tạo các đường cong Bezier tùy chỉnh để tái sử dụng, tạo sự nhất quán.
        bezier = easeInOut, 0.42, 0.0, 0.58, 1.0  # Dùng cho hầu hết các animation, tạo sự mượt mà
        bezier = easeOut, 0.0, 0.0, 0.58, 1.0    # Dùng cho các animation "ra" (out), nhanh dần về cuối
        bezier = easeIn, 0.42, 0.0, 1.0, 1.0    # Dùng cho animation "vào" (in), chậm dần về cuối
        bezier = myOvershoot, 0.05, 0.9, 0.1, 1.4    # Dùng cho các animation workspace, tạo điểm nhấn


        # ===== Global Windows Animations =====
        animation = windowsIn, 1, 7, easeIn, slide
        animation = windowsOut, 1, 7, easeOut, slide
        animation = windowsMove, 1, 7, easeInOut, none  # Không dùng 'slide' cho di chuyển để tránh giật

        # ===== Layers Animations =====
        # Layer: Các lớp layer shell (ví dụ: thanh trạng thái, thông báo, ...)
        animation = layersIn, 1, 6, easeInOut, fade
        animation = layersOut, 1, 5, easeOut, fade

        # ===== Fade Animations =====
        # Độ mờ (opacity)
        animation = fadeIn, 1, 7, easeInOut
        animation = fadeOut, 1, 7, easeInOut
        animation = fadeSwitch, 1, 4, easeInOut
        animation = fadeShadow, 1, 4, easeInOut
        animation = fadeDim, 1, 4, easeInOut
            # Fade layer
        animation = fadeLayersIn, 1, 7, easeIn,
        animation = fadeLayersOut, 1, 7, easeOut,

        # ===== Border Animations =====
        animation = border, 1, 10, default  # Điều chỉnh tốc độ đổi màu viền
        animation = borderangle, 1, 30, default, loop # Đổi góc gradient, chậm và lặp lại

        # ===== Workspaces Animations =====
        # Chuyển workspace
        animation = workspacesIn, 1, 8, myOvershoot, slide
        animation = workspacesOut, 1, 8, myOvershoot, slidefade 20%

        # ===== Special Workspace Animations =====
        animation = specialWorkspaceIn, 1, 8, myOvershoot, slide
        animation = specialWorkspaceOut, 1, 8, myOvershoot, slidefade 20%
    }

