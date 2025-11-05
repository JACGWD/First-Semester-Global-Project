# Adding Images to Your Site

The proper way to add an image to a web page is to combine the image with a caption, often used for adding a byline.


## Simple HTML

        <figure>
            <img src="img/image.jpg" />
            <figcaption>Photo by John Smith</figcaption>
        </figure>


## HTML with Links

        <figure>
            <a href="#">
                <img src="img/image.jpg" />
            </a>
            <figcaption>
                Photo by <a href="#">John Smith</a> on <a href="#">Unsplash</a>
            </figcaption>
        </figure>

## Image Sizing

Read the [Image Sizes page for information on resizing the image properly](./image-sizes.md) for web design use.

<blockquote>

### TLDR;

Save your images at **1536px on the longest side**.

</blockquote>

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