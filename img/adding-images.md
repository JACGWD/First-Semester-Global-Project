# Adding Images

The proper way to add an image to a web page is to combine the image with a caption, often used for adding a byline.

## Sample HTML

        <figure>
            <img src="img/photo.jpg" />
            <figcaption>Photo by John Doe</figcaption>
        </figure>      

## Sample HTML with Links

        <figure>
            <a href="#"><img src="img/photo.jpg" /></a>
            <!-- link to another web page on the current site -->

            <figcaption>
                <a href="#">Photo by John Doe</a>
                <!-- link to photographer's site -->
            </figcaption>

        </figure>      



## Credit the photographer

For each photo, add a byline given credit to the photographer. When you
download an image from Unsplash, there is a popup that appears at the
bottom of the page where you can copy the attribution HTML code. Paste
this in the \<figcaption\> tag.

### Credit Unsplash 

<figure>
<img src="img/pupaza.jpg" />
<figcaption>Photo by <a
href="https://unsplash.com/@davfts?utm_content=creditCopyText&amp;utm_medium=referral&amp;utm_source=unsplash">David
Pupăză</a> on <a
href="https://unsplash.com/photos/black-flat-screen-computer-monitor-Q9-QEy1_jYI?utm_content=creditCopyText&amp;utm_medium=referral&amp;utm_source=unsplash">Unsplash</a></figcaption>
</figure>


<figure>
<img src="img/unsplash.png" />
<figcaption>Copy the code from the Unsplash attribution popup by clicking the icon in the red box</figcaption>
</figure>

        <figure>
            <img src="img/unsplash-photo.jpg">

            <figcaption>Photo by <a href="https://unsplash.com/@davfts?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">David Pupăză</a> on <a href="https://unsplash.com/photos/black-flat-screen-computer-monitor-Q9-QEy1_jYI?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
            </figcaption>      

        </figure>

### Credit Your Own Work 

If you took the picture yourself, simply add a **copyright notice**
under your photo:

            <figure>
              <img src="img/my-photo.jpg">

              <figcaption>
                &copy; Your Name Goes Here, 2025
              </figcaption>      
            </figure>