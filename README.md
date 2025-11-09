# spansaver
Dual-Monitor Spanning Screensaver for Linux Mint
![SPANSAVER GUI Screenshot](screenshot_main.png)
![SPANSAVER Dual-Monitor View](screenshot_dual.png)
*Dual-monitor panoramic screensaver running in full 3480x1080 glory*


SPANSAVER v1.0
==========================
Developed by: James Witterschein (State Exam Pass) and EVE
License: MIT License
Tested on: Linux Mint 22.1 Cinnamon

---------------------------------------------------------------
ABOUT SPANSAVER
---------------------------------------------------------------
SPANSAVER is a lightweight, dual-monitor panoramic screensaver system 
for Linux Mint. It cycles through 3480x1080 images from your 
~/3480x1080 folder, smoothly spanning both displays.

---------------------------------------------------------------
HOW SPANSAVER RUNS ON YOUR SYSTEM
---------------------------------------------------------------
SPANSAVER runs as a normal user app. By default, it uses a local 
Python virtual environment (.venv) to keep everything clean and 
self-contained.

What .venv is (and isn’t):
- Not a security sandbox.
- Just a private folder with Python packages SPANSAVER needs.
- Keeps SPANSAVER separate from your system Python setup.

Security & permissions:
- Runs as a normal user (no root/sudo required).
- Fully offline, no network activity.
- Security-tested with Bandit and pip-audit tools.
- Memory-tested: stable at ~12.8 MB average use.

Advanced users may install dependencies globally:
    sudo apt install -y python3-pyqt6 python3-psutil
    python3 gui/main.py

---------------------------------------------------------------
INSTALLATION INSTRUCTIONS
---------------------------------------------------------------
1. Download SPANSAVER v1.0 from:
   https://github.com/StateExamPass/spansaver/releases/tag/v1.0

2. Extract the package:
   cd ~/Downloads
   tar -xzf spansaver-v1.0.tar.gz -C ~

3. Enter the folder:
   cd ~/spansaver

4. Set up environment and install dependencies:
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt

5. Run the installer script:
   bash install.sh

6. Launch SPANSAVER:
   ~/spansaver/run_spansaver.sh

---------------------------------------------------------------
USAGE
---------------------------------------------------------------
- Use “Start Timer” to activate the countdown.
- Move your mouse to reset timer.
- “Test Screensaver Now” immediately starts the slideshow.
- Images should span both monitors.
- Exit via tray icon > Quit.

---------------------------------------------------------------
UNINSTALL
---------------------------------------------------------------
1. Stop SPANSAVER (tray icon > Quit).
2. Remove autostart entry if enabled:
   Menu > Preferences > Startup Applications > Remove SPANSAVER
3. Delete its folder:
   rm -rf ~/spansaver
