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
- [ ] Lesson 10
- [ ] Lesson 11
- [ ] Lesson 12
- [ ] Lesson 13
- [ ] Lesson 14
- [ ] Lesson 15
- [ ] Lesson 16
- [ ] Lesson 17
- [ ] Lesson 18
- [ ] Lesson 19
- [ ] Lesson 20
- [ ] Lesson 11
- [ ] Lesson 12
- [ ] Lesson 13
- [ ] Lesson 14
- [ ] Lesson 15

## Lesson 01

General intro. Nothing of note.

## Lesson 02

- **browser-sync**: neat tool to hot-reload html

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

- `repeast(#, 1fr 2fr)` repeat function

## Lesson 09

Property on Grid Items:

- `grid-column: span 5;` span multiple grid column slots
- `grid-row: span 2;` ditto for rows

## Lesson 10

