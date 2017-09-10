#HTML (HyperText Makeup Language)

## not a programming language, but define the contents of webpage

## basic structure
```html
<!DOCTYPE html>
<html>
<head>
  <title>My fist web page</title>
</head>
<body>
  <p> Hello World!</p>
</body>
</html>
```

## view source code of web
- Chrome: Option-Command-U
- Firefox: Command-U

## HTML is composed of Tags
- 1. content element: <tagname> Contents </tagname>
- 2. void element: <tagname />
- both elements can have attributes to further define functionality

```html
<contenttag attribute="value"> Content </contenttag>
<emptytag attribute="value" />
```

## Commonly Used Tags
1. semantic elements:
header, footer, nav, article, section, figure, figcaption, form,

2. external media:
* <iframe src="source"> Represents a little window on your page into which source is loaded; source could be a PDF document, for example, or an entire other web page
* <link rel="what" type="mime" href="source" /> Defines an external document what located at source with the mime type mime that should be loaded into your HTML page. Note: <link /> does NOT define a hyperlink! <a> is for that. Used most commonly for including CSS stylesheets.
* <img src="source" alt="text" /> Defines an image located at source that has a textual representation of text
* audio, video, canvas

3. outline elements
* <h1> to <h6> Defines the outline for your page
* <p> Defines a paragraph of text
* <dl> Defines a Dictionary List
* <ol> and <ul> Define ordered and unordered lists, <li> defines either
* <table> Defines a table for displaying data
* <q> or <blockquote> represent quote

4. miscellaneous elements
* <a href="destination"> a hyperlink to destination
* <br/> line break
* <button> <code>
* <output> result of calculation
* <pre> pre-formatted text with whitespace preserved
* <script>
* <div> block section, <span> inline section, both for styling,

## Quick and easy layout
```html
<!DOCTYPE html>
<head>
<meta charset="utf-8"/>
<title>My Web Page</title>
<style type="text/css">
body{
	width: 760px; /* how wide to make your web page */
	background-color: teal; /* what color to make the background */
	margin: 0 auto;
	padding: 0;
	font:12px/16px Verdana, sans-serif; /* default font */
}
div#main{
	background-color: #FFF;
	margin: 0;
	padding: 10px;
}
</style>
</head>
<body><div id="main">

<!-- CONTENT HERE -->

</div></body>
</html>
```

## The HTML5 Shiv (for old explorer)
put this in <head> tag
```html
<!--[if lt IE 9]>
<script src="https://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
<![endif]-->
```

## [ALWAYS validate code!](https://validator.w3.org/)

## form
1. *input* type
```html
<form action="/action_page.php">
  First name:<br>
  <input type="text" name="firstname" value="Mickey"><br>
  Last name:<br>
  <input type="text" name="lastname" value="Mouse"><br><br>
  <input type="submit" value="Submit">
</form>
```

2. *Action* attribute
3. *Method* attributes : get and post
- when *GET* is used, the submitted form data will be visible in the page address field.
 GET is best suited for short, non-sensitive, amounts of data, because it has size limitations too.
- Always use *POST* if the form data contains sensitive or personal information. The POST method does not display the submitted form data in the page address field. No size limitations
4. *name* attribute
If the name attribute is omitted, the data of that input field will not be sent at all.
5. grouping form data with <fieldset>
```html
<form action="/action_page.php">
  <fieldset>
    <legend>Personal information:</legend>
    First name:<br>
    <input type="text" name="firstname" value="Mickey"><br>
    Last name:<br>
    <input type="text" name="lastname" value="Mouse"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form>
```html
