# Hành trình Hyprland trên CachyOS

1. Cài CachyOS cùng WM Hyprland
2. Mở Hyprland docs -> Master Tutorial

**Monitor**

	monitor=eDP-1,1920x1200@60,0x1080,1
	monitor=HDMI-A-1,1920x1080@75,0x0,1

**Animation** 

    animations {
        enabled = yes

        # Bezier curve mượt mà, hiện đại (ease-in-out)
        bezier = easeinout, 0.4, 0.0, 0.6, 1.0

        # Global durations (có thể tùy chỉnh nếu muốn)
        animation_duration_windows = 5
        animation_duration_layers = 5
        animation_duration_workspaces = 7
        animation_duration_fade = 5
        animation_duration_border = 5

        # Windows Animations
        animation = windows, 1, $animation_duration_windows, easeinout, fade # Fallback animation cho windows
        animation = windowsIn, 1, $animation_duration_windows, easeinout, slide, left
        animation = windowsOut, 1, $animation_duration_windows, easeinout, slide, right
        animation = windowsMove, 1, $animation_duration_windows, easeinout, fade

        # Layers Animations
        animation = layers, 1, $animation_duration_layers, easeinout, fade # Fallback animation cho layers
        animation = layersIn, 1, $animation_duration_layers, easeinout, fade
        animation = layersOut, 1, $animation_duration_layers, easeinout, fade

        # Fade Animations
        animation = fade, 1, $animation_duration_fade, easeinout # Fallback animation cho fade
        animation = fadeIn, 1, $animation_duration_fade, easeinout, fade
        animation = fadeOut, 1, $animation_duration_fade, easeinout, fade
        animation = fadeSwitch, 1, $animation_duration_fade, easeinout
        animation = fadeShadow, 1, $animation_duration_fade, easeinout
        animation = fadeDim, 1, $animation_duration_fade, easeinout
        animation = fadeLayers, 1, $animation_duration_fade, easeinout # Fallback cho fadeLayers
        animation = fadeLayersIn, 1, $animation_duration_fade, easeinout, fade
        animation = fadeLayersOut, 1, $animation_duration_fade, easeinout, fade

        # Border Animation
        animation = border, 1, $animation_duration_border, default

        # Border Angle Animation
        animation = borderangle, 1, once

        # Workspaces Animations
        animation = workspaces, 1, $animation_duration_workspaces, easeinout, slidefade # Fallback cho workspaces
        animation = workspacesIn, 1, $animation_duration_workspaces, easeinout, slidefade
        animation = workspacesOut, 1, $animation_duration_workspaces, easeinout, slidefade
        animation = specialWorkspace, 1, $animation_duration_workspaces, easeinout, slidefade # Fallback cho specialWorkspace
        animation = specialWorkspaceIn, 1, $animation_duration_workspaces, easeinout, slidefade
        animation = specialWorkspaceOut, 1, $animation_duration_workspaces, easeinout, slidefade
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

