# DailyXKCD
A module for MagicMirror<sup>2</sup> that displays the daily XKCD web comic.

## Screenshot
![Example of DailyXKCD](screenshot.png?raw=true "Example screenshot")

## Dependencies
  * A [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror) installation

## Installation
  1. Clone this repo into your `modules` directory.
  2. Create an entry in your `config.js` file to tell this module where to display on screen.
  
 **Example:**
```
 {
    module: 'DailyXKCD',
	position: 'top_left',
	config: {
		invertColors: true,
		showTitle: true,
		showAltText: false
	}
 },
```

## Config
| **Option** | **Type** | **Default Value** | **Description** |
| --- | --- | --- | --- |
| `grayScale` | `bool` | `false` | Set to `true` to desaturate the colors of the comic to grayscale. |
| `invertColors` | `bool` | `false` | Set to `true` to invert the colors of the comic to white on black for a darker feel. |
| `updateInterval` | `int` | `3600000` | Set to desired update interval (in ms), default is `3600000` (10 hours). |
| `showTitle` | `bool` | `false` | Set to `true` to display the title of the comic. |
| `titleFont` | `string` | `large light bright` | Set a custom font format, default is `"large light bright"`. <br>To set the size use one of `xsmall small medium large xlarge`, <br>for boldness one of `thin light regular bold`, <br>and to adjust brightness one of `dimmed normal bright`. |
| `showAltText` | `bool` | `false` | Set to `true` to show the alt text (tooltip on the original comic). |
| `altTextFont` | `string` | `xsmall dimmed` | See `titleFont`, except for this is the formatting of the alt text. The default is `"xsmall dimmed"` |
| `randomComic` | `bool` | `false` | Set to `true`, if you want to see a random comic on days, when there is no new comic. |
| `alwaysRandom` | `bool` | `false` | Set to `true`, if you always want to see a random comic, even on days when there is a new comic. _Note: only effective if `randomComic` is set to `true`_ |
| `limitComicHeight` | `int` | `450` | Set to limit the height of the comic (in px), default is `450`. The comic will scroll downwards every few seconds, if it is heigher. |
| `limitComicWidth` | `int` | `0` | Set to limit the width of the comic (in px), default is `0`. The comic will scroll downwards every few seconds, if it is heigher. |
| `scrollInterval` | `int` | `8000` | How often to scroll long comics (in ms), default is `8000` (every 8 seconds). |
| `scrollRatio` | `float` | `0.8` | Set how much of the visible height is being scrolled every time. The value should be between `0.0` and `1.0`, default is `0.8` so it scrolls down by 80%. |
