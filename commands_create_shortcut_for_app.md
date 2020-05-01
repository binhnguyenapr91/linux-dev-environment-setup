# CREATE SHORTCUT ICON 
1.Open a text editor: copy and paste the following text into the editor:

    [Desktop Entry]
    Version=1.0
    Name=Eclipse
    Comment=Java IDE
    Type=Application
    Categories=Development;IDE;
    Exec=/home/{username}/Programs/eclipse/eclipse
    Terminal=false
    StartupNotify=true
    Icon=/home/{username}/Programs/eclipse/icon.xpm
    Name[en_US]=Eclipse

- Update any paths if you extracted Eclipse to a different location
- Save the file as eclipse.desktop in /home/{username}/.local/share/applications/
- Reboot your machine
- Search for Eclipse
- Drag and drop the Eclipse icon to the launcher
