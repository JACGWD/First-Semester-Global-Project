# Edit the default navigation


## Edit the navigation

### Unedited Nav Code

In index.html, find this section of code:

        <nav class="primary-navigation">
            <button class="hide-text">Menu</button>

            <ul id="menu">
                <li><a href="#">Home</a></li>
                <li><a href="#">Page 1</a></li>
                <li><a href="#">Page 2</a></li>
            </ul>
        </nav>

Duplicate the last two lines, and modify like this. Please replace the "subtopic-X.html" and "name of subtopic" with the proper names from your site map:

### Customized Nav Code

            <nav class="primary-navigation">
                <button class="hide-text">Menu</button>
                <ul id="menu">
                    <li><a href="index.html">Home</a></li>
                    <li><a href="subtopic-1.html">Name of Subtopic 1</a></li>
                    <li><a href="subtopic-2.html">Name of Subtopic 2</a></li>
                    <li><a href="subtopic-3.html">Name of Subtopic 3</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </nav>

### Duplicate the Customized Nav Code for use in the Footer

Copy the customized nav code for and paste it into the footer. Change the list's ID from id="menu" to id="bottom-menu".

        <footer>
            <ul id="bottom-menu">
                <li><a href="index.html">Home</a></li>
                <li><a href="subtopic-1.html">Name of Subtopic 1</a></li>
                <li><a href="subtopic-2.html">Name of Subtopic 2</a></li>
                <li><a href="subtopic-3.html">Name of Subtopic 3</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </footer>

### Add SVG placeholder and span tags for main navigation

Just like in the AP Nav exercise, we will have SVG icons in our navigation. We will also put the link name inside a span tag so that we can target it individually.

#### Before

        <ul id="menu">
            <li><a href="index.html">Home</a></li>
            <li><a href="subtopic-1.html">Name of Subtopic 1</a></li>
            <li><a href="subtopic-2.html">Name of Subtopic 2</a></li>
            <li><a href="subtopic-3.html">Name of Subtopic 3</a></li>
            <li><a href="contact.html">Contact</a></li>
        </ul>

#### After

        <ul id="menu">
            <li><a href="index.html"><!-- SVG code goes here --><span>Home</span></a></li>
            <li><a href="subtopic-1.html"><!-- SVG code goes here --><span>Name of Subtopic 1</span></a></li>
            <li><a href="subtopic-2.html"><!-- SVG code goes here --><span>Name of Subtopic 2</span></a></li>
            <li><a href="subtopic-3.html"><!-- SVG code goes here --><span>Name of Subtopic 3</span></a></li>
            <li><a href="contact.html"><!-- SVG code goes here --><span>Contact</span></a></li>
        </ul>


## Final Code

        <body>
            <nav class="primary-navigation">
            <button class="hide-text">Menu</button>

        <ul id="menu">
            <li><a href="index.html"><!-- SVG code goes here --><span>Home</span></a></li>
            <li><a href="subtopic-1.html"><!-- SVG code goes here --><span>Name of Subtopic 1</span></a></li>
            <li><a href="subtopic-2.html"><!-- SVG code goes here --><span>Name of Subtopic 2</span></a></li>
            <li><a href="subtopic-3.html"><!-- SVG code goes here --><span>Name of Subtopic 3</span></a></li>
            <li><a href="contact.html"><!-- SVG code goes here --><span>Contact</span></a></li>
        </ul>

            </nav>
            
            <header></header>
            <h1></h1>
            <main></main>
            <aside></aside>
            <footer>
                <ul id="bottom-menu">
                        <li><a href="index.html">Home</a></li>
                        <li><a href="subtopic-1.html">Name of Subtopic 1</a></li>
                        <li><a href="subtopic-2.html">Name of Subtopic 2</a></li>
                        <li><a href="subtopic-3.html">Name of Subtopic 3</a></li>
                        <li><a href="contact.html">Contact</a></li>
                    </ul>
            </footer>

            <script src="https://code.jquery.com/jquery-3.7.1.min.js"
            integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo="
            crossorigin="anonymous"></script>

            <script src="js/combined-scripts.js"></script>
        </body>