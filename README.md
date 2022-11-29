![dactyl-manuform-micro-wiring](https://user-images.githubusercontent.com/61080/77671457-9efde780-6fc2-11ea-8700-d4a23125b4fe.jpg)
![dactyl-manuform-micro](https://user-images.githubusercontent.com/61080/77671473-a3c29b80-6fc2-11ea-8560-f24b60ecb28f.jpg)

# Dactyl ManuForm Micro Keyboard

This is a fork of the [Dactyl Manuform Mini Keyboard](https://github.com/l4u/dactyl-manuform-mini-keyboard). Checkout the Fork History for detail.

# Fork History (original -> latest)

- https://github.com/adereth/dactyl-keyboard
- https://github.com/jeffgran/ManuForm
- https://github.com/tshort/dactyl-keyboard
- https://github.com/lebastaq/dactyl-manuform-mini-keyboard
- https://github.com/l4u/dactyl-manuform-mini-keyboard

## Features

- Fully 3D-Printing cases, plates and wrist-rests.
- Reduce number of keys of thumb cluster to 3.
- Wrist-rest hookup mechanisim.
- TRRS/ProMicro are mounted on plate
- Use tapping screw,  no Heat-set insert is needed

## Generate OpenSCAD and STL models

* Run `lein generate` or `lein auto generate`
* This will regenerate the `things/*.scad` files
* Use OpenSCAD to open a `.scad` file.
* Make changes to design, `.scad` files will be regenerated automatically, and OpenSCAD will auto refresh if you used `lein auto generate`.
* When done, use OpenSCAD to export STL files, remember you need to render it first by press F6


## How to build

- Generate STL files or download from [thingiverse](https://www.thingiverse.com/thing:4242792/files)
- Print the right side with these files: `right.stl`, `plate.stl`, `wrist-rest.stl`, and mirror them for the left side
- Wire up switches by following this wonderful guide: https://github.com/abstracthat/dactyl-manuform . (Just skip those missing keys)
- Use (QMK Configurator)[https://config.qmk.fm/#/handwired/dactyl_manuform/5x6/LAYOUT_5x6] to build your firmware: Hit compile button and wait a sec then click on firmware to download
- Use (QMK Toolbox)[https://github.com/qmk/qmk_toolbox] on Windows or (QMK CLI)[https://github.com/qmk/qmk_cli] on Linux to flash your Pro-Micros (remember to short RST and GND pins to make them flashable)
- Hot glue USB jack onto the board for ProMicro, this is VERY IMPORTANT, I paid 2 pcs for this lesson. Then, Hot glue ProMicro and TRRS onto plate.


## How to remix

If you want to change number of rows, you can import `plate-reference.stl` to your favourite CAD software and make a new plate.

For the wrist-rest, use `wrist-rest-reference.stl` for cutting if your CAD software unable to convert the `right.stl` correctly.


## License

Copyright © 2015-2018 Matthew Adereth, Tom Short, Leo Lou and others

The source code for generating the models is distributed under the [GNU AFFERO GENERAL PUBLIC LICENSE Version 3](LICENSE).

The generated models are distributed under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](LICENSE-models).
