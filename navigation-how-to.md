# Pop Up Navigation Menu How To


### Links

-   [Start Here](./index.md)
-   [Evaluation Criteria](./evaluation-criteria.md)
-   [Quick Start](./quick-start.md)
-   [Design considerations](./design-considerations.md)
-   [Tips & Tricks](./tips-tricks.md)
-   [Typography Tips](./global-project-typography-tips.md)
-   [Navigation How To](./navigation-how-to.md)


## HTML

-   Add the following button code to your HTML.

-   Add it as the **first line at the top of the \<header\>** tag.

         <button class="hide-text" id="menu-button">menu</button>

-   Modify the main (top) menu unordered list by **adding an id of
    menu**:

          <ul class="main navigation" id="menu">

## CSS


### 1. Style the button tag to look like a hamburger icon 

First, either create a \"hamburger\" icon in Illustrator or download an
appropriate icon from [SVG Repo Hamburger
Icons](https://www.svgrepo.com/vectors/hamburger). Remember to optimize
the icon by dragging and dropping it onto the **ImageOptim** app.

        button#menu-button {
            height: 2rem;
            width: 2rem;
            display: block;
            border: none;
            background-image: url(bgimg/hamburger.svg); 
            background-repeat: no-repeat;
            background-size: cover;
        }



### 2. Hide the menu by default 

The menu should not appear automatically when the page loads. It should
only appear when the user taps the hamburger icon.

        #menu {
            display: none;
        }



### 3. Reveal & style the menu when the hamburger is tapped/clicked 

#### 3.1 The javascript adds a \"show-nav\" class to the #menu when the hamburger button is clicked. 

        #menu.show-nav {
            display: block;
        }  

#### 3.2. Style and position the menu 

We will move the hamburger to the top/right edge of the screen by using
absolute positioning. We will add a background color and border, and
move it to layer #100 (towards the reader, away from the background) to
make sure it is always above all the other items on the page.

You can adjust the position and appearance of the menu according to your
design\'s style.

        /* Add this code to the selector created in Step 3.1 above */
        
        #menu.show-nav {
            position: absolute;  /* position the menu */
            z-index: 100;
            top: 0;
            right: 0.6rem;
            
            background-color: rgb(255, 255, 237);  /* style the dropdown menu */
            padding: 1rem;
            width: 95%;
            margin: 0 auto;
            border: 1px solid #444;
        }  



### 4. Position the button to the top/right corner 

        #menu-button {
            position: absolute;
            right: 0.5rem;
            top: 0.5rem;
            padding: 0;
            background-color: transparent;
            z-index: 10;
        }



### 5. Add a custom cursor to the hover state 

Although this cursor would not be visible on a mobile device (because
there is \"hover\" state when using your finger on a touch screen) we
can still add a custom cursor for mouse users.

        #menu-button:hover {
            cursor: pointer;
            }



### 6. Hide the word \"menu\" in the button 

Because we want to use the menu button as an icon only, without text, we
will hide the text. However, we will keep it within the HTML so that
screen readers for the visually impaired still have the text to read.

The hide-text class works by indenting the text by 100%, so outside the
edges of the button, and hiding that overflowing text content (that is
effectively pushed beyond the edge of the box).

        .hide-text {
            text-indent: 100%;
            white-space: nowrap;
            overflow: hidden;
            padding: 0;
        }



### 7. Style the dropdown menu links 

#### 7.1 Adjust icon size 
        .icon a img {
            width: 2rem;
            height: auto;
        }

#### 7.2 Adjust height of the list item (link line) 

        li.icon {
            width: 100%;
            height: 1.8rem;
            margin: 1.3rem 0;  /* space apart for easier finger tapping */
          }

#### 7.3 Place the icon and text side-by-side with flexbox 

Although the anchor and span tags within the navigation are both inline
elements and will naturally go side-by-side, we will nonetheless use
display:flex (which puts them side-by-side) but will also let us control
their alignment within the flexbox.

        li.icon a {
            display: flex;  /* place logo and span side by side */
            justify-content: start; /* align left */
            align-items: center; /* vertically align */
            
            font-family: arial, helvetica, sans-serif; /* style span text as desired */
            font-weight: bold;
            text-decoration: none;  /* remove underline */
            font-size: 1.5rem;
            margin: 0; 
            height: 1.5rem;
        }



### 8. Hide button and display menu horizontally on desktop 

        @media only screen and (min-width: 64em) {
            button#menu-button {
                display: none;
            }

            #menu {
                display: flex;
            }
        }


