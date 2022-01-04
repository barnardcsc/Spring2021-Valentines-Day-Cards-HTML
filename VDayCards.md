# Workshop: Valentine’s Day Cards and Memes in HTML & CSS

### WORKSHOP DESCRIPTION : This workshop will introduce you to HTML and CSS in order to create two Valentine's Day cards.  One will be simple text with styling, and an animated svg element.  The other will include text over an image.  After the creation of the Valentine's Day Cards, we will go over embedding the cards into emails and hosting websites on Github.  You will leave this workshop having sent out a card or meme via email, and with the ability to apply your skills towards making more cards or towards designing web pages. In this workshop, we will use JSFiddle.  JSFiddle is an online IDE where you can see your HTML, CSS, JavaScript and rendering all in one screen.  

### What is HTML?
HTML is a markup language that describes how to structure the elements in a web document like text and images. 

### What is CSS?
CSS is what styles the HTML structure, bringing colors, more precise layouts, fonts, borders, etc...

## HTML Setup
This is the basic skeleton for starting an HTML page.  
 
#### HTML
```
<html>

    <head>
    </head>

    <body>
    </body>

</html>
```

* HTML is made of tags: ```< open_tag_type >  </close_tag_type> ``` You can have tags inside of tags, a bit like Russian Nesting Dolls. 
* Most of your HTML will go inside the body tags, while links, downloads, titles, etc. will go inside the head tag.

## Title the Page, and Create a heading
 * ```<title>``` is the tag that goes inside the ```<head>``` tag and titles a webpage when launched in a browser.
 * ```<h1>``` is the tag for a header.
 * ```<h2>```, ```<h3>```, ```<h4>```, ... are headers in smaller sizes.

#### HTML
```
<html>

    <head>
        <title> Valentine's Day Card </title>
    </head>

    <body>
        <h1> Happy Valentine's Day! </h1>
    </body>

</html>
```
### More Headers:
```
<html>

    <head>
        <title> Valentine's Day Card </title>
    </head>

    <body>
        <h1> Happy Valentine's Day! </h1>
        <h3> Roses are red, violets are blue, missing '}' on line 32. </h3>
    </body>

</html>
```

## Styling HTML: CSS
CSS is a language used for styling HTML.  The HTML tag needs to be identifyable, and then you can style it internallly in a style section in the head, externally in a CSS file that gets linked with the HTML in the head, or inline which is in the opening HTML tag. In jsfiddle, the linking is automatically done for you.  Just write the HTML in the HTML box, and the CSS in the CSS box...

#### CSS
You can style headers, and then h3 even though smaller, can be larger than h1.

```
h3{
  font-size: 7em;
  color: pink;
}

body{
  font-family: "Lucida Handwriting", cursive;
}

```
- style on tags applies to everything nested inside of it.  


other fonts: 
    * ```impact``` is the meme font
    * ```https://www.w3schools.com/css/css_font.asp ```

    * font-family: "Times New Roman", Times, serif;
    * font-family: "Lucida Console", "Courier New", monospace;
    * font-family: "Lucida Handwriting", cursive;
    * Brush Script MT, cursive


other colors:
    * red, purple, blue...
    * you can also use R,G,B, Hex, or HSL representions.
    * Here is a tool for colors: https://www.w3schools.com/colors/colors_picker.asp

### New lines/ line-breaks in Text
```<div> </div> ```
The div tag creates a line break after the closing tag. 

```
<html>
    <head>

        <title>classic card</title>
    </head>

    <body>


      <h1> Happy Valentine's Day! </h1>

      <div> Roses are red </div> 
      <div> violets are blue </div>
      <div> missing '}' on line 32! </div>

    </body>

</html>

```

### Multiple Stylings: Classes and ID's
- Let's put a closing.
```
<html>
    <head>

        <title>classic card</title>
    </head>

    <body>


      <h1> Happy Valentine's Day! </h1>

      <div> Roses are red </div> 
      <div> violets are blue </div>
      <div> missing '}' on line 32! </div>
      From your friend, Katie.

    </body>

</html>
```
#### What if you need space after the last div but not between all divs?

#### CSS
```
div{
  padding-bottom: 10px;
}
```
### Need Classes/ID's
- Classes for use many time, ID's only should be used once.  The only difference is writing class, or id, and refering to them with a . or a #. 

#### HTML
```
<div class = "pad"> missing '}' on line 32! </div>
      From your friend, Katie.
```
#### CSS
```
h3{
  font-size: 7em;
  color: pink;
}

body{
  font-family: "Lucida Handwriting", cursive;
}

.pad{
  padding-bottom: 40px;
}
```
### Styling One element in a div. <span> 

span elements allow us to give an id or class and style an element without a div/ making a new line. 

Let's change the words red and blue to their respective colors: 
- we do red with class and blue with id for demonstration purposes.

#### HTML
```
<div> Roses are <span class = "r"> red </span></div> 
<div> violets are <span id = "b"> blue </span></div>
```
#### CSS
```
.r{
  color: red;
}

#b{
  color: blue;
}
```

### More Styling:
- https://www.w3schools.com/colors/colors_picker.asp
```
body{
  font-family: "Lucida Handwriting", cursive;
  text-align: center;
  background: #ffcce6;
}
```
### Add SVG Animation

#### Add SVG Box ie. Canvas for your svg
#### Add this after From friend, Katie
- begins at the coordinates 0 0 (top left) and measures 100x100px

```
<svg width="100" height="100" viewBox="0 0 100 100">
   
</svg>
```
- Notice the from Katie text shifts. To protect from this, we use a container:
```
<html>
    <head>

        <title>classic card</title>
    </head>

    <body>

  <div class = "container">
      <h1> Happy Valentine's Day! </h1>

      <div> Roses are <span class = "r"> red </span></div> 
      <div> violets are <span id = "b"> blue </span></div>
      <div class = "pad"> missing '}' on line 32! </div>
      <span class = "pad">From your friend, Katie. </span>
  </div>
  
  <svg width="100" height="100" viewBox="0 0 100 100">
    
  </svg>


    </body>

</html>
```
- You can style the container to see that it's there. 
hint: (try svg)

### Path- draw the heart
```
<svg width="100" height="100" viewBox="0 0 100 100">
  <path fill="tomato" d="M92.71,7.27L92.71,7.27c-9.71-9.69-25.46-9.69-35.18,0L50,14.79l-7.54-7.52C32.75-2.42,17-2.42,7.29,7.27v0 c-9.71,9.69-9.71,25.41,0,35.1L50,85l42.71-42.63C102.43,32.68,102.43,16.96,92.71,7.27z"> </path>
  </svg>
```
### Animate the SVG
```
 <svg width="100" height="100" viewBox="0 0 100 100">
    <path fill="tomato" d="M92.71,7.27L92.71,7.27c-9.71-9.69-25.46-9.69-35.18,0L50,14.79l-7.54-7.52C32.75-2.42,17-2.42,7.29,7.27v0 c-9.71,9.69-9.71,25.41,0,35.1L50,85l42.71-42.63C102.43,32.68,102.43,16.96,92.71,7.27z"> </path>
  
    <animateTransform
      attributeName="transform"
      type="scale"
      dur="4s"
      values=".75; 1; 1.25; 1; .75"
      repeatCount="indefinite">
    </animateTransform>
  </svg>

  ```
- play with values for speed and size
- play with dur for speed
- change infinite to seconds: 5s etc. 

### More styling
We need padding under The from your friend text, or above the heart. 

```
svg{
  padding-top: 30px;
}
```
### Last syling gradient backgroung:
```
body{
  font-family: "Lucida Handwriting", cursive;
  text-align: center;
  /* background: #ffcce6;*/
  background-image: linear-gradient(to bottom right, white, pink); 
}
```

### Talk about emailing it, text works and svg didn't.  

### Embed into email

### Embedding into email
 * As much code as possible needs to have style inline. 
 * No body tags etc. needed anymore.
 * Some style can't be inline, will go to style tag section.
 * Not everything will render as expected in gmail.

1. With the styled text there.
2. Double click under the text in the compose window > Inspect.
3. In the div that is highlighted automatically:
4. Double click that div > Edit > HTML
5. before the closing div ```</div>```, paste the heart code:
```
<svg width="100" height="100" viewBox="0 0 100 100">
    <path fill="tomato" d="M92.71,7.27L92.71,7.27c-9.71-9.69-25.46-9.69-35.18,0L50,14.79l-7.54-7.52C32.75-2.42,17-2.42,7.29,7.27v0 c-9.71,9.69-9.71,25.41,0,35.1L50,85l42.71-42.63C102.43,32.68,102.43,16.96,92.71,7.27z"> </path>
  
    <animateTransform
      attributeName="transform"
      type="scale"
      dur="4s"
      values=".75; 1; 1.25; 1; .75"
      repeatCount="indefinite">
    </animateTransform>
  </svg>
```
6. Close the inspect window, see the heart but not animated -- inhibited by Google security.
10.  Send your card to yourself.
11. Open and inspect -- heart is missing. 

### Let publish to a website and link url 
### Publish Card as a website hosted by Github
- first, last styling: 
```padding-top: 100px;```
1. Login or make a Github account: https://github.com

2. Click New to make a new repository.

3. For the repository name, write ``` your_username.github.io ```
4. Leave as Public

5. Click Create Repository

6. Select the blue text, ``` creating a new file ```

7. In the input button next to your website name, write index.html

8. Paste your website HTML & CSS code into the file.

9. Click Commit new file in green. 

10. Select Settings

11. Scroll down to 'Github Pages'

12. Click None and then select main > Save.

13. Scroll back down to 'Github Pages' and click the blue url of your new published website.

**This created your 'user' github website.  If you want to make more websites you can create 'project' websites.  For this, you will need to use the same yourusername.github.io/a_repository_name_you_pic**

## Send yourself the link embedded in text as an email. 

# Card #2

### HTML
```
<html>
    <head>
    	<link rel="stylesheet" href="styles.css">
        <title>D3 Workshop</title>
    </head>

    <body>
    	<tr>
<td><div id = "container">
    	<h1> Happy Valentine's Day! </h1> 

      <img src="https://cdn.shopify.com/s/files/1/0150/0643/3380/products/SBSP-VD-HSGG_Viacom_SpongeBob_TriblendT-shirt_NL6010_Black_RO_600x.jpg?v=1579642479">
      

        <div class= "stud"> Hey STUD, </div> 
        <div class = "valentine"> Wanna be my Valentine?</div>


      
     </div>
 </td>
</tr>
    
    </body>

</html>
```
### CSS
```
#container{
  text-align: center;
  background: black;
  border-style: dotted;
  border-color: red;
  border-width: 40px;
  padding-bottom: 10px;
}
h1{
  font-size: 50px;
	color: pink;
  font-family: 'Brush Script MT', cursive;
  text-shadow:2px 2px 0 #B22222,
  -2px -2px 0 #B22222,
  2px -2px 0 #B22222,
  -2px 2px 0 #B22222,
  0px 2px 0 #B22222,
  2px 0px 0 #B22222,
  0px -2px 0 #B22222,
  -2px 0px 0 #B22222,
  2px 2px 5px #B22222;
}

img{
  width : 40%;
}



.stud{
  font-size: 40px;
  position: absolute;
  top: 19%;
  padding-left: 30%;
  color: white;
  font-family: impact;
  text-shadow:2px 2px 0 #B22222,
  -2px -2px 0 #B22222,
  2px -2px 0 #B22222,
  -2px 2px 0 #B22222,
  0px 2px 0 #B22222,
  2px 0px 0 #B22222,
  0px -2px 0 #B22222,
  -2px 0px 0 #B22222,
  2px 2px 5px #B22222;
}

.valentine{
  font-size: 40px;
  position: absolute;
  bottom: 7%;
  padding-left: 30%;
  color: white;
  font-family: impact;
  text-shadow:2px 2px 0 #B22222,
  -2px -2px 0 #B22222,
  2px -2px 0 #B22222,
  -2px 2px 0 #B22222,
  0px 2px 0 #B22222,
  2px 0px 0 #B22222,
  0px -2px 0 #B22222,
  -2px 0px 0 #B22222,
  2px 2px 5px #B22222;
}
```
### If problems come up:

```
add an extra container? 
.container {
    max-width: 60em;
  margin: 0 auto;
}

Then I set the image to have:

.responsive {
  width: 100%;
  height: auto;
}
```


### Add images
```<img src="url" alt="description of image for accessibility purposes">```
```
<html>
    <head>
    	<link rel="stylesheet" href="styles.css">
        <title>D3 Workshop</title>
    </head>

    <body>
    <div id = "container">
    	<h1> Happy Valentine's Day! </h1> 

      <img src="https://cdn.shopify.com/s/files/1/0150/0643/3380/products/SBSP-VD-HSGG_Viacom_SpongeBob_TriblendT-shirt_NL6010_Black_RO_600x.jpg?v=1579642479">
      

        <div class= "stud"> Hey STUD, </div> 
        <div class = "valentine"> Wanna be my Valentine?</div>

      
     </div>
    </body>

</html>
```
#### CSS
Styling the Image, Sizing and Position

#### CSS
Styling the Text Position

#### CSS
More Text Styling

### Styling the Background - Background Color and Border
* border styles ``` https://www.w3schools.com/css/tryit.asp?filename=trycss_border-style ```
### CSS


### Embedding into email
 * As much code as possible needs to have style inline. 
 * No body tags etc. needed anymore.
 * Some style can't be inline, will go to style tag section.
 * Not everything will render as expected in gmail.

1. Open an email in gmail.
2. Double click in the compose window > Inspect.
3. Find the div that contains ```content-editable = true ``` should be automatically highlighted. 
4. Double click that div > Edit > HTML
5. after the <br> and the closing div ```</div>```, paste this code:
```
<div style = "text-align: center;
  background: black;
  border-style: dotted;
  border-color: red;
  border-width: 40px;">
    	<h1 style ="font-size: 50px;
	color: pink;
  font-family: 'Brush Script MT', cursive;
  "> Happy Valentine's Day! </h1> 
  <div class="studtext" style = "font-size: 40px;
  color: white;
  font-family: impact;"> Hey STUD, </div> 

      <img style = "width : 40%;"src="https://cdn.shopify.com/s/files/1/0150/0643/3380/products/SBSP-VD-HSGG_Viacom_SpongeBob_TriblendT-shirt_NL6010_Black_RO_600x.jpg?v=1579642479">
      

        
        <div class = "studtext"style = "font-size: 40px;
  color: white;
  font-family: impact;"> Wanna be my Valentine?</div>

      
     </div>

```
6. Scroll up to ```<head>``` in the inspect code.
7. Double click ```<head>``` to expand, and find ```<style>``` tags. 
8.  Double click on the style tags to expand, and after the style tag, paste the following code, including the style tags.
#### Style Embedding
```
<style>

     h1{
   margin-top: 2%;
  text-align: center;
  font-size: 50px;
  color: pink;
  font-family: 'Brush Script MT', cursive;
  text-shadow:2px 2px 0 #B22222,
  -2px -2px 0 #B22222,
  2px -2px 0 #B22222,
  -2px 2px 0 #B22222,
  0px 2px 0 #B22222,
  2px 0px 0 #B22222,
  0px -2px 0 #B22222,
  -2px 0px 0 #B22222,
  2px 2px 5px #B22222;

}
.studtext{
    font-size: 40px;
  color: white;
    font-family: impact;
    text-shadow:2px 2px 0 #B22222,
    -2px -2px 0 #B22222,
    2px -2px 0 #B22222,
    -2px 2px 0 #B22222,
    0px 2px 0 #B22222,
    2px 0px 0 #B22222,
    0px -2px 0 #B22222,
    -2px 0px 0 #B22222,
    2px 2px 5px #B22222;
}
</style>
```
9. Close the inspect window, edit the contacts and add a message.  
10.  Send your card.
### Publish Card as a website hosted by Github

1. Login or make a Github account: https://github.com

2. Click New to make a new repository.

3. For the repository name, write ``` your_username.github.io ```
4. Leave as Public

5. Click Create Repository

6. Select the blue text, ``` creating a new file ```

7. In the input button next to your website name, write index.html

8. Paste your website HTML & CSS code into the file.

9. Click Commit new file in green. 

10. Select Settings

11. Scroll down to 'Github Pages'

12. Click None and then select main > Save.

13. Scroll back down to 'Github Pages' and click the blue url of your new published website.

**This created your 'user' github website.  If you want to make more websites you can create 'project' websites.  For this, you will need to use the same yourusername.github.io/a_repository_name_you_pic**

### Embed Link into Email

#### Make a button

```
 <input type="button" onclick="location.href='https://krb2162.github.io/krb2162.github.io-card-3/';" value="Click for a Valentine <3" />

 ```

 #### Style Button

 ```
  <input type="button" style ="background-color: pink; font-size: 30px;border-radius: 8px;font-family: 'Brush Script MT', cursive; border-style: outset; border-color: white; border-radius: 8px; border-width: 10px;"onclick="location.href='https://krb2162.github.io/krb2162.github.io-card-3/';" value="Click for a Valentine <3" />
  ```
### Issues with gmail

Gmail does not link to the website on click. 

But, we can get around this by using the embed link.

1. Embed the button in your email, following the same instructions for embedding the HTML from before. Inspect > Edit > Edit as HTML > Paste the input button code as the div.

2. Close the inspect window, and the button should be visible in the compose window of your email.

3. Click into the window next to your button, click the embed button.

4. For which text to embed, paste in the entire HTML with internal styling of the button. 

5. For the link, place the url from the button. 

6. Techinically, you could probably have just a button with no link and embed that then use the embedded gmail link.  However, it would not route to a url in anything other than gmail.  This way you learn how to do it for websites... etc. 



