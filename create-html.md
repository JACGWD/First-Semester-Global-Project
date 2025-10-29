# Use This File & Folder Structure

Using the files and folders from the **enhanced template** [modified in the previous step](edit-navigation.md), duplicate the completed index.html file multiple times and rename the copies to respect the file names as written on the site map. 

-   index.html
-   contact.html
-   three other pages (minimum)
-   img (Content images, ie images that represent **content** not
    style/decoration. For example, a picture of the company owner is
    content. It will not change if the style of the site is redesigned.
    A texture image is used for decorative purposes (as a background
    image by the css), and belongs in the img folder within the theme
    folder.)
-   theme
    -   css
    -   bgimg (only decorative images referred to by the css)
    -   js

## Sample file hierarachy (for a restaurant site)

    ├── contact.html <-- this page is required
    ├── css
    │   ├── bgimg
    │       └── hamburger.svg
    │   ├── reset.css
    │   └── style.css
    ├── img
    │   └── logo.png
    ├── index.html  <---- this is the home page
    ├── locations.html    <---- name the other pages according to what makes sense for your project's subject
    ├── menu.html  <------------|
    └── reservations.html <-----|