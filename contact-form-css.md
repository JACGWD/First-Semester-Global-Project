# Basic CSS for the Contact Form

Understanding how to design the form is an excellent review of the basics of CSS, and will help you design the rest of the web site easily.

## 1. Make the Outer Fieldset Boxes Visible

As usual, making HTML elements visible on screen is key to making the design.

        fieldset {
            margin: 1rem;
            border: 1px solid #444;
        }

## 2. Use Display: Block for initial Page Layout

Make inline elements display as normal **block level elements** so that the form elements stack one on top of the other. This is the most important step in the page layout.

Notice the use of the **:not()**, because we don't want this rule to affect the buttons. We want to keep the buttons side-by-side.

        input:not(.button), textarea, select {
            display: block;
            margin: 0;
            }

## 3. Add Inner Whitespace

Padding will help align and inset both the inputs and labels, as well as the textarea.

        fieldset {
            margin: 1rem;
            border: 1px solid #444;
            padding: 1rem;
        }


## 4. Make the Input Fields Wider

Here we maximize the width of the text boxes so users have as much space as possible to enter text, especially on mobile.

        input:not(.button),
        textarea,
        select {
            display: block;
            margin: 0;
            width: 100%;
        }


## 5. Space Elements Apart with Margins

To help users better understand the form, we will make the label and inputs pairs stay close together and further away from the next pair.

We do this by pushing elements down from the bottom of the text field.

Note that we have to use a **more specific rule** than just saying "input", one that includes the extra info \[type="text"], because this input rule conflicts with the input:not(.button) rule. 

<blockquote>

### Important Note

The way that [CSS handles conflicts is called "Specificity"](https://www.w3schools.com/css/css_specificity.asp)

</blockquote>


       input[type="text"] {
            margin-bottom: 1rem;
        }


6. Make the Legend Easier to Read

Add a little space to the left and right of the legend text.

        legend {
            padding: 0 0.5rem;
        }

7. Add Extra Space below the Label

Note that the **label is an inline element** and we cannot give it margins until it becomes a block level element.

        label {
            margin-bottom: 0.35rem;
            display: block;
        }      


8. Align Buttons to the Right

Flexbox is the perfect tool for managing page layout **on a single line**. Here we use it to send the content of the .align-right class to the end of the block level element.

        .align-right {
            display: flex;

            justify-content: flex-end;
            /* Send buttons to the end of the flex box, ie right */

            margin-right: 1rem;
            /* match the width of the margin of the fieldset so it aligns */
        }        


9. Prevent the Two Buttons from Touching

Add margin-right to the reset button to make the buttons clearly stand out.

        .button[type="reset"] {
            margin-right: 1rem;
        }    

## Adding Creative Elements

Similar to what we did in the footer assignment, we can now add visual flair to our design by adding whitespace (margins and/or padding) to specific elements and **adding background images in that empty space**.

To Target a specific element when you have several of teh same type on the page (for eample a fieldset), give the one you want to target a class name.

        <fieldset class="comment-box">

Then add your background image to that selector:

        .comment-box {
            padding-top: 4rem;
            background-image: url(img/typing-01.svg);
            background-repeat: no-repeat;
            background-size: 4rem;
            background-position: 90% 1rem;
        }
