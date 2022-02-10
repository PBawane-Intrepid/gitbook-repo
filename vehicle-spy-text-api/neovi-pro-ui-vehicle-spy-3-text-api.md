# neoVI PRO UI - Vehicle Spy 3 Text API

**Objective**

The neoVI PRO user interface is accessed using the UI object. The syntax is as follows:

ui.clear ; clears the screen

**neoVI PRO Display**

The neoVI PRO has a 128 wide by 64 pixel high monochrome display. UI commands support x coordinates between 0 and 127 and y coordinates between 0 and 63. The UI commands supports two colors: blue (1) and white (0). Colors can be inverted using the invert command (useful in different lighting environments).

**UI Object**

| Command Name  | Description                                                                                                                                                                                                                                                                                                                      | Example                                                                      |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| ledpwr        | Sets/Clears the neoVI PRO power LED                                                                                                                                                                                                                                                                                              | ui.ledpwr 1 ;// sets the led on ui.ledpwr 0 ;// turns led off                |
| clear         | Clears the LCD screen                                                                                                                                                                                                                                                                                                            | ui.clear ;// clears the LCD screen                                           |
| line          | Draws a line on the LCD screen in a specified color Arguments: x1,y1,x2,y2,color                                                                                                                                                                                                                                                 | ui.line 0,32,127,32,1 ;// draw a line in the center of the screen            |
| print         | <p>Prints Text on the LCD screen in a specified color, size and horizontal alignment. Arguments: x1,y1,fontsize,alignment, color,{text} Font Size: 0) normal letters (5x8), 1) small letters (Xx5), 2) large (10x16)</p><p>Alignment: 0) no alignment 1) left, 2) center, 3) right. x is ignored for alignments 1 through 3.</p> | ui.print 0,28,0,2,1,Hello neoVI World ;// displays hello world on the screen |
| rect          | Draws a rectangle on the LCD screen with optional fill Arguments: x1,y1,x2,y2,color,fill                                                                                                                                                                                                                                         | ui.rect 10,10,30,30,1,0 ;// draw a square on the screen                      |
| ledex         | Sets/Clears the neoVI PRO exclaim (!) LED                                                                                                                                                                                                                                                                                        | ui.ledex 1 ;// sets the led on ui.ledex 0 ;// turns led off                  |
| leddb         | Sets/Clears the neoVI PRO database LED                                                                                                                                                                                                                                                                                           | ui.leddb 1 ;// sets the led on ui.leddb 0 ;// turns led off                  |
| buzz          | Sets/Clears the neoVI PRO buzzer                                                                                                                                                                                                                                                                                                 | ui.buzz 1 ;// turns on buzzer ui.buzz 0 ;// turns off buzzer                 |
| keys          | Returns the key pad state in a bitfield: 1) Up 2) Down 4) Left 8) Right 16) check 32) X 64) O 128) Square 256) Star                                                                                                                                                                                                              | ui.keys? ok keys 1 ;// the up buttons is currently pressed                   |
| keycheck      | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  | ui.keycheck? ok keycheck 0                                                   |
| keyleft       | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| keyright      | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| keyup         | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| backlight     | Sets/Clears the neoVI PRO backlight                                                                                                                                                                                                                                                                                              | ui.backlight 1 ;// turns on backlight ui.backlight 0 ;// turns off backlight |
| invert        | Allows you to invert the colors on the display.                                                                                                                                                                                                                                                                                  | ui.invert 1 ;// invert on ui.invert 0 ;// invert off                         |
| dbitmap       | Draws a bitmap x1,y1,widthinpixels,heightinpixels,{csv hex bitmap}                                                                                                                                                                                                                                                               | ui.dbitmap 0,0,4,8,FF,FF,FF,FF ;// draws a block of pixels                   |
| keydown       | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| keyo          | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| keystar       | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| keybox        | Returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| Circle        | Draws a circle on the display Arguments: x,y,radius, color                                                                                                                                                                                                                                                                       | ui.circle 30,30,5,1                                                          |
| Pixel         | Draws a pixel on the display Arguments: x,y,color                                                                                                                                                                                                                                                                                | ui.pixel 30,30,1 ;// set pixel to blue                                       |
| operatingmode | <p>Gets/Sets the operating mode of the display and neoVI PRO:</p><ol><li>Bus Decoder Normal</li><li>Bus Decoder J1979</li><li>Vehicle Spy Mini Mode</li><li>Custom</li><li>Diag Tool</li><li>Test and Debug</li></ol>                                                                                                            | ui.operatingmode 3 ;// switch to custom mode                                 |
| keyx          | returns and clears the keypress latch This will return 1 if the enter key has been pressed since last time the key was checked.                                                                                                                                                                                                  |                                                                              |
| setpendant    | This enables the neoVI PRO pendant                                                                                                                                                                                                                                                                                               |                                                                              |
| pred          | Sets the intesity of the RED led on the neoVI PRO pendant                                                                                                                                                                                                                                                                        |                                                                              |
| pblue         | Sets the intensity of the Blue LED on the neoVI PRO pendant                                                                                                                                                                                                                                                                      |                                                                              |
| pgreen        | Sets the intensity of the Green LED on the neoVI PRO pendant                                                                                                                                                                                                                                                                     |                                                                              |
| button        | Reads the button on the pendant                                                                                                                                                                                                                                                                                                  | ui.button?                                                                   |