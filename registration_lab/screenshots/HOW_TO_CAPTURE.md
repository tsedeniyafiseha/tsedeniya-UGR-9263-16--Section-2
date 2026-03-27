# How to Capture Screenshots

## 1. App Screenshot

### Method 1: Using Windows Snipping Tool
1. Run your Flutter app: `flutter run -d chrome`
2. Wait for the app to load in Chrome
3. Press `Windows + Shift + S` to open Snipping Tool
4. Select the app window area
5. Save as `app-screenshot.png` in this folder

### Method 2: Using Browser DevTools
1. Open the app in Chrome
2. Press `F12` to open DevTools
3. Click the device toolbar icon (or press `Ctrl + Shift + M`)
4. Right-click on the page and select "Capture screenshot"
5. Save as `app-screenshot.png` in this folder

## 2. Widget Tree Screenshot

### Using Flutter DevTools:
1. Run your app: `flutter run -d chrome`
2. Look for this line in the terminal:
   ```
   The Flutter DevTools debugger and profiler on Chrome is available at:
   http://127.0.0.1:XXXXX/...
   ```
3. Open that URL in your browser
4. Click on the "Widget Inspector" tab (tree icon)
5. The widget tree will be displayed on the left side
6. Take a screenshot of the widget tree panel
7. Save as `widget-tree.png` in this folder

### Alternative: Use the Widget Tree from README
The README.md file already contains a text-based widget tree diagram that you can reference.

## Quick Screenshot Checklist

- [ ] Run the app: `flutter run -d chrome`
- [ ] Capture app screenshot showing the registration form
- [ ] Open Flutter DevTools from the terminal URL
- [ ] Capture widget tree from the Widget Inspector tab
- [ ] Save both images in the `screenshots/` folder
- [ ] Verify images are named correctly:
  - `app-screenshot.png`
  - `widget-tree.png`
