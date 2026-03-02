# Quick Start Guide for ControllerViewer.com

Based on the tutorial: https://www.youtube.com/watch?v=Si3M0SGghbg&t=356s

## Step-by-Step Instructions

### 1. Test Your Setup Locally (5 minutes)

1. **Open the test file:**
   - Double-click `test-viewer.html` in this folder
   - It will open in your default browser

2. **Connect your Razer Wolverine V3 Pro:**
   - Connect via USB or Bluetooth
   - Click "Connect Controller" button
   - Press any button to verify detection

3. **Test all inputs:**
   - Press each button to see it light up
   - Move both analog sticks
   - Pull both triggers
   - Test all D-pad directions
   - Verify back paddles (M1-M4) if configured

### 2. Customize Your Design (10-15 minutes)

#### Option A: Edit in Inkscape (Free)

```
1. Download Inkscape: https://inkscape.org/
2. Open controller-layout.svg
3. Modify colors, add your logo, adjust layout
4. Save the file
5. Refresh test-viewer.html to see changes
```

#### Option B: Edit in VS Code

```
1. Open controller-layout.svg in VS Code
2. Install "SVG Preview" extension
3. Edit colors in the <defs> section
4. Change button colors by editing fill attributes
5. Save and preview in test-viewer.html
```

#### Colors to customize:

- Line 8-9: Main controller body gradient
- Lines 67-117: Button colors (A, B, X, Y)
- Lines 15-16: Razer green glow effect
- Line 190: Razer logo color

### 3. Upload to ControllerViewer.com (5-10 minutes)

#### Method 1: Direct Upload (Easiest)

1. Go to https://controllerviewer.com
2. Click "Create" or "New Controller"
3. Choose "Upload Custom Controller"
4. Upload `controller-layout.svg`
5. Upload `styles.css`
6. Upload `controller-config.json`
7. Click "Test" and press buttons on your controller
8. Save your configuration

#### Method 2: Use Their Editor

1. Go to https://controllerviewer.com
2. Click "Editor" or "Controller Editor"
3. Select "Xbox Controller" as base template
4. In the editor:
   - Click "Import SVG" → upload controller-layout.svg
   - Click "Import Config" → upload controller-config.json
   - Click "Import Styles" → paste contents of styles.css
5. Use their visual editor to fine-tune positions
6. Test with your controller
7. Click "Save" or "Generate Link"

### 4. Add to OBS/Streaming Software (5 minutes)

#### For OBS Studio:

```
1. In ControllerViewer.com, click "Share" or "Get URL"
2. Copy the viewer URL (looks like: https://controllerviewer.com/view/your-id)
3. In OBS, add a "Browser Source"
4. Paste the URL
5. Set width: 440, height: 280 (or scale as needed)
6. Check "Shutdown source when not visible"
7. For transparency: In the CSS section, add:
   body { background-color: rgba(0,0,0,0); }
```

#### For Streamlabs:

```
1. Add "Widget" → "Browser Source"
2. Paste your ControllerViewer URL
3. Set dimensions to 440x280
4. Enable hardware acceleration
```

#### For XSplit:

```
1. Add Source → Web Page
2. Enter your ControllerViewer URL
3. Set size and position
```

### 5. Pro Tips from the Video

✅ **Positioning in stream:**

- Bottom-left or bottom-right corner works best
- Scale to about 20-30% of your screen size
- Keep it away from important UI elements

✅ **Chroma key (green screen):**

- Open `test-viewer.html`
- Click "Green Screen" button
- Use OBS Chroma Key filter (right-click Browser Source → Filters → + → Chroma Key)
- Set color to #00FF00
- Adjust similarity and smoothness

✅ **Streaming performance:**

- Use hardware acceleration in OBS settings
- Set browser source FPS to 30-60
- Disable "Refresh browser when scene becomes active"

✅ **Visual customization:**

- Add your logo to the SVG (around line 186-192)
- Change Razer green (#44D62C) to your brand color
- Adjust button sizes in the SVG for better visibility

### 6. Common Issues & Fixes

**Problem: Controller not detected**

- Solution: Update Razer Synapse software
- Try USB connection instead of Bluetooth
- Use Chrome or Edge browser (better gamepad API support)
- Check browser permissions for gamepad access

**Problem: Buttons not mapping correctly**

- Solution: In controller-config.json, check the "mappings" section
- Different controllers may have different button indices
- Test in test-viewer.html and note which buttons light up
- Update the buttonMap in the config file

**Problem: SVG not showing on ControllerViewer.com**

- Solution: Validate your SVG at https://validator.w3.org/
- Remove any invalid XML or special characters
- Ensure all IDs in SVG match the config file
- Check the browser console for errors

**Problem: Lag or stuttering**

- Solution: Reduce SVG complexity (fewer filters/effects)
- In styles.css, reduce animation durations
- Disable drop-shadow filters if performance is critical
- Use simpler shapes instead of complex paths

**Problem: Colors look washed out in stream**

- Solution: Increase color saturation in your streaming software
- Use brighter colors in the SVG
- Adjust OBS color correction filter
- Enable "Hardware Acceleration" in OBS

### 7. Advanced Customization

**Add your Twitch/YouTube logo:**

```svg
<!-- Add this inside the SVG, before </svg> tag -->
<image x="180" y="240" width="80" height="20"
       href="your-logo.png" opacity="0.8"/>
```

**Change button text to icons:**

- Replace text content with Unicode symbols
- Find icons at: https://unicode-table.com/
- Example: ★ ♠ ♣ ♥ ♦ ▲ ▼ ◄ ►

**Add combo indicators:**

- Edit the JavaScript in test-viewer.html
- Track button combinations
- Display special effects for fighting game inputs

**Animate on button press:**

- In styles.css, modify .face-button.pressed
- Add complex animations using @keyframes
- Example: pulse, bounce, rotate effects

## Need More Help?

- Video tutorial: https://www.youtube.com/watch?v=Si3M0SGghbg&t=356s
- ControllerViewer docs: https://controllerviewer.com/docs
- SVG reference: https://developer.mozilla.org/en-US/docs/Web/SVG
- OBS forums: https://obsproject.com/forum/

## File Summary

- `README.md` - Full documentation
- `QUICKSTART.md` - This file
- `controller-layout.svg` - Visual design (edit this for appearance)
- `controller-config.json` - Button mappings (edit for button positions)
- `styles.css` - Animations and effects (edit for styling)
- `test-viewer.html` - Local testing page (open in browser)

**Next Step:** Open `test-viewer.html` in your browser and connect your controller!
