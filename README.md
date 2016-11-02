# Exam: HTML & CSS

### Getting Started
 - Fork this repository under your own account
 - Commit your progress frequently and with descriptive commit messages
 - All your answers and solutions should go in this repository

### What can I use?
 - You can use any resource online, but **please work individually**
 - Instead of copy-pasting your answers and solutions, write them in your own words.


# Tasks

## 1. Build a design (~90 minutes) [10 points]
Build the following profile cards according to the design provided.   
Follow the design as closely as possible.   
Commit an HTML and a CSS file to this repository.
![design](exercise-1.png)

### Assets
John Duck | Jane Duck | Pencil icon
--------- | --------- | -----------
![duck](duck.jpg) | ![duck](duck2.jpg) | ![pencil-icon](edit-icon.png)   

### Other data
  - Name font size: 28 pixels
  - Text size: 14 pixels
  - Font family: Arial, sans-serif

### Acceptance criteria
The task is accepted if:
  - The result follows design [2p]
  - The code follows style guide [1p]
  - The CSS & HTML are valid [1p]
  - The HTML considers semantic responsibilities [2p]
  - The code avoids code duplication [2p]
  - The CSS has meaningful and short selectors [2p]

Extra points for if:
  - the result is centered on the page [2p]


## 2. Understand code (~15 minutes) [2 points]
Read the following code snippet:   
What is the distance between the top-left corner of the document body and the yellow box?   
Give a detailed explanation below!   
Add your answer to this readme file, commit your changes to this repository.
```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        padding: 0px;
        margin: 0px;
      }
      .foo {
        top: 20px;
        left: 20px;
        width: 100px;
        height: 100px;
        position: absolute;
        background: blue;
      }
      .bar {
        top: 20px;
        left: 20px;
        width: 30px;
        height: 30px;
        position: absolute;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <div class="foo">
      <div class="bar"></div>
    </div>
  </body>
</html>
```
#### Your answer: [2p]
First the blue cube, so the basic principles about this is the position value, it is displayed: absolute (blue cube), an element that is positioned absolutely is taken out of the flow and thus takes up no space when placing other elements. The absolutely positioned element is positioned relative to nearest positioned ancestor (non-static). In this case that is the body, and it is positioned away from it top: 20px, and left 20px. 
So the yellow cube is inside within the "foo" so it is positioned absolutely to the foo, so it is positioned away from the blue cube's corner, if we turn off the top and left attribute that we can see it stick to the left corner. So the yellow one is away the foo left: 20px right: 20px.

## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: [2p]
- Normaly every html's basic display attribute is block, the standard block-level element. A block-level element starts on a new line and stretches out to the left and right as far as it can. If no width is set, will expand naturally to fill its parent container.
And what does the inline does? An inline element will accept margin and padding, but the element will still sit inline as you might expect. Margin and padding will only push other elements horizontally away, not vertically. The easiest way to picture an inline element is to think of it as a box that acts like text. What happens, for example, to text that’s not separated by other elements? It flows one letter after the other.

-inline-block: it is almost the same as inline, but it got a special power and what's that power you may ask? You can assign height and width to that element, and a simple inline element would ignore that, but not the special inline-block!!

### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: [2p]
article: An article is an independent, stand-alone piece of discrete content. Think of a blogpost, or a news item.
sectiom: on the other hand, isn’t “a self-contained composition in a document, page, application, or site and that is intended to be independently distributable or reusable”. It’s either a way of sectioning a page into different subject areas, or sectioning an article into … well, sections. For example I'm using sections since we've learned about it. It's better than div, cause' google's algorithms does not like divs anymore, it sees an empty element :)