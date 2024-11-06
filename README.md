# Auto-Pause Media When Headphones Disconnect

When using wireless headphones on Linux, it's common for media playback to continue playing through the speakers without any warning when the headphones die or disconnect. On mobile devices, however, media typically pauses automatically.

This simple systemd service brings that expected behavior to Linux: it pauses media playback when your Bluetooth headphones disconnect, providing a more intuitive experience.

### Step 1: Save the Files
Copy these two files into the following directory:
```
cp playerctl-pause.path ~/.config/systemd/user/playerctl-pause.path
```
```
cp playerctl-pause.service ~/.config/systemd/user/playerctl-pause.service
```

### Step 2: Reload the Systemd Daemon
Run the following command to reload the systemd configuration:
```
systemctl --user daemon-reload
```

### Step 3: Enable and Start the Service
Enable and start the `playerctl-pause.path` service immediately:
```
systemctl --user enable --now playerctl-pause.path
```
