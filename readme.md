

Data for each device should be placed in a separate directory, with `device.json` file describing the device:

- **`type`** should be one of the `phone`, `tablet`, `notebook`, `desktop`, `unknown`;
- **`capabilities`** should listen enabled capabilities for the device (currently supported: `mobile`, `touch`);
- **`screen`** describes the physical device screen size and dpr in horizontal and vertical orientations;
- **`outline`** provides an image to draw around the screen;
- **`modes`** represent different browser states on the screen (e.g. with/without on-screen keyboard);
- **`page-rect`** is the rect relative to the `screen` size (see above), where web page is displayed; this rect will be emulated;
- **`title`** values should be user-readable.

All sizes in should be in device independent pixels

# Deployment

Run the following to update devices.json:
```sh
python generate_devices_list.py
```
