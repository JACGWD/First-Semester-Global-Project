# Adding Basic HTML Tags to your Texts

After importing the texts from Word to the HTML document, you must add HTML tags. For the most part, you will be adding H2, h3, section, paragraph and possibly list tags.

## Sample HTML: Add your texts to the \<main> tag

        <body>
            <nav class="primary-navigation">
            <button class="hide-text">Menu</button>

        <ul id="menu">
            <li><a href="index.html"><svg></svg><span>Home</span></a></li>
            <li><a href="subtopic-1.html"><svg></svg><span>Name of Subtopic 1</span></a></li>
            <li><a href="subtopic-2.html"><svg></svg><span>Name of Subtopic 2</span></a></li>
            <li><a href="subtopic-3.html"><svg></svg><span>Name of Subtopic 3</span></a></li>
            <li><a href="contact.html"><svg></svg><span>Contact</span></a></li>
        </ul>

            </nav>
            
            <header></header>
            <h1>About Animals</h1>

            <main>
                <!-- Your content texts go here -->
            </main>

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

## Sample \<main> after pasting your text

            <main>
                About Dogs
                
                Ea excepteur labore sit reprehenderit do quis Lorem minim culpa. Minim consectetur do id do consequat. Qui tempor consectetur quis eiusmod nostrud veniam do velit officia est quis. Irure ex do occaecat reprehenderit nisi duis tempor culpa commodo deserunt tempor. Fugiat elit aute duis fugiat adipisicing nisi occaecat sit labore et adipisicing. Enim officia ullamco elit aliqua pariatur pariatur ut exercitation sit ex nisi. 

                About Puppies

                Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.

                About Cats 
                
                Magna nisi enim consequat elit excepteur duis eu eiusmod laborum sunt dolore. Deserunt tempor sit incididunt sunt consequat ipsum reprehenderit elit eiusmod. Eiusmod aliqua non ullamco non laboris irure Lorem labore adipisicing.

                Non quis consequat aliquip voluptate ut deserunt occaecat occaecat cupidatat non. Eu aute labore in deserunt dolor minim. Ipsum id ad consectetur fugiat veniam fugiat fugiat non sunt. Consectetur veniam quis anim laborum. Ipsum quis elit eiusmod consequat aliqua laboris ad tempor. Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.

                About fish.
            </main>


If the HTML document is previewed when the text is like this, all the text will appear as one giant paragraph with no breaks or spaces. We need to add HTML tags to structure the text.

In the above example, we have:

- Two subtitles and two paragraph about dogs (four tag unit).
- One subtitle and two paragraphs about cats (three tag unit).
- One single paragraph about fish (one unit).

## Sample \<main> after adding HTML tags

            <main>
                <h2>About Dogs</h2>
                
                <p>Ea excepteur labore sit reprehenderit do quis Lorem minim culpa. Minim consectetur do id do consequat. Qui tempor consectetur quis eiusmod nostrud veniam do velit officia est quis. Irure ex do occaecat reprehenderit nisi duis tempor culpa commodo deserunt tempor. Fugiat elit aute duis fugiat adipisicing nisi occaecat sit labore et adipisicing. Enim officia ullamco elit aliqua pariatur pariatur ut exercitation sit ex nisi. </p>

                <h3>About Puppies</h3>

                <p>Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.</p>

                <h2>About Cats </h2>
                
                <p>Magna nisi enim consequat elit excepteur duis eu eiusmod laborum sunt dolore. Deserunt tempor sit incididunt sunt consequat ipsum reprehenderit elit eiusmod. Eiusmod aliqua non ullamco non laboris irure Lorem labore adipisicing.</p>

                <p>Non quis consequat aliquip voluptate ut deserunt occaecat occaecat cupidatat non. Eu aute labore in deserunt dolor minim. Ipsum id ad consectetur fugiat veniam fugiat fugiat non sunt. Consectetur veniam quis anim laborum. Ipsum quis elit eiusmod consequat aliqua laboris ad tempor. Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.</p>

                <p>About fish.</p>
            </main>

### HTML tags are about showing the hierarchy of the information

- H1: About Animals
- H2: About Dogs (first subsection about Animals)
- H3: About Puppies (breaks down the Dogs subsection into a new sub-subsection)
- H2: About Cats (goes back up one level, is a second subsection of About Animals) 
- P: About fish (third subsection of About Animals)   


        H1: About Animals
        |
        |--- H2: About Dogs
             |--- Paragraph about dogs
             |--- H3: About Puppies 
                  |--- Paragraph about puppies
        |
        |--- H2: About Cats
             |--- Paragraph about cats
             |--- Another paragraph about cats
        |
        |--- P: Single paragraph about fish

Notice that our content is in really three parts, but we have nine tags. We need to join our content into groups.


## Regrouping content into sections

            <main>

                <section class="dogs">
                    <h2>About Dogs</h2>
                    
                    <p>Ea excepteur labore sit reprehenderit do quis Lorem minim culpa. Minim consectetur do id do consequat. Qui tempor consectetur quis eiusmod nostrud veniam do velit officia est quis. Irure ex do occaecat reprehenderit nisi duis tempor culpa commodo deserunt tempor. Fugiat elit aute duis fugiat adipisicing nisi occaecat sit labore et adipisicing. Enim officia ullamco elit aliqua pariatur pariatur ut exercitation sit ex nisi. </p>
                    <h3>About Puppies</h3>
                    <p>Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.</p>
                </section>

                <section class="cats">
                    <h2>About Cats </h2>
                    
                    <p>Magna nisi enim consequat elit excepteur duis eu eiusmod laborum sunt dolore. Deserunt tempor sit incididunt sunt consequat ipsum reprehenderit elit eiusmod. Eiusmod aliqua non ullamco non laboris irure Lorem labore adipisicing.</p>
                    <p>Non quis consequat aliquip voluptate ut deserunt occaecat occaecat cupidatat non. Eu aute labore in deserunt dolor minim. Ipsum id ad consectetur fugiat veniam fugiat fugiat non sunt. Consectetur veniam quis anim laborum. Ipsum quis elit eiusmod consequat aliqua laboris ad tempor. Occaecat occaecat consectetur deserunt elit cupidatat esse et id quis sit reprehenderit commodo occaecat culpa. Veniam reprehenderit velit irure velit.</p>
                </section>

                <p class="fish">About fish.</p>
            </main>

## Note the use of Classes

In the above example, the content groups (sections and the fish paragraph) have been given classes. This is so that you can individually target either section or the fish paragraph so you can add style to that one specific item.

Learn more about [classes here](./classes-and-ids.md)