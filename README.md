# CSS Tutorial

## Part 0: HTML Refresher
1. HTML files are written in a `.html` file.
2. `<elementname></element>` is the syntax of defining an HTML element. Some are written like `<elementname />` if there is no body.
3. You can assign an attribute to an element. e.g. `<div id="example"></div>` is a division element with an attribute called id with a value of 'example'.
4. Elements and attributes are kebab-case `this-is-kebab-case` or underscore-case `this_is_underscore_case` (pick one).

**Resource:** HTML Element Tags [https://www.w3schools.com/tags/default.asp](https://www.w3schools.com/tags/default.asp), Style guide [https://www.w3schools.com/html/html5_syntax.asp](https://www.w3schools.com/html/html5_syntax.asp)

## Part 1: Setting up an Stylesheet
Although you can write all of your styles inline or within a `style` element in your `.html` file, this isn't recommended because it encourages writing your entire website in one file, which ends up turning your website into *al-dente* spaghetti code. 

1. To start, create a directory called `tutorial` and within the directory, create 2 files `index.html` and `style.css`.

`index.html`
```html
<!doctype html>
<head>
  <meta charset="UTF-8">
  <link href="style.css" rel="stylesheet" type="text/css">
</head>
<body>
</body>
```

`style.css`
```css
body {
  background-color: #ff00ff;
}
```

2. Next, navigate to the `index.html` file in your computer's file explorer and open the file up in your browser. If you see a pink website show up, then your CSS file successfully linked up!


## Part 2: CSS Selectors
[https://www.w3schools.com/cssref/css_selectors.asp](https://www.w3schools.com/cssref/css_selectors.asp) is a good resource for CSS selectors. This list might be overwhelming at first, but only about half the list is commonly used, and rather intuitive once you get used to them.

The format of a basic CSS block is as followed:
```css
selector_goes_here {
  property-1: value;
  property-2: value;
  ...
  property-n: value;
}
```

The following are the most commonly used selectors:
* Element Selector `elementname`
* Class Selector `.classname`
* ID Attribute Selector `#idname` (note: try to avoid styling elements on a page using the ID attribute)
* Attribute Selector `[attribute=value]`
* Pseudo Classes `:pseudo_classes`
* Pseudo Elements `::pseudo_elements`

You can extend or narrow the reach of the properties of a block by combining a few selectors together. Here are some notable examples:
### `element#id.classname[name=value]:pseudo-classes::pseudo-elements`
You can narrow down your selector by combining them in the order of:
1. Element
2. ID
3. Class
4. Attribute
5. Pseudo Classes
6. Pseudo Elements

Of course, you don't need to have all of selectors, so you can do selectors like `input[type=text]` or `h1.bold:hover`.

### `selector, selector, ..., selector`
The comma operator allows you to select and apply styling to multiple selectors.

### Pseudo Classes
Pseudo classes are used to style a *"special state"*, usually something with user interaction but aren't limited to it. e.g. `:hover` will style an element that is currently being hovered over by the user, `:nth-child(n)` selects every nth element, etc.

[https://www.w3schools.com/css/css_pseudo_classes.asp](https://www.w3schools.com/css/css_pseudo_classes.asp)

### Pseudo Elements
Pseudo elements are used to style a specific part of the element. e.g. `::first-letter` selects the first letter of the element body, `::after` allows you to insert some content after the selected element. 

[https://www.w3schools.com/css/css_pseudo_elements.asp](https://www.w3schools.com/css/css_pseudo_elements.asp)

## Part 3: Media Queries
Media queries are used to change styling of the website based on the additional properties and parameters you define.
```css
@media only screen and (max-width: 500px) {
    body {
        background-color: #00ff00;
    }
}
```

[https://www.w3schools.com/css/css_rwd_mediaqueries.asp](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)

## Part 4: Centering Elements
Centering elements are different for several cases, depending on if you want to vertically or horizontally center elements, and what display property the element has.

[http://howtocenterincss.com/](http://howtocenterincss.com/)

## Part 5: Libraries to Consider in your Project
* `normalize.css` [https://necolas.github.io/normalize.css/](https://necolas.github.io/normalize.css/)
* `skeleton.css` [http://getskeleton.com/](http://getskeleton.com/)
* `animate.css` [https://daneden.github.io/animate.css/](https://daneden.github.io/animate.css/)
