APO-DZ-Form-Name-Formatter
==========================
**EDIT:** *Consider using [transformy](https://www.transformy.io/#/) if this isn't enough for you- it's a very cool, more general tool.*


Simple webapp to format copied spreadsheet columns to Dean's (@turniphead) Google Forms format. This is used for the backend of the [APO app](http://bit.ly/apo-dz).

The app maps (a newline-separated list of) inputs of the form  `Last Name\tFirst Name` to `Last Name; First Name` using `<form>` and the new HTML5 `<output>` [tag](http://www.w3schools.com/tags/tag_output.asp):

```html
<form oninput="formatted.innerHTML=names.value.split('\t').join('; ').split(/\r?\n/).join('<br/>')">
  <!-- Input -->
  <textarea cols="35" id="names" placeholder="Paste spreadsheet names here..." autofocus
  style="max-height:100px;min-height:100px;resize:none"></textarea>
  
  <!-- Output -->
  <output name="formatted" for="names"></output>
</form>
```

Check it out here: http://ronaldsmartin.github.io/APO-DZ-Form-Name-Formatter
