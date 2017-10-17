# Custom Components

SubGraph (.pxg) files are a way of reusing and sharing custom components or groups of components for use with [Praxis LIVE](http://www.praxislive.org)

## Usage

Download the [latest zip file](https://github.com/praxis-live/pxg/archive/master.zip) and extract the contents. Drag .pxg files into your patch from the File Browser tab, or import them into your palette (choose `Import` from the popup menu on palette categories).

## Components

Under active development - lots more to come! Components marked experimental may not be well tested or fully functional.

### Core

Components that can be used in any graph (audio, video, tinkerforge, etc.).

* `seconds.pxg` - output running time in seconds.
* `array-map.pxg` (experimental) - map a range from 0 to 1 to values in an array.
* `normalize.pxg` (experimental) - normalize incoming signals to between 0 and 1.

### Audio

Components that can be used in any audio graph.

* `mixer-6s.pxg` - stereo 6-channel mixer.
* `mono-kit.pxg` - simple 6-sample player with triggers and levels. Useful for drum samples.
* `synth-base.pxg` - basis for a monophonic synthesizer.
* `synth-duo-osc.pxg` - monophonic analog style synthesizer with two oscillators and resonant filter with envelope modulation.
* `synth-pm3.pxg` - monophonic phase-modulation synthesizer.

### Video

Components that can be used in any video graph.

* `colourbalance.pxg` - alter the rgb balance of a video input.
* `xform.pxg` - 2D transform (translate, scale, rotate) a video input.
* `framerate.pxg` (experimental) - measure framerate of video passing through component.

### VideoGL

Video components that can only be used with the OpenGL renderer.

* `fx-kaleidoscope.pxg` - kaleidoscope effect with controllable number of segments. GLSL code derived from https://github.com/neilmendoza/ofxPostProcessing/blob/master/src/KaleidoscopePass.cpp
* `fx-noise-warp.pxg` - noise warp image effect. GLSL code derived from https://github.com/ashima/webgl-noise
* `fx-pinch.pxg` - pinch image effect.
* `gl-filter-base.pxg` - GLSL filter base - add to graph and edit fragment (GLSL) and code (Java/Processing).
* `gl-gradients.pxg` - simple mouse reactive OpenGL source example. GLSL code from http://weworkweplay.com/play/introduction-to-glsl-and-fragment-pixel-shaders/
* `glsl-io-transitions.pxg` (experimental) - range of video transition effects between two sources, ported from GLSL.io
* `gl-source.pxg` - GLSL source base = add to graph and edit fragment (GLSL) and code (Java/Processing). Supports most shaders from GLSL Sandbox directly.
* `gl-svg.pxg` - SVG viewer (and example of SVG loading).
* `gl-text.pxg` - text component (and example of text rendering). **Requires a .ttf font file to be set.**
* `isf-edges.pxg` edges video filter ported from https://www.interactiveshaderformat.com/sketches/184
* `isf-solarize.pxg` - solarize video filter ported from https://www.interactiveshaderformat.com/sketches/390
* `xform-3d.pxg` - translate and rotate a video input in 3D space.

### TinkerForge

TinkerForge binding components.

* `rotary-encoder.pxg` - binding for the rotary encoder bricklet.

## Create your own SubGraph (.pxg) file

Simply select the component(s) you wish to reuse within the patcher window, right-click and select `Export` to save a PXG file. You can then drag this file from the File Manager into the patcher window, or import into the palette.

Please share!
