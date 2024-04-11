# android-clean
# Android optimization script for Termux
# This script performs the following optimizations:
# 1. Set maximum FPS
# 2. Clear junk cache
# 3. Improve performance
# 4. Extend battery life
# 5. Speed up app responsiveness

import os

def set_max_fps():
    # Set maximum FPS for smoother animations
    os.system("settings put global animator_duration_scale 0.5")
    os.system("settings put global transition_animation_scale 0.5")
    os.system("settings put global window_animation_scale 0.5")

def clear_junk_cache():
    # Clear app cache and system cache
    os.system("pm clear com.android.systemui")
    os.system("pm clear com.android.providers.downloads")
    os.system("pm clear com.android.providers.media")
    os.system("pm clear com.android.providers.calendar")
    os.system("pm clear com.android.providers.contacts")
    os.system("pm clear com.android.providers.userdictionary")
    os.system("pm clear com.android.providers.settings")

def improve_performance():
    # Optimize system performance
    os.system("pm disable com.android.inputmethod.latin")
    os.system("pm disable com.android.systemui")
    os.system("pm disable com.android.providers.downloads")
    os.system("pm disable com.android.providers.media")
    os.system("pm disable com.android.providers.calendar")
    os.system("pm disable com.android.providers.contacts")
    os.system("pm disable com.android.providers.userdictionary")
    os.system("pm disable com.android.providers.settings")

def extend_battery_life():
    # Disable unnecessary services to save battery
    os.system("pm disable com.android.bluetooth")
    os.system("pm disable com.android.nfc")
    os.system("pm disable com.android.location.fused")
    os.system("pm disable com.android.location.gps")
    os.system("pm disable com.android.location.network")
    os.system("pm disable com.android.location.passive")

def speed_up_responsiveness():
    # Improve app responsiveness
    os.system("pm disable com.android.inputmethod.latin")
    os.system("pm disable com.android.systemui")
    os.system("pm disable com.android.providers.downloads")
    os.system("pm disable com.android.providers.media")
    os.system("pm disable com.android.providers.calendar")
    os.system("pm disable com.android.providers.contacts")
    os.system("pm disable com.android.providers.userdictionary")
    os.system("pm disable com.android.providers.settings")

if __name__ == "__main__":
    set_max_fps()
    clear_junk_cache()
    improve_performance()
    extend_battery_life()
    speed_up_responsiveness()

    print("Android optimization completed successfully!")


