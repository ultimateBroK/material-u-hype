# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    # Global animation settings
    animation {
        enabled = true;
        speed = 8; # Tốc độ animation (giá trị càng cao, animation càng nhanh)
        bezier = "default"; # Đường cong bezier mặc định cho animation
    }

    # Windows animations
    animation:windows {
        style = slide; # Sử dụng animation kiểu slide cho windows
    }

    animation:windowsIn {
        style = slide;
        direction = left; # Slide từ trái vào khi mở cửa sổ mới
        duration = 200ms; # Thời gian animation
    }

    animation:windowsOut {
        style = slide;
        direction = right; # Slide ra bên phải khi đóng cửa sổ
        duration = 200ms; # Thời gian animation
    }

    animation:windowsMove {
        style = popin; # Animation nhẹ nhàng khi di chuyển hoặc thay đổi kích thước cửa sổ
        duration = 150ms; # Thời gian animation ngắn hơn để tránh cảm giác chậm
    }

    # Layers animations
    animation:layers {
        style = fade; # Sử dụng animation kiểu fade cho layers
    }

    animation:layersIn {
        style = fade;
        duration = 200ms; # Fade in khi layer mở
    }

    animation:layersOut {
        style = fade;
        duration = 200ms; # Fade out khi layer đóng
    }

    # Fade animations
    animation:fade {
        style = fade; # Sử dụng animation kiểu fade
    }

    animation:fadeIn {
        duration = 200ms; # Fade in khi mở cửa sổ
    }

    animation:fadeOut {
        duration = 200ms; # Fade out khi đóng cửa sổ
    }

    animation:fadeSwitch {
        duration = 150ms; # Fade khi chuyển đổi giữa các cửa sổ hoạt động
    }

    animation:fadeShadow {
        duration = 150ms; # Fade shadow khi chuyển đổi giữa các cửa sổ hoạt động
    }

    animation:fadeDim {
        duration = 200ms; # Dimming animation cho cửa sổ không hoạt động
    }

    animation:fadeLayers {
        style = fade; # Fade animation cho layers
    }

    animation:fadeLayersIn {
        duration = 200ms; # Fade in khi layer mở
    }

    animation:fadeLayersOut {
        duration = 200ms; # Fade out khi layer đóng
    }

    # Border animations
    animation:border {
        duration = 100ms; # Animation nhẹ nhàng cho border color switch
    }

    animation:borderangle {
        style = loop; # Gradient angle animation lặp lại liên tục
        duration = 5000ms; # Thời gian dài để tạo hiệu ứng gradient mượt mà
    }

    # Workspaces animations
    animation:workspaces {
        style = slidefade; # Kết hợp slide và fade cho workspace transitions
    }

    animation:workspacesIn {
        style = slidefade;
        direction = left; # Slide từ trái vào khi chuyển workspace
        duration = 300ms; # Thời gian animation dài hơn để tạo cảm giác mượt mà
    }

    animation:workspacesOut {
        style = slidefade;
        direction = right; # Slide ra bên phải khi chuyển workspace
        duration = 300ms;
    }

    animation:specialWorkspace {
        style = slidefade; # Animation đặc biệt cho workspace cụ thể
    }

    animation:specialWorkspaceIn {
        style = slidefade;
        direction = left;
        duration = 300ms;
    }

    animation:specialWorkspaceOut {
        style = slidefade;
        direction = right;
        duration = 300ms;
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

