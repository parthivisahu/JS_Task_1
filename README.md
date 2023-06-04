# JS_Task_1
# JavaScript Date and Time Display

This JavaScript file provides functionality to display the current date and time in a web page. It utilizes the `Date` object and various methods to retrieve and format the date and time information.

## Usage

1. Include the JavaScript file in your HTML document using the `<script>` tag:

   ```html
   <script src="date-time.js"></script>
   ```

2. Create an HTML element with a specific `id` where you want the date and time to be displayed:

   ```html
   <div id="currentDateTime"></div>
   ```

3. In your JavaScript code or within a `<script>` tag, call the `displayDateTime` function passing the `id` of the HTML element as an argument:

   ```javascript
   displayDateTime("currentDateTime");
   ```

   This will update the content of the HTML element with the current date and time.

## Function Reference

### `displayDateTime(elementId)`

This function displays the current date and time in the specified HTML element identified by `elementId`.

- `elementId`: A string representing the `id` of the HTML element where the date and time should be displayed.

```javascript
displayDateTime("currentDateTime");
```

## Example

HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Date and Time Display Example</title>
    <script src="date-time.js"></script>
  </head>
  <body>
    <div id="currentDateTime"></div>

    <script>
      displayDateTime("currentDateTime");
    </script>
  </body>
</html>
```

JavaScript (date-time.js):

```javascript
function displayDateTime(elementId) {
  const element = document.getElementById(elementId);

  const currentDate = new Date();
  const formattedDate = currentDate.toDateString();
  const formattedTime = currentDate.toLocaleTimeString();

  element.textContent = `Current Date: ${formattedDate}\nCurrent Time: ${formattedTime}`;
}
```

When you open the HTML file in a web browser, the current date and time will be displayed in the specified HTML element:

```
Current Date: Fri Jan 01 2023
Current Time: 12:34:56 PM
```

Feel free to customize the formatting of the date and time according to your preferences by modifying the `formattedDate` and `formattedTime` variables in the `displayDateTime` function.
