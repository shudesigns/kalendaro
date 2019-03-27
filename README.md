# kalendaro.js
A simple, easily-customized jQuery plugin to create calendars.

## Installation
### Set Up
Add the links to the CSS files in your `<head> `
```html
<link rel="stylesheet" type="text/css" href="kaledanro.css" />
<!-- if you want to use the default theme -->
<link rel="stylesheet" type="text/css" href="kaledanro.theme.css" />
```
And then add the js file after jQuery before `</body>`
```html
<script type="text/javascript" src="kalendaro.js"></script>
```

## Usage
### Basic Usage
To render the calendars, your element can just be as easy as this:
```html
<div id="myCalendar"></div>
```
Then call your jQuery plugin:
```javascript
$('#myCalendar').kalendaro();
```
### Rendering Events
To add events to your calendar, you can simply add them like this:
```html
<div id="myCalendar">
  <div event-date="0101" event-type="holiday">Happy New Year!</div>
  <div event-date="0418" event-type="important">Project due</div>
  <div event-date="1025" event-type="birthday">My birthday</div>
</div>
```
Please note that the format for `event-date` must be `mmdd`. You can define each event type in your options.

## Options
| Name            | Type    | Default   | Description |
| --------------- | ------- | --------- | ----------- |
| calendarClass   | string  | null      | Custom class for calendars if you need. For example: `'.custom-calendar'` |
| nav             | boolean | true      | Enable months navbar |
| navClass        | string  | null      | Custom class for navbar if you need. For example: `'.custom-nav'` |
| navPosition     | string  | 'top'     | The position for your navbar. You can go with `'top'`, `'left'`, `'right'`, or `'bottom'`|
| stickyNav       | boolean | true      | Enable sticky navbar |
| scrollSpeed     | number  | 800       | The transition speed for scrolling to targeted month |
| scrollEasing    | string  | 'swing'   | animate() fallback easing |
| slider          | boolean | false     | Displaying calendars in slider style |
| year            | string  |           | The year for your calendars. Default setting is the current year. For example: `'2019'` |
| firstDayOfWeek  | number  | 0         | The first day of the week for your calendar. `0` equals to Sunday, `1` equals to Monday, etc. |
| monthNames      | array   | `[ "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December" ]`| The list of full month names |
| monthNamesShort | array   | `[ "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec" ]` | The list of abbreviated month names |
| dayNames        | array   | `[ "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday" ]` | The list of long day names, starting from Sunday |
| dayNamesShort   | array   | `[ "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" ]` | The list of abbreviated day names, starting from Sunday |
| dayNamesMin     | array   | `[ "Su","Mo","Tu","We","Th","Fr","Sa" ]` | The list of minimised day names, starting from Sunday |
| disableMonths   | array   | null      | Disable certain month(s) if you wish. For example: `[1, 10]` (hide January and October) |
| events          | array   | null      | Configure your calendar events settings. See examples below. |
