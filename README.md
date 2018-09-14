# MicroPython touch:bit library for the BBC micro:bit

Open touchbit.py in Mu editor and flash it to your micro:bit to run the example code.

Due to code constaints on the micro:bit this library serves as a simple demonstration for getting touch input up and running. The Cap1166 has dozens of possibly useful features relating to input sensing and LED control that you can find documented in the datasheet - http://ww1.microchip.com/downloads/en/DeviceDoc/00001621B.pdf

# Installing

Copy the touchbit.py file from library/touchbit.py into your "mu_code" folder, this might be in:

* C:\Users\YourUserName\mu_code on Windows
* /Users/YourUserName/mu_code on macOS

Create a new blank file in Mu for your project, leave it blank and Flash it to your micro:bit with the Flash button. You can close this for now.

Create another new file, save this one as "main.py" and keep it open.

Now open the "Files" dialog (you might have to close the "Repl" first) and drag and drop main.py and touchbit.py from the right pane, to the left pane.

When you reset your micro:bit, it will load main.py- so you can "import touchbit" and start writing your code here!

# Function Reference

## Initialise The Library

```setup()```

Call this once to load the default settings-  linked LED with multi-touch support, release interrupts and 16x sensitivity.

## Set an LED

```set_led(index, state)```

Turn an LED on `set_led(0, 1)` or off `set_led(0, 0)`.

The pads on touch:bit are numbered 0 to 5 from left to right.

## Read button events

```wait_for_change(timeout=500)```

Wait `timeout` milliseconds for an interrupt event and return a dictionary of button indexes and states indicating the current pressed/released buttons.

