----->WORKSCAPE-AURAGEN>-----

Workscape: The logic that maps your virtual workspace to a specific color folder.
Auragen: The bridge that takes Matugen's output and forces your ASUS keyboard RGB to match.

Required Files:

->switch_and_theme.sh (Main logic)

->change-wallpaper.sh (Wallpaper rotation)

->keyb.sh (RGB injection)

->matugen installed and configured (Binary)

->asusctl (Binary)

->the custom matugen template for the keyboard script(auragen)


Instructions:
1)
    Verify asusctl aura -c 000000 works.
    
2)
    copy the template css into your templates folder for matugen
  
3)
    Add the template path to your matugen conf.toml.
  
4)
    create a scripts folder inside hypr cofig folder, copy the swith_and_theme.sh file into here
  
5)
    copy the change-wallpaper.sh and keyb.sh into hypr folder itself
  
6)
    make sure you have 5 folders(can be same as mine) inside a 'Wallpapers' in your Downloads folder 
    NOTE: if you wanna use diff directory or diff amount of folders/worskpaces linked, you must change the change-wallpaper.sh file directly,
   
7)
    Hyprland:
Add this to your hyprland config file:

---------------------------------------------------------------------------------------
 
     bind = SUPER, W, exec, ~/.config/hypr/change-wallpaper.sh
    
    # Switch to workspace with mainMod + [0-9]
    
    bind = $mainMod, 1, exec, ~/.config/hypr/scripts/switch_and_theme.sh 1
    
    bind = $mainMod, 2, exec, ~/.config/hypr/scripts/switch_and_theme.sh 2
    
    bind = $mainMod, 3, exec, ~/.config/hypr/scripts/switch_and_theme.sh 3
    
    bind = $mainMod, 4, exec, ~/.config/hypr/scripts/switch_and_theme.sh 4
    
    bind = $mainMod, 5, exec, ~/.config/hypr/scripts/switch_and_theme.sh 5
    
    bind = $mainMod, 6, exec, ~/.config/hypr/scripts/switch_and_theme.sh 6
    
    bind = $mainMod, 7, exec, ~/.config/hypr/scripts/switch_and_theme.sh 7
    
    bind = $mainMod, 8, exec, ~/.config/hypr/scripts/switch_and_theme.sh 8
    
    bind = $mainMod, 9, exec, ~/.config/hypr/scripts/switch_and_theme.sh 9
    
    bind = $mainMod, 0, exec, ~/.config/hypr/scripts/switch_and_theme.sh 10
    
    
    # Move active window to a workspace and switch focus
    
    # Note: We still need the initial movetoworkspace command here.
    
    bind = $mainMod SHIFT, 1, exec, hyprctl dispatch movetoworkspace 1; ~/.config/hypr/scripts/switch_and_theme.sh 1
    
    bind = $mainMod SHIFT, 2, exec, hyprctl dispatch movetoworkspace 2; ~/.config/hypr/scripts/switch_and_theme.sh 2
    
    bind = $mainMod SHIFT, 3, exec, hyprctl dispatch movetoworkspace 3; ~/.config/hypr/scripts/switch_and_theme.sh 3
    
    bind = $mainMod SHIFT, 4, exec, hyprctl dispatch movetoworkspace 4; ~/.config/hypr/scripts/switch_and_theme.sh 4
    
    bind = $mainMod SHIFT, 5, exec, hyprctl dispatch movetoworkspace 5; ~/.config/hypr/scripts/switch_and_theme.sh 5
    
    bind = $mainMod SHIFT, 6, exec, hyprctl dispatch movetoworkspace 6; ~/.config/hypr/scripts/switch_and_theme.sh 6
    
    bind = $mainMod SHIFT, 7, exec, hyprctl dispatch movetoworkspace 7; ~/.config/hypr/scripts/switch_and_theme.sh 7
    
    bind = $mainMod SHIFT, 8, exec, hyprctl dispatch movetoworkspace 8; ~/.config/hypr/scripts/switch_and_theme.sh 8
    
    bind = $mainMod SHIFT, 9, exec, hyprctl dispatch movetoworkspace 9; ~/.config/hypr/scripts/switch_and_theme.sh 9
    
    bind = $mainMod SHIFT, 0, exec, hyprctl dispatch movetoworkspace 10; ~/.config/hypr/scripts/switch_and_theme.sh 10
    
-------------------------------------------------------------------------------------


Author's Note

I'm a first-year Chemistry student at IIT Madras. I built this because I wanted my physical hardware to feel like an extension of my virtual environment.

This is an early-stage project. I'm still learning! Feel free to fork, optimize, or suggest changes. If you find a way to make the color transitions even smoother or lower on resources, I'd love to see it.


