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
    speed = 8; # Adjusts overall animation speed (lower is faster)
    }

    # Windows animations
    window {
    animation-style = slide;
    animation-in = left;   # Slide in from the left when opening a window
    animation-out = right; # Slide out to the right when closing a window
    animation-move = popin; # Smooth effect for moving/resizing windows
    }

    # Layers animations
    layer {
    animation-style = fade;
    animation-in = fadeLayersIn;  # Fade in layers smoothly
    animation-out = fadeLayersOut; # Fade out layers smoothly
    }

    # Fade animations
    fade {
    animation-fadein = 300ms;       # Window open fade duration
    animation-fadeout = 300ms;      # Window close fade duration
    animation-fadeswitch = 200ms;   # Active window switch fade duration
    animation-fadeshadow = 200ms;   # Shadow fade duration
    animation-fadedim = 250ms;      # Dimming inactive windows easing
    animation-fadelayers = 300ms;   # Layer fade duration
    }

    # Border animations
    border {
    animation-speed = 200ms;        # Speed of border color transitions
    }

    # Border angle animations
    borderangle {
    animation-style = loop;         # Looping gradient angle animation
    animation-speed = 5000ms;       # Slow and subtle looping effect
    }

    # Workspaces animations
    workspace {
    animation-style = slidefade;    # Combines sliding and fading for workspaces
    animation-in = slidefade;       # Workspace enter animation
    animation-out = slidefade;      # Workspace exit animation
    animation-specialworkspace-in = slidefade; # Special workspace enter
    animation-specialworkspace-out = slidefade; # Special workspace exit
    }

**Gesture**

    gesture {
        workspace_swipe = true
        workspace_swipe_fingers = 3
        disable_while_typing = true
    }

