# OOP-Tutorial
**Util Lib of OOP**

# Object Definition.

* Material or abstract thing that can be perceived by the senses and described through its characteristics, behaviors and current **states**.

# What is Object?

## Example using a pen:

Attributes:
color, load, capped, weight

Methods:
draw, cover, uncover

State.

**EVERY OBJECT HAS ATTRIBUTE, METHODS AND STATE.**

Instantiate = Generate **object** from a **class**;

Class = "classification", planning of an object;

Class:
* Defines common **attributes** and methods that will be shared by an **object**.

Object:
* It is an **instance** of a **class**.

### Example:

```js
// Defining the Pen class
class Pen {
    constructor () {

        this.opened = false; // Pen state
        this.weight = 50;    // Pen weight (in grams)
        this.charge = 100;   // Pen charge amount
        this.color = 'Blue'; // Pen color

    }

    // Method to open the pen
    openPen () {
        if (!this.opened) {

            this.opened = true;

            console.log ('Pen Opened Successfully!');

            return true;
        }

        console.log ('Unable to open an already opened pen');

        return false;
    }

    // Method to close the pen
    closePen () {
        if (this.opened) {

            this.opened = false;

            console.log ('Pen Closed Successfully!');
            
            return true;
        }

        console.log ('Unable to close an already closed pen');

        return false;
    }

    // Method to draw with the pen
    drawPen () {
        if (this.opened) {
            if (this.charge !== 0) {

                console.log ('You drew with your pen!');

                return true;
            }

            console.log ('Unable to draw with an empty pen');

            return false;
        }

        console.log ('Unable to draw with a closed pen');

        return false;
    }
}

// Instantiation of the Pen class
const instance = new Pen ();
```
