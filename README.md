# lakansyèl for Stylus

![NPM version](http://img.shields.io/npm/v/stylus-lakansyel.svg) ![Build Status](http://img.shields.io/travis/leny/stylus-lakansyel.svg) ![Dependency Status](https://david-dm.org/leny/stylus-lakansyel.svg) ![Downloads counter](http://img.shields.io/npm/dm/stylus-lakansyel.svg)

> Color Scheme utilities for [Stylus](http://learnboost.github.io/stylus/)

* * *

# Hey, listen !

This plugin is deprecated. The `0.1.3` version will be the last.

Hey, don't cry ! All the incredible mixins of lakansyèl have been moved to [kouto-swiss](https://www.npmjs.org/package/kouto-swiss), a complete css framework for Stylus.

* * *

**lakansyèl for Stylus** is a collection of utilities to generate color schemes in your stylesheets.

## Installation

```
npm install stylus-lakansyel
```

## Usage

Include **lakansyèl** in your stylus stylesheets with

```css
@import "lakansyel"
```

### Utility functions

#### monochrome( color )

Returns monochromatic variations of the given color.  
`returned[0]`: first monochrome variation ( given color's lightness minus 33% )  
`returned[1]`: second monochrome variation ( given color's lightness minus 66% )

```css
variations = monochrome( #f00 )

.red-mono-one
    color variations[0]
    
.red-mono-two
    color variations[1]
```

#### analogous( color )

Returns analogous variations of the given color.  
`returned[0]`: first analogous variation ( spinning given color by 30 degrees )  
`returned[1]`: second analogous variation ( spinning given color by -30 degrees )

```css
variations = analogous( #f00 )

.red-analog-one
    color variations[0]
    
.red-analog-two
    color variations[1]
```

#### extended-analogous( color )

Returns more analogous variations of the given color.  
`returned[0]`: first analogous variation ( spinning given color by 30 degrees )  
`returned[1]`: second analogous variation ( spinning given color by -30 degrees )  
`returned[2]`: third analogous variation ( spinning given color by 60 degrees )  
`returned[3]`: fourth analogous variation ( spinning given color by -60 degrees )

```css
variations = extended-analogous( #f00 )

.red-analog-one
    color variations[0]
    
.red-analog-two
    color variations[1]
    
.red-analog-three
    color variations[2]
    
.red-analog-four
    color variations[3]
```

#### split-complements( color )

Returns split-complements variations of the given color.  
`returned[0]`: first split-complements variation ( spinning given color by 150 degrees )  
`returned[1]`: second split-complements variation ( spinning given color by -150 degrees )

```css
variations = split-complements( #f00 )

.red-split-complement-one
    color variations[0]
    
.red-split-complement-two
    color variations[1]
```

#### triad( color )

Returns triad variations of the given color.  
`returned[0]`: first triad variation ( spinning given color by 120 degrees )  
`returned[1]`: second triad variation ( spinning given color by -120 degrees )

```css
variations = triad( #f00 )

.red-triad-one
    color variations[0]
    
.red-triad-two
    color variations[1]
```

#### quad( color ) & tetrad( color )

Returns quad (*tetrad*) variations of the given color.  
`returned[0]`: first quad variation ( spinning given color by 90 degrees )  
`returned[1]`: second quad variation ( spinning given color by -90 degrees )  
`returned[2]`: third quad variation ( spinning given color by 180 degrees ) - complement color

```css
variations = quad( #f00 )

.red-quad-one
    color variations[0]
    
.red-quad-two
    color variations[1]
    
.red-quad-three
    color variations[2]
```

#### luminosity( color )

Returns the [WCAG luminosity](http://www.w3.org/TR/WCAG20/#relativeluminancedef) of the given color, as a `Number` between `0` (*black*) and `1` (*white*).

```
.luminosity
    background #ff0
    color luminosity( #ff0 ) > 0.5 ? black : white
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style.  
Add unit tests for any new or changed functionality.  
Test your code using `npm test`.

## Release History

**2014-01-07** : v0.0.1
**2014-01-28** : v0.1.0
**2014-05-14** : v0.1.3 + deprecation in favor of [kouto-swiss](https://www.npmjs.org/package/kouto-swiss)

## License 

(The MIT License)

Copyright (c) 2014 Pierre-Antoine "*Leny*" Delnatte

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
