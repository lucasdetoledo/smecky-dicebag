# smecky-dicebag

Another simple dice roller.

### Installation
Install the library with `npm install smecky-dicebag`

### Usage
Dicebag's default behavior is to return the sum of a series of rolls. This behavior can
be modified by passing in an optional options_map.

#### roll(dice_type, number_of_dice, options_map)
let Dicebag = require('smecky-dicebag')

Dicebag.roll(4, 4) // => 16
Dicebag.roll(1, 1) // => 1
Dicebag.roll(100, 1) // => 98

#### d4(number_of_dice, options_map)
let Dicebag = require('smecky-dicebag')

Dicebag.d4(4) // => 16
Dicebag.d4(1) // => 2

#### d6, d8, d10, d12, d20
These have the same contract as Dicebag.d4

### options_map
options_map can be included in any Dicebag call. Currently, verbose is the only option
supported by Dicebag.

#### verbose - Returns the sum, and an array of roll values.
let Dicebag = require('smecky-dicebag')

Dicebag.roll(4, 4, { verbose: true }) // => { sum: 16, roll_log: [4, 4, 4, 4] }
Dicebag.d4(4, { verbose: true }) // => { sum: 10, roll_log: [2, 4, 1, 3] }