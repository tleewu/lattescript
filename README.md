Lattescript
=======

A small library that converts the best functions of Coffescript to Javascript

## Installation

  `npm install lattescript`

## Usage

  ```
  // Sample code...
  var lattescript = require('lattescript');
  var nbaTeams = {
    lakers: ['kobe', 'magic', 'shaq'],
    bulls: ['mj', 'scottie', 'butler'],
    warriors: 'steph curry'
  };

  ```

  This library currently supports the much coveted "?" operator from coffeescript. For those
  who have only used Javascript, you would know that if you wanted to query a specific
  property in a deeply nested object and wanted to prevent an exception from breaking your code,
  you would have to do something along the lines of this:

  ```
  if (nbaTeams && nbaTeams.lakers && nbaTeams.lakers[0]) {
    // Insert code here.
  }
  ```

  In coffeescript, it's literally just this:

  ```
  if nbaTeams?.lakers?[0]
    # Insert code here.
  ```

  With lattescript, you can do this:

  ```
  if lattescript.valueOf(nbaTeams, "lakers", ...args) {
    // Insert code here.
  }
  ```

  ```
  console.log(lattescript.valueOf(nbaTeams, "lakers", 0) === "kobe")
  // true
  ```

## Tests

TODO:!!
