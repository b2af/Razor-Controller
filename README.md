# Razer Wolverine V3 Pro - ControllerViewer.com Custom Display

This project contains custom controller display files for your Razer Wolverine V3 Pro to use with [controllerviewer.com](https://controllerviewer.com).

## Overview

The Razer Wolverine V3 Pro is an Xbox-style controller with:

- Standard Xbox face buttons (A, B, X, Y)
- D-Pad (4 directions)
- Left and Right analog sticks (with click buttons L3/R3)
- Triggers (LT, RT)
- Bumpers (LB, RB)
- Additional back buttons (M1, M2, M3, M4 or remappable paddles)
- View, Menu, and Xbox buttons

## Files in This Project

- `controller-config.json` - Main configuration file mapping controller inputs
- `controller-layout.svg` - Visual SVG representation of your controller
- `styles.css` - Custom styling and animations for button presses

## How to Use with ControllerViewer.com

### Method 1: Using the Website Builder

1. Go to [controllerviewer.com](https://controllerviewer.com)
2. Click "Create Custom Controller" or "Editor"
3. Choose "Xbox" as the base template (closest to Wolverine V3 Pro)
4. Import your `controller-config.json` file
5. Upload your `controller-layout.svg` file
6. Apply `styles.css` for custom styling
7. Test with your controller connected
8. Generate the viewer URL to use in OBS or browser source

### Method 2: Direct Integration

1. Connect your Razer Wolverine V3 Pro via USB or Bluetooth
2. Visit controllerviewer.com
3. Allow controller access when prompted
4. Select your controller from the list
5. Use the "Import Theme" option to load your files
6. Customize colors, animations, and button positions
7. Save your configuration

## Customization Guide

### Editing the SVG Layout

Open `controller-layout.svg` in a vector graphics editor like:

- Adobe Illustrator
- Inkscape (free)
- Figma
- VS Code with SVG extension

Each button element has an ID that matches the configuration file for easy mapping.

### Modifying the Configuration

Edit `controller-config.json` to:

- Remap button positions
- Change button colors
- Adjust animation timings
- Add custom labels

### Styling

Edit `styles.css` to customize:

- Button press animations
- Color schemes
- Opacity effects
- Shadows and glows

## Testing Your Setup

1. Open `controller-layout.svg` in a browser to preview the layout
2. Connect your controller to test button mappings
3. Use controllerviewer.com's test mode to verify all buttons register correctly
4. Adjust the configuration as needed

## Tips for Streaming

- Use a chroma key background (green/blue) for easy OBS integration
- Keep animations subtle to avoid distracting from gameplay
- Test visibility at different stream resolutions
- Consider creating multiple themes for different games

## Resources

- [ControllerViewer.com Documentation](https://controllerviewer.com/docs)
- [YouTube Tutorial](https://www.youtube.com/watch?v=Si3M0SGghbg&t=356s)
- [SVG Editing Guide](https://developer.mozilla.org/en-US/docs/Web/SVG)

## Troubleshooting

**Controller not detected:**

- Ensure Razer Synapse is updated
- Try USB connection instead of Bluetooth
- Check browser permissions for gamepad access

**Buttons not mapping correctly:**

- Verify button IDs in the SVG match the config file
- Some browsers may have different gamepad APIs
- Test in Chrome/Edge for best compatibility

**Custom design not showing:**

- Clear browser cache
- Verify SVG file is valid XML
- Check console for errors

## License

Free to use and modify for personal use.
