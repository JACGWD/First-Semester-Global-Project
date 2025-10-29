# Global Project Typography


### Links

-   [Start Here](./index.md)
-   [Evaluation Criteria](./evaluation-criteria.md)
-   [Quick Start](./quick-start.md)
-   [Design considerations](./design-considerations.md)
-   [Tips & Tricks](./tips-tricks.md)
-   [Typography Tips](./global-project-typography-tips.md)
-   [Navigation How To](./navigation-how-to.md)



## 1. CSS Reset 

Please make sure to use the [CSS Reset from the JAC
GitHub](https://raw.githubusercontent.com/JACGWD/CSS-Reset-Selector/refs/heads/main/reset/simple-css-reset-v2.4.css)
repository.

The CSS Reset must be placed in the \<head\> **before** the link to the
actual stylesheet:

        <link rel="stylesheet" href="theme/default/css/reset.css" media="all">
        <link rel="stylesheet" href="theme/default/css/style.css" media="all">



## 2. Choose your Fonts 

-   Choose at least two fonts:

    1.  For titles and subtitles (h1, h2, h3, h4, h5, h6, label and
        legend tags)
    2.  Another font for default/body text

-   Refer to our previous exercises for how we integrated Google fonts
    into our projects.

    1.  Go to Google Fonts
    2.  Select a font by clicking the blue **Get Font** button at top
        right
    3.  Select another (you need two)
    4.  Click the little basket icon **View selected families** (above
        the Get Fonts button)
    5.  Click **Get Embed Code**

    ### Sample HTML Code

              <head>
              <link rel="preconnect" href="https://fonts.googleapis.com">
              <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
              <link href="https://fonts.googleapis.com/css2?family=Parkinsans:wght@300..800&display=swap" rel="stylesheet">

              <link rel="stylesheet" href="theme/default/css/reset.css" media="all">
              <link rel="stylesheet" href="theme/default/css/style.css" media="all">

    ### Sample CSS Code

              h1,
              h2,
              h3,
              h4,
              h5,
              h6,
              label,
              legend {
                  font-weight: bold;
                  font-family: 'Bebas Neue', 'Helvetica Neue', Helvetica, Arial, serif;
                  color: red;
              }


              body {
                  font-family: Montserrat, 'Gill Sans', Verdana, Tahoma, sans-serif;
                  line-height: 1.6; /* leading */
                  font-weight: normal;
                  color: black;   
              }



## 3. Use a Typographic Scale to Set Font Sizes 

With your choice of fonts active on the page, do these steps:

1.  Find the page with the longest h1 title. Ex: \"Contemporary
    Photography\". We need to define an H1 font size that is small
    enough that the words **do not get hyphenated**.

2.  Inspect the web page.

3.  In the web inspector, go into mobile preview.

4.  Set the mobile preview to 320px wide (if it is not already).

5.  Inspect a paragraph tag and adjust the font-size up until it looks
    nice (not too small nor too big). Ex: 1.1rem (this value will vary
    depending on your choice of font).

6.  Inspect the H1 tag and adjust the font-size up until the text is
    large enough to look like a title **yet does not hyphenate**. Ex:
    2.3rem (this value will vary depending on your choice of font).

7.  Go to [the typographic scale web
    site](https://spencermortensen.com/articles/typographic-scale/).
    (Also check out [Baseline Type Scale
    Generator](https://baseline.is/tools/type-scale-generator/))

8.  Scroll down to the \"classic typographic scale\" (or whichever you
    prefer).

9.  Set the n value to 6 (we want h1 to H6).

10. Set the r value to what number you found in Step 6.

11. Set the f~0~ value to what you found in Step 5.

12. Copy the CSS at the bottom of the \"classic typographic scale\" and
    paste it towards the top of your CSS stylesheet.

        /* Classic Typographic Scale */

        h1 { font-size: 2.53em; }  /* step 6 value */
        h2 { font-size: 2.1418em; }
        h3 { font-size: 1.8131em; }
        h4 { font-size: 1.5349em; }
        h5 { font-size: 1.2994em; }
        p { font-size: 1.1em; }  /* step 5 value */
        small { font-size: .9312em; }



## 4. Define margins for text 

The last step is defining **the amount of space before and after** each
type of text tag. We do this mostly with margin-top and margin-bottom.
Indents can be controlled with margin-left.

        h1 {
            margin: 2rem 0 0.5rem 0;  
            /* top, right, bottom, left */

            line-height: 1; 
            /* titles need less leading than paragraphs, experiment by adding decimal values like 1.25 or 1.11567 */
        }

        h2 {
            margin: 1.75rem 0 0.25rem 0;  
            /* Experiment with em vs rem to see the difference, choose your preferred appearance */
        }

        p {
            margin: 0 0 1rem 0;
            line-height: 1.6; 
            /* paragraphs need more leading than titles, experiment with decimal values between 1 and 2 */
        }



## 5. LoVeHA Rules 

Depending on the background colors of your header, top menu, main area
and footer, your link colors will need to be adjusted accordingly.

Each link has to have four states defined (otherwise you get the
browser\'s default color/appearance).

### Main menu LoVeHA

        #menu a:link {
            color: blue; 
            /* change to suit your design */

            text-decoration: none;  
            /* remove default underline */
        }

        #menu a:visited {
            color: gray;  

            /* less vivid color, must look "less interesting" than the a:link color 
                basically, this style must suggest "been there, seen that" */
        }

        #menu a:hover {
            text-decoration: underline; 
            /* add underline on hover to show it is a link */
        }

        #menu a:active {
            color: magenta; 
            /* only shows when clicking the mouse */
        }

### Main content LoVeHA

        main a:link {
            color: blue;
            text-decoration: none;
        }

        main a:visited {
            color: gray;
        }

        main a:hover {
            text-decoration: underline;
        }

        main a:active {
            color: magenta;
        }

### Footer menu LoVeHA

        footer a:link {
            color: blue;
            text-decoration: none;
        }

        footer a:visited {
            color: gray;
        }

        footer a:hover {
            text-decoration: underline;
        }

        footer a:active {
            color: magenta;
        }


