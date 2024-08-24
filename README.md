# pytimer
A tatsumato inspired CLI pomodoro timer in Python, adapted for Hyprland. It takes on flag arguments for the work and break times, and can do the following as well:
- Switch to an app on work time, and make it fullscreen.
- Lock the screen on break time, and unlock it when break time ends.
- Run the wayland app launcher wofi on break time.

The script will also log the pomodoro's work length, date, and category in an SQL database. No query tool is included as this is meant to be a standalone script (above dependencies to Hyprland notwithstanding).

Flags:
```
-n: Number of pomodoro cycles. Default 4
-t: Pomodoro time in minutes. Default 13
-b: Break length in minutes. Default 2
-l: Long break length in minutes. Default 3
-f: Number of cycles before a long break. Default 4
-c: Category for logging. Default none (input string)
-F: Launches or switches to the specified app. Default none (input string)
-L: Locks the screen at the start of each break. Default false
-W: Launches wofi at the start of each break. Default false
```

Example usage:
```
pytimer -n 4 -t 25 -b 5 -l 10 # Classic pomodoro timer
pytimer -c chinese -F anki -L # Vocab study timer
```

Remember to move the pytimer script to your path.
