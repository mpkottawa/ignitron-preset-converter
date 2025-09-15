


<img width="1024" height="1024" alt="IPF" src="https://github.com/user-attachments/assets/51e9db7b-563d-460e-b52d-32089fdc3859" />




# ignitron-preset-tool
automatically pull json preset files loaded onto ignitron pedal over usb connection


Ignitron Preset Converter / Manager
-----------------------------------
A one-stop Python utility for working with presets on the Ignitron pedal.
Features:
- Convert serial output from Ignitron into individual JSON preset files
- Create preset index (filename.json UUID) with UUID in uppercase
- Convert stored .txt / .log files from VSCode or other logs
- Build PresetList.txt interactively using a drag-and-drop GUI
- Export PresetList_*.txt to the ./dist/ folder (filenames only, no UUIDs)
- Serial live capture of all presets (LISTPRESETS)
- Serial live capture of only the pedal’s active presets (LISTBANKS + LISTPRESETS)
Prerequisites:
- Python 3.8+
- pyserial (pip install pyserial)
- Tkinter (bundled with most Python installs)
Usage:
Run the tool:
python ignitron_preset_converter.py
Menu Options:
1. Convert a single log file
2. Convert a folder of log files
3. Convert a full dump file
4. Build PresetList.txt from presets (GUI)
5. Live capture from Ignitron over Serial (ALL presets)
6. Live capture from Ignitron (ONLY presets in pedal’s PresetList)
7. Exit
Serial Live Capture:
- Select a serial port from the numbered list.
- Enter baud rate (default 115200).
- Hold down Preset 1 on the pedal when pressing Enter after baud entry.
- Captures presets to JSON files, index, and optionally PresetList.txt in ./dist.
Outputs:
- presets_json_YYYY-MM-DD_HH-MM/ : one JSON per preset
- preset_index_YYYY-MM-DD_HH-MM.txt : filename + UUID (uppercase)
- ./dist/PresetList_YYYY-MM-DD_HH-MM.txt : exported preset list (filenames only)
Packaging to EXE (Windows):
pip install pyinstaller
pyinstaller --noconfirm --onefile --name "IgnitronPresetConverter"
ignitron_preset_converter.py
Enjoy managing your Ignitron presets!
