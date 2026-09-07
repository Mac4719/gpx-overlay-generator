# gpx-overlay-generator
A simple browser-based GPX overlay generator for cycling videos. Upload a GPX file, automatically detect available telemetry, select individual data boxes, drag and resize them on a 16:9 canvas, preview the animated data, and export a transparent video overlay. Everything runs locally with no cloud processing.
# GPX Overlay Generator

A simple, browser-based tool for creating animated cycling telemetry overlays from GPX files.

Upload a GPX file, choose the telemetry you want to display, position the individual overlay boxes, preview the animation, and export the result.

## Features

* Drag and drop GPX files
* Automatically detects available GPX data
* Select as many or as few telemetry overlays as required
* Individual, independently positioned overlay boxes
* Drag and resize overlay elements
* 16:9 preview canvas
* Animated telemetry based on GPX timestamps
* Timeline playback and scrubbing
* GPX course/map overlay with moving position marker
* Smooth interpolation between GPX data points
* Support for common Garmin GPX extensions
* Runs locally in the browser
* No account required
* No cloud processing
* GPX data remains on the user's device

## Available Overlays

Depending on the information contained in the GPX file, the following overlays may be available:

* Speed
* Distance
* Elevation
* Gradient
* Course
* Heart Rate
* Cadence
* Power
* Temperature
* Elapsed Time
* Average Speed
* Maximum Speed
* Elevation Gain
* Distance Remaining

The application only makes overlays available when the required data can be obtained or calculated.

## How It Works

### 1. Load a GPX

Drag a GPX file into the application or use the file picker.

The application analyses the GPX and determines what information is available.

### 2. Select Overlays

Choose which telemetry elements you want to use.

You can select one overlay or as many as are available.

Each selected telemetry item becomes its own independent box.

### 3. Position the Overlays

Use the 16:9 canvas to position the boxes.

Each element can be:

* Moved
* Resized
* Positioned independently

This allows the overlay layout to be customised for different video compositions.

### 4. Preview

Use the timeline to preview the GPX animation.

Telemetry values update as the timeline moves, and the Course marker follows the GPS track.

### 5. Export

Export the completed overlay for use over video footage.

The overlay contains telemetry only, with no video background.

## GPX Support

The application supports common GPX structures including:

* `trk`
* `trkseg`
* `trkpt`
* `time`
* `ele`

It also attempts to read common sensor extensions for:

* Heart rate
* Cadence
* Power
* Temperature

Different devices and applications can structure GPX extensions differently, so available telemetry can vary between files.

## Calculated Data

Where required, the application calculates values from the available GPS and elevation data.

These can include:

* Distance
* Speed
* Gradient
* Elevation gain
* Average speed
* Maximum speed
* Distance remaining

GPS and elevation data may be smoothed where necessary to reduce noise and unrealistic values.

## Privacy

The application is designed to process GPX files locally.

GPX files do not need to be uploaded to a server.

No account is required.

No third-party mapping service is required for the Course overlay.

## Running Locally

The application can be run by opening the HTML application in a modern web browser.

For the best compatibility with browser file and export features, serving the application through a local web server or hosting it through a service such as GitHub Pages may be preferable to opening it directly using a `file://` URL.

## Hosting

The application can be hosted as a static website because the core application runs entirely in the browser.

GitHub Pages is one option for hosting the application.

Once hosted, users can open the application through a normal web address without installing anything.

## Video Transparency

Transparent video export depends on browser and codec support.

A normal H.264 MP4 with a black background is **not** considered a transparent overlay.

Where the browser cannot directly create an alpha-capable video, an appropriate alpha-capable format or local conversion workflow should be used.

Suitable formats may include:

* ProRes 4444 with alpha
* WebM with alpha

The exported result should contain genuine transparency rather than a simulated black background.

## Project Status

This project is designed as a lightweight tool for creating custom GPX-based cycling telemetry overlays.

The application is intended to remain simple:

**Load GPX → Select → Position → Preview → Export**

## Future Improvements

Possible future additions include:

* Additional telemetry types
* More visual themes
* Custom fonts
* More styling controls
* Improved course visualisation
* Additional export formats
* 4K export
* Vertical 9:16 video support
* Saved overlay presets
* Project import/export
* Automatic video/GPX synchronisation

## License

Add the project's chosen license here.

If no license has been selected, the project remains subject to the default copyright rules of its author.
