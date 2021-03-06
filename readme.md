# Notes on CSS Grid Fundamentals

Notes on [CSS Grid Fundamentals](https://cssgrid.io/) by Wes Bos

## Table of Contents

<!-- TOC -->

- [Notes on CSS Grid Fundamentals](#notes-on-css-grid-fundamentals)
  - [Table of Contents](#table-of-contents)
  - [Progress](#progress)
  - [Lesson 01](#lesson-01)
  - [Lesson 02](#lesson-02)
  - [Lesson 03](#lesson-03)
  - [Lesson 04](#lesson-04)
  - [Lesson 05](#lesson-05)
  - [Lesson 06](#lesson-06)
  - [Lesson 07](#lesson-07)
  - [Lesson 08](#lesson-08)
  - [Lesson 09](#lesson-09)
  - [Lesson 10](#lesson-10)
  - [Lesson 11: Exercise](#lesson-11-exercise)
  - [Lesson 12](#lesson-12)
  - [Lesson 13](#lesson-13)
  - [Lesson 14](#lesson-14)
  - [Lesson 15](#lesson-15)
  - [Lesson 16](#lesson-16)
  - [Lesson 17](#lesson-17)
  - [Lesson 18](#lesson-18)
  - [Lesson 19: Exercise](#lesson-19-exercise)
  - [Lesson 20: Exercise](#lesson-20-exercise)
  - [Lesson 21: Flexbox vs CSS Grid](#lesson-21-flexbox-vs-css-grid)
  - [Lesson 22: Exercise](#lesson-22-exercise)
  - [Lesson 23: Exercise](#lesson-23-exercise)
  - [Lesson 24: Exercise](#lesson-24-exercise)
  - [Lesson 25: Exercise](#lesson-25-exercise)

<!-- /TOC -->

## Progress

- [X] ~~*Lesson 01*~~ [2018-06-13]
- [X] ~~*Lesson 02*~~ [2018-06-13]
- [X] ~~*Lesson 03*~~ [2018-06-13]
- [X] ~~*Lesson 04*~~ [2018-06-13]
- [X] ~~*Lesson 05*~~ [2018-06-13]
- [X] ~~*Lesson 06*~~ [2018-06-14]
- [X] ~~*Lesson 07*~~ [2018-06-14]
- [X] ~~*Lesson 08*~~ [2018-06-14]
- [X] ~~*Lesson 09*~~ [2018-06-14]
- [X] ~~*Lesson 10*~~ [2018-06-14]
- [X] ~~*Lesson 11*~~ [2018-06-14]
- [X] ~~*Lesson 12*~~ [2018-06-14]
- [X] ~~*Lesson 13*~~ [2018-06-14]
- [X] ~~*Lesson 14*~~ [2018-06-14]
- [X] ~~*Lesson 15*~~ [2018-06-14]
- [X] ~~*Lesson 16*~~ [2018-06-14]
- [X] ~~*Lesson 17*~~ [2018-06-14]
- [X] ~~*Lesson 18*~~ [2018-06-14]
- [X] ~~*Lesson 19*~~ [2018-06-14]
- [X] ~~*Lesson 20*~~ [2018-06-14]
- [ ] Lesson 21
- [ ] Lesson 22
- [ ] Lesson 22
- [ ] Lesson 23
- [ ] Lesson 24
- [ ] Lesson 25

## Lesson 01

General intro. Nothing of note.

## Lesson 02

- **browser-sync**: neat tool to hot-reload html

- `"browser-sync start --server --files '**/*.css, **/*.html, **/*.js, !node_modules/**/*' --directory --port 7777 --browser 'Firefox Developer Edition'"`

## Lesson 03

- `.item{$}*10`: sweet emmet trick to generate 10 numbered divs with class item
- `display: grid` creates a grid container
- `grid-template-columns` defines column dimensions
- `grid-template-row` defines row dimension
- `grid-gap` determines gap dimensions
- dimesions can be `px percents auto rem em`
- undefined grid items (rows or columns) auto-size
- `repeat(#,dimension)` repeat logic

## Lesson 04

- Wes goes over tips on how to use Firefox Grid Dev Tool
- Implicit vs. Implied Tracks
- Solids lines indicate container bounding lines

## Lesson 05

- `grid-auto-rows: 100px 500px;` determines height of implicit rows
- `grid-auto-columns: 30%;` determines width of implicit columns

## Lesson 06

- `grid-auto-flow: [column/row/dense]` similar to flex-flow to change main axis

## Lesson 07

- _fractional unit_ `fr` unit, proportion of 'free space'

## Lesson 08

- `repeat(#, 1fr 2fr)` repeat function

## Lesson 09

Property on Grid Items:

- `grid-column: span 5 / 2;` span multiple grid column slots
- `grid-row: 3 / span 2;` ditto for rows

## Lesson 10

- `grid-column: 1 / -1` 100% width of container

## Lesson 11: Exercise

- [Spacing & Placing Cardio Exercise](https://jsfiddle.net/cesarnml/prbex23c/)
- Good practice. Easy

## Lesson 12

- `auto-fit:` similar but new grid fits contained items
- `auto-fill:` used to auto-fill columns/rows to container capacity (e.g `repeat(auto-fill,100px))

## Lesson 13

- `minmax(min-size, max-size)`: smart sizing of grid-items
- `fit-content(max-size)`: edge-case solution

## Lesson 14

- `.` unnamed area

```css
grid-template-areas:
    "sidebar1 content sidebar2"
    "sidebar1 content sidebar2"
    "footer   footer  ."
```

## Lesson 15

- Naming grid lines:

```css
grid-template-columns: [name1 name2] 1fr [name3]
```

## Lesson 16

- `grid-auto-flow: dense`
- `item:nth-child(6n)` neat trick

## Lesson 17

- `justify-items`: [stretch], start, end, center
- `align-items`: [stretch], start, end, center
- `place-items`: short-hand for above
- `justify-content`: aligns grid within container (left-right)
- `align-content`: [start], end, center, stretch, space-around, space-between, space-evenly
- `place-content`: shorthand for above two
- `justify-self`: item specific changes, row
- `align-self`: item specific changes, column

## Lesson 18

- `order: [0]`: default is 0

## Lesson 19: Exercise

[Album Cover Layout Exercise](https://jsfiddle.net/cesarnml/res69thd/)

```css
    .albums {
      display: grid;
      grid-gap: 20px;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    }

    .album {
      display: grid;
      background: rgba(244, 244, 244, .3);
      box-shadow: 0 0 5px rgba(0, 0, 0 .2);
      grid-gap: 10px;
      grid-template-columns: 150px 1fr;
      align-items: center;
      padding: 20px;
      color: white;
      font-weight: 100;
    }

    .album__artwork {
      width: 100%
    }
```

## Lesson 20: Exercise

- [CSS Grid Image Gallery](https://jsfiddle.net/cesarnml/tgbdrz2k/)

- `Array.from({length: 50}, [cb, cb])` create an array from object with length property = number of arrays created; call back can used to define each array entry

```javascript
// Wes Bos JS-fu
    function generateHTML ([h, v]) {
      return `
      <div class="item h${h} v${v}">
        <img src="./images/${randomNumber(12)}.jpg">
        <div class="item__overlay">
          <button>View ➡</button>
        </div>
      </div>
      `
    }

    function randomNumber (limit) {
      return Math.floor(Math.random() * limit) + 1
    }

    const digits = Array.from({
      length: 50
    }, () => {
      return [randomNumber(4), randomNumber(4)]
    })

    const html = digits.map(generateHTML).join('')
    gallery.innerHTML = html
```

## Lesson 21: Flexbox vs CSS Grid

## Lesson 22: Exercise

- [Recreating Codepend Exercise](https://jsfiddle.net/cesarnml/p2t90v6m/)

## Lesson 23: Exercise

- [Bootstrappy Grid and CSS Variables Exercise](https://jsfiddle.net/cesarnml/p4tru59f/)

## Lesson 24: Exercise

- [Responsive Website Layout](https://jsfiddle.net/cesarnml/kg8smzp1/)

## Lesson 25: Exercise

- [Full Bleed Blog Layout](https://jsfiddle.net/cesarnml/85pxa1jv/)
