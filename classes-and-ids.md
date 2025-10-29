# Classes and IDs

Classes and IDs are ways to name/target a specific part of a web page. CSS can use either ID or class in exactly the same way, it makes no difference how you give a name to an element the same style rules will apply.

        <ul>
            <li class="red">Billy Poppins</li>
            <li id="red">François Lesmatte</li>
            <li class="red">Jonny Smith</li>
            <li class="red">Mary Poppins</li>
        </ul>

        .red {color: red;}

        #red {color: red;}

The main difference is that classes are meant to be reused multiple times per page, whereas IDs are meant to be unique. This is only really important when using javascript.

## A Class

- Using a class is the most common way of targeting a specific part of the page.
- Classes can be used multiple times per page.
- In CSS, a class name starts with a period: .classname

### HTML

        <ul class="students">
            <li>Billy Poppins</li>
            <li>François Lesmatte</li>
        </ul>


        <ul class="teachers">
            <li>Maggie Poppins</li>
            <li>Juliette Lasmatte</li>
        </ul>

        <ul>
            <li class="students">Billy Poppins</li>
            <li class="students">François Lesmatte</li>
            <li class="teachers">Maggie Poppins</li>
            <li class="teachers">Juliette Lasmatte</li>
        </ul>


### CSS
        .students {color: blue}

        .teachers {font-weight: bold;}


See: [https://www.w3schools.com/html/html_classes.asp](https://www.w3schools.com/html/html_classes.asp)

## An ID

- Using an ID is the least common way of targeting a specific part of the page.
- An ID can be used only one time per page. 
- You can have multiple different IDs on a page.
- Javascript depends on IDs to provide interactivity (such as showing the #menu when clicking the hamburger icon).
- In CSS, an ID name starts with a hash tag: #idname

### HTML

        <ul id="students">
            <li>Billy Poppins</li>
            <li>François Lesmatte</li>
        </ul>


        <ul id="teachers">
            <li>Maggie Poppins</li>
            <li>Juliette Lasmatte</li>
        </ul>

        <ul>
            <li id="bp1234567">Billy Poppins</li>
            <li id="fl7654321">François Lesmatte</li>
            <li id="7035">Maggie Poppins</li>
            <li id="7855">Juliette Lasmatte</li>
        </ul>


### CSS
        .students {color: blue}

        .teachers {font-weight: bold;}

See: [https://www.w3schools.com/html/html_id.asp](https://www.w3schools.com/html/html_id.asp)