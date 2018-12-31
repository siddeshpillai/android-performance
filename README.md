# android-performance
Android Performance Improvements

### Battery Historian
Refer: https://github.com/google/battery-historian

Inorder to use Battery Historian install docker
Run this command $ docker run -p 5665:9999 gcr.io/android-battery-historian/stable:3.0 --port 9999
http://localhost:9000/

To view battery stats
run the following commands
0. adb kill-server
1. adb devices
2. adb shell dumpsys batterystats > batterystats.txt
3. adb shell dumpsys batterystats > com.example.sunshine.app > sunshine.txt
4. python historian.py sunshine.txt > sunshine_battery_stats.html
