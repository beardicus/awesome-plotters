# Awesome Plotters [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of code and resources for pen plotters and other robots that draw.

## Contents

- [Hardware](#hardware)
  - [Plotters](#plotters)
  - [Motor Controllers](#motor-controllers)
  - [Accessories](#accessories)
  - [Pens](#pens)
- [Software](#software)
  - [HPGL](#hpgl)
  - [G-code](#g-code)
  - [Plotter-Specific](#plotter-specific)
  - [Vector Creation](#vector-creation)
  - [Vector Utilities](#vector-utilities)
  - [Fonts](#fonts)
- [Inspiration and Instruction](#inspiration-and-instruction)
- [Community](#community)
- [Plotter Art For Sale](#plotter-art-for-sale)
- [Other Awesomes](#other-awesomes)

## Hardware

### Plotters

- [AxiDraw](https://shop.evilmadscientist.com/productsmenu/846) – Pen plotter from [Evil Mad Scientist](https://www.evilmadscientist.com), very popular on [#plottertwitter](https://twitter.com/hashtag/plottertwitter).
- [Line-us](https://www.line-us.com) – A cute little kickstarted robotic drawing arm.
- [Makeblock XY Plotter](http://learn.makeblock.com/en/xy-plotter-robot-kit) – Hackable XY plotter kit (discontinued?).
- [Drawing Robot](https://www.thingiverse.com/thing:2349232) – 3d-Printable AxiDraw clone w/ [Arduino CNC Shield](https://blog.protoneer.co.nz/arduino-cnc-shield) controller running grbl firmware.
- [WaterColorBot](https://watercolorbot.com) – XY art robot and software to plot with watercolor paints.
- [EggBot](https://egg-bot.com) – Pen plotter for egg-shaped and spherical objects.
- [HP Pen Plotters](https://www.hpmuseum.net/exhibit.php?class=4&cat=24) – Vintage desktop and floor-standing pen plotters from the creator of the HPGL standard. Model 7475A is very common and can usually be found on eBay.
- [Roland Pen Plotters](https://www.youtube.com/watch?v=6_pwzqPk6Gg) (YouTube) – Vintage flatbed HPGL pen plotters. Search eBay for "roland dxy".
- [Polargraph](http://www.polargraph.co.uk) – The original polargraph hardware and software project.
- [Makelangelo](http://www.makelangelo.com) – Open source polargraph artbot.

### Motor Controllers

- [grblShield](https://github.com/synthetos/grblShield) – All the stepper motor control hardware needed to turn an [Arduino](https://www.arduino.cc) into a G-code-based motion controller using the grbl firmware. ([adafruit](https://www.adafruit.com/product/1750))
- [TinyG](https://github.com/synthetos/TinyG) – More featureful and robust 6-axis G-code-based motion control hardware. ([adafruit](https://www.adafruit.com/product/1749))
- [Arduino CNC Shield](https://blog.protoneer.co.nz/arduino-cnc-shield) – Grbl-compatible stepper motor control shield for Arduino, similar to the [grblShield](https://github.com/synthetos/grblShield).
- [Raspberry Pi CNC Hat](https://wiki.protoneer.co.nz/Raspberry_Pi_CNC) – Raspberry Pi add-on board w/ stepper controllers and a microcontroller running grbl. Interfaces with the Pi's serial pins

### Accessories

- [WiFi232](http://biosrhythm.com/?page_id=1453) – Wifi to RS-232 serial via a DB25 plug. Control your serial plotter wirelessly.
- [Plotter Cable Pinout](http://sites.music.columbia.edu/cmc/chiplotle/plotter_cable.pdf) (PDF) – Schematic for a plotter cable that will work for most HP and Roland plotters. Search eBay or Amazon for `DB9 to DB25 Serial Null Modem Cable` or similar to find them for sale.

### Pens

- [Sharpie Fine Point Plotter Adapter](https://www.thingiverse.com/thing:229982) – 3d-printed adapter to fit a standard Sharpie in an HP-GL plotter.
- [Parametric 3d-Printable Plotter Pen Adapter](https://openjscad.org/#https://gist.githubusercontent.com/beardicus/d668c0f6b96be53d16dc/raw/plotter-pen-adapter.jscad) – Adjustable model to print adapters for various pens.
- [Plotter Pen STL Models](https://www.thingiverse.com/thing:227985) – Accurate STL models of both short and long standard plotter pens.
- [Pens for AxiDraw](https://wiki.evilmadscientist.com/Pens_for_AxiDraw) – List of pens suitable for general plotter abuse.
- [Pens for EggBot](https://wiki.evilmadscientist.com/Pen_choices) – Egg- and glass-focused pen recommendations but still generally applicable information.

## Software

### HPGL

HPGL is a serial/text-based protocol used by most old pen plotters, and even many new vinyl cutters.

- [Chiplotle](https://github.com/drepetto/chiplotle) ([web site](http://chiplotle.org)) – Python library for generating HPGL and interfacing with serial plotters.
- [HPGL Reference Guide](https://www.isoplotec.co.jp/HPGL/eHPGL.htm) – HTML-based HPGL Reference.
- [HP 7475A Interfacing and Programming Manual](https://archive.org/details/HP7475AInterfacingandProgrammingManual) – Scanned PDF manual that contains a full HPGL reference.
- [djipco/hpgl](https://github.com/djipco/hpgl) – A Node.js library to communicate with HPGL-compatible plotters and printers.
- [hp2xx](https://www.gnu.org/software/hp2xx) – GNU tool to convert HPGL into other vector and raster formats. Can also be used as a previewing in X11.
- [vec](https://github.com/anachrocomputer/vec) – Example C code for generating HPGL, with a turtle graphics interface.
- [d3-hpgl](https://github.com/aubergene/d3-hpgl) – An adapter for the HTML Canvas API so you can output HPGL using the popular [D3](https://d3js.org) library.
- [HPGL Viewer](https://github.com/drskullster/HPGLViewer) – An HPGL Viewer using Javascript and HTML5 canvas.
- [HPGL Sender](https://github.com/LgHS/hpgl-sender) – A web interface for previewing HPGL and sending it to your plotter.

### G-code

G-code is a text-based standard for controlling CNC machines. Though it was designed for industrial machines, its use in many hobbyist 3d printer firmwares has made it ubiquitous in small-scale DIY projects as well.

- [grbl](https://github.com/grbl/grbl) – A high-performance G-code interpreting firmware for the Atmega 328 microcontroller and Arduino.
- [cncjs](https://github.com/cncjs/cncjs) – A web-based interface controlling CNC machines running grbl, TinyG, or other G-code-based firmware.
- [node-gcode](https://github.com/ryansturmer/node-gcode) – Node.js-based G-code interpreter and simulator.
- [svg2gcode](https://github.com/em/svg2gcode) – Node.js-based command line utility for converting SVG to G-code.
- [svg2gcode](https://github.com/vishpat/svg2gcode) – Python-based utility for fast SVG to G-code conversion.
- [Universal-G-Code-Sender](https://github.com/winder/Universal-G-Code-Sender) – Java-based grbl-compatible cross-platform G-code sender.
- [ChiliPeppr Hardware Fiddle](http://chilipeppr.com) – Modular web-based workspaces to visualize G-code and control hardware.

### Plotter-Specific

Software that is specific to a particular plotter or controller.

- [axidraw](https://github.com/evil-mad/axidraw) – Official AxiDraw extensions for Inkscape.
- [axi](https://github.com/fogleman/axi) – Unofficial Python library for the AxiDraw v3.
- [xy](https://github.com/fogleman/xy) – Utilities for the Makeblock XY Plotter Robot Kit.
- [LaserGRBL](https://github.com/arkypita/LaserGRBL) – Laser-optimized Windows GUI for grbl controllers. Could be repurposed for DIY pen plotters that use a solenoid for pen up/down movements.
- [Line-us Inkscape Plugin](https://github.com/Line-us/Inkscape-Plugin) – Sends drawings to the [Line-us plotter](https://www.line-us.com) directly from Inkscape.
- [Line-us API Examples](https://github.com/Line-us/Line-us-Programming) – Example code for the [Line-us](https://www.line-us.com) plotter's G-code-based API.
- [PenPlotter](https://github.com/RickMcConney/PenPlotter) – Polargraph controller that uses repetier firmware.
- [Makelangelo-firmware](https://github.com/MarginallyClever/Makelangelo-firmware) – Firmware for the Makelangelo polargraph robot.
- [RoboPaint](https://github.com/evil-mad/robopaint) – Software for the WaterColorBot.
- [AxiTurtle](https://github.com/ralphcrutzen/AxiTurtle) – Turtle graphics for AxiDraw in Processing.
- [GRBL-Plotter](https://github.com/svenhb/GRBL-Plotter) – Plotter-optimized Windows GUI for grbl controller with SVG and DXF import, and flexible pen up/down control.
- [saxi](https://github.com/nornagon/saxi) – Driver and library for the AxiDraw. Uses constant-acceleration motion planning and automatically resizes to paper.

### Vector Creation

Tools to create vector artwork from scratch or by conversion from other formats.

- [Inkscape](https://inkscape.org) – Popular cross-platform open source vector graphics editor.
- [p5.js](https://p5js.org) – "Javascript library that makes coding accessible for artists, designers, educators, and beginners".
- [Paper.js](http://paperjs.org) – "The Swiss Army Knife of Vector Graphics Scripting".
- [ln](https://github.com/fogleman/ln) – Vector-based 3D renderer written in Go.
- [autotrace](https://github.com/autotrace/autotrace) – Converts bitmap images to vector graphics.
- [stipplegen](https://github.com/evil-mad/stipplegen) – Creates interesting stippled drawings from bitmap images. ([blog post](https://www.evilmadscientist.com/2012/stipplegen2))
- [SquiggleDraw](https://github.com/gwygonik/SquiggleDraw/commits/master) – "SquiggleDraw will create a SVG file from an image, using the brightness to change the amplitude of sine waves".
- [svgurt](https://svgurt.com) – Web-based PNG to SVG creative noodler.
- [maptrace](https://github.com/mzucker/maptrace) – Produce watertight polygonal vector maps by tracing raster images.
- [Drawbot_image_to_gcode_v2](https://github.com/Scott-Cooper/Drawbot_image_to_gcode_v2) – Creates G-code for use on drawbots.
- [blackstripes](https://github.com/fullscreennl/blackstripes-python-extensions) – Turns a PNG image into a SVG line drawing.
- [Ribbon](https://github.com/fogleman/ribbon) – Ribbon diagrams of proteins in written in Go.
- [penplot](https://github.com/mattdesl/penplot) – A development environment for plotter art in JavaScript.
- [penkit](https://github.com/paulgb/penkit) – A Python library for creating line-based SVG graphics.
- [generativeExamples](https://github.com/digitalcoleman/generativeExamples) – Example Processing code that generates plottable PDFs.
- [Let's make map](https://svg-exporter.netlify.com) – Web-based tool to export an SVG map from Mapzen tiles.
- [SuperformulaSVG for web](https://jasonwebb.github.io/SuperformulaSVG-for-web) – A generative line art web app.
- [scribbleplot](https://github.com/bleeptrack/scribbleplot) – Scribbly image transformations in Processing.
- [Maker.js](https://maker.js.org) – Library for creating 2D vector drawings for CNC and laser cutter machines.

### Vector Utilities

Tools to manipulate and optimize vector-based file formats.

- [svgsort](https://github.com/inconvergent/svgsort) – Path planning for plotting SVG files, reduces time spent moving with the pen up.
- [svgo](https://github.com/svg/svgo) – Node.js-based tool for optimizing SVG files.
- [Polargraph Optimizer](https://github.com/ezheidtmann/polargraph-optimizer) – Optimize drawing plan for a polargraph.
- [penkit-optimize](https://github.com/paulgb/penkit/tree/master/optimizer) – An SVG optimizer that uses a vehicle routing solver to minimize plot time.
- [svg-crowbar](https://github.com/NYTimes/svg-crowbar) – Chrome-only bookmarklet for extracting SVG from an HTML document.

### Fonts

Single-line vector fonts or "engraving fonts".

- [Summary of single line fonts](http://imajeenyus.com/computer/20150110_single_line_fonts/index.shtml) – Good information and links to other resources and fonts.
- [Hershey Vector Font](http://paulbourke.net/dataformats/hershey) – `.fnt` format of vector fonts from the 60s. Includes a good overview of the original data format of the fonts.
- [hershey-fonts](https://github.com/kamalmostafa/hershey-fonts) – C library and original font data for the Hershey fonts.
- [OneLineFonts.com](https://www.onelinefonts.com) – Commercial site with some single-line fonts available for purchase.

## Inspiration and Instruction

Blog posts, articles, tutorials, galleries, videos, et cetera.

- [An Intro to Pen Plotters](https://www.tobiastoft.com/posts/an-intro-to-pen-plotters) – Good info on getting started with old HPGL plotters.
- [1980s pen plotters of the future](https://notes.variogr.am/2012/08/12/1980s-pen-plotters-of-the-future) – Another intro to vintage pen plotters.
- [Pen Plotter Programming: The Basics](https://medium.com/@fogleman/pen-plotter-programming-the-basics-ec0407ab5929) – Some basics of programming vector paths, including sorting, joining, and simplifying.
- [On Generative Algorithms](https://inconvergent.net/generative) – Nice 13-part walkthrough of interesting algorithms.
- [Roland DG DXY-990](https://hackaday.io/project/12276-roland-dg-dxy-990) – Quickstart guide for a Roland flatbed plotter.
- [The Cohen-Sutherland Line Clipping Algorithm](https://sighack.com/post/cohen-sutherland-line-clipping-algorithm) – Detailed explanation and examples of an interesting algorithm.
- [Vera Molnár](https://www.surfacemag.com/articles/vera-molnar-in-thinking-machines-at-moma) – OG plotter artist.
- [The Recode Project](http://recodeproject.com) – "The ReCode Project is a community-driven effort to preserve computer art by translating it into a modern programming language".
- [Hektor](http://juerglehni.com/works/hektor) – The original cable-based drawbot from 2002.
- [Pen Plotter Art & Algorithms Part I](https://mattdesl.svbtle.com/pen-plotter-1) and [II](https://mattdesl.svbtle.com/pen-plotter-1) – A two-part intro to creating generative graphics for plotting.
- [Surface Projection](https://bitaesthetics.com/posts/surface-projection.html) and [Fractal Generation with L-Systems](https://bitaesthetics.com/posts/fractal-generation-with-l-systems.html) – Some techniques for creating line graphics suitable for plotting.
- [Pen Plotter Art & Algorithms](https://mattdesl.svbtle.com/pen-plotter-1) – Introduction to plotters, AxiDraw, walkthrough of the `penplot` library.
- [Surface Projection](https://bitaesthetics.com/posts/surface-projection.html) – Deep dive into surface projection and hidden line removal using Python and penplot.
- [Introduction to TSP art](https://wiki.evilmadscientist.com/TSP_art) – Resources for traveling salesman problem (single path) art.
- [Hidden wireframe removal](https://trmm.net/Hidden_Wireframe) – Discussion and links to code for wireframe removal of STL files.

## Community

Where to find other plotter and drawbot friends.

- [#plottertwitter](https://twitter.com/hashtag/plottertwitter) – Twitter hashtag with lots o' plots.
- [PlotterArt Subreddit](https://www.reddit.com/r/PlotterArt)
- [AxiDraw Subreddit](https://www.reddit.com/r/axidraw)
- [Generative Art Subreddit](https://www.reddit.com/r/generative)
- [Chiplotle-discuss](https://lists.columbia.edu/mailman/listinfo/chiplotle-discuss) – Fairly inactive mailing list for the Chiplotle HPGL Python library with some general plotter talk.

## Plotter Art For Sale

- [Paul Rickards](http://biosrhythm.com/?page_id=1569)
- [Michael Fogleman](https://www.michaelfogleman.com/plotter)
- [inconvergent](http://buy.inconvergent.net)
- [Customized Streetart](https://www.literalstreetart.com) – Customizable maps with optional pen plotter output.
- [Monica Rizzolli](https://www.saatchiart.com/account/artworks/155196)
- [EmergentDesign](https://emergentdesign.bigcartel.com/products)

## Other Awesomes

- [awesome-generative-art](https://github.com/kosmos/awesome-generative-art)
- [awesome-creative-coding](https://github.com/terkelg/awesome-creative-coding)
