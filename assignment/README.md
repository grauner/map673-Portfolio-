# Assignment 01

Assignment 01 requires the completion of three parts:

* Part I: respond to the [Introductions](https://uk.instructure.com/courses/1952466/discussion_topics/12289608) Discussion thread within Canvas. (**1 pt**)
* Part II: respond to [Reading response #1](https://uk.instructure.com/courses/1952466/discussion_topics/12289618) Discussion thread within Canvas. (**1 pt**)
* Part III: make a personal web portfolio using Bootstrap (or another boilerplate/framework of your choosing). (**8 pts**) 

You should build your portfolio within the **lesson-01/** directory of your **map673-module-01-_username_/** repository (and commit and push changes as you work). This way your instructor can easily help you diagnose problems along the way.

However, the final product will be copied over to a new repository you'll create on your personal GitHub account (see the [instructions below](#hosting-your-portfolio-on-github-pages)).

Requirements for the deliverable:

* Portfolio should be hosted on GitHub and rendered through GitHub Pages
* Portfolio must showcase at least four mapping projects from NMP courses. These may include static maps, web maps hosted on GitHub Pages or another hosting service, and/or links to maps hosted on a service such as CARTO.
* Each project should be displayed using a smaller image, some descriptive text about the map, and a brief summary of the tools and processes used to create the map. You may wish to include links to the data sources of the maps as well, depending on the map and if it doesn't make that clear.
* Portfolio should include a brief "About" section which summaries your public/professional persona.
* Portfolio should minimally link to your GitHub account (and other websites, social media, and contact information of your choice).
* Portfolio should be usable on mobile, tablet, and desktop devices.

Use the *lesson-template/* provided within the *module-01/* directory for guidance and submit a URL to the portfolio within Canvas by the due date.

## Recommendations for completing the portfolio

First, assemble the following:

* links to web maps that you've built and are hosted through GitHub Pages or another hosting service (such as your "hometown" map created in MAP672)
* links to maps hosted on a web service such as CARTO
* large, high-resolution images of static maps you've created (to which the web portfolio will link for viewing or downloading)
* smaller, low-resolution images for displaying in the portfolio
* copy: text meeting the requirements listed above (i.e., descriptions of the map, about you, etc)

This is the content of your product, the production of which is much more closely aligned with Chimero's "stepping back" to view the project from afar. The content should inform the decisions about how to build the site. Therefore, it is always preferable to have the content first and let the design unfold from it.

Once the layout and visual design of your portfolio is established, build the content into the page. Then, tweak and iterate the layout and visual design again. Real content always upsets a design that rests upon the Lorem ipsum filler content.

### Text

Insert your copy into the document, and adhere to using semantically meaningful markup when you can (you may need to refer back to Lesson 02 of 672). In other words, use headings (`<h1>`, `<h2>`, etc) to establish the hierarchal order of the content. Use `<p>` tags for paragraphs and ordered, unordered, or definition lists for lists (and not a paragraph with a bunch of `<br>` breaking tags within it). You can also use `<strong></strong>` tags to make text bold to help the reader skim over the key points and concepts related to your map descriptions.

### Hyperlinks

Use semantically meaningful text as the [link text](https://www.marketingterms.com/dictionary/link_text/).

You may also wish to use the `target="_blank"` attribute on the anchor tags so links open in new tabs or pages, rather than directing the user away from your site:

```html
<a target="_blank" href="https://bl.ocks.org/">Popular Blocks<a>
```

Test all links before you submit!

### Images

For the "thumbnail" images on your portfolio page, you'll want to process your images to reduce the file size and overall page load. Save these images in the **images/** directory that resides alongside your **index.html** file. You'll then need to provide a relative path to this image from the **index.html** document.

For example, in the **lesson-01-template/**, if you wanted to replace one of the gray filler images (`http://placehold.it/430x245`) with the **spotlight.png** file in the **images/** directory, update the HTML within the **index.html** document with a relative path to the image like this:

```html
<a href="#"><img class="card-img-top" src="images/spotlight.png" alt=""></a>
```

You'll then want to replace the pound symbol in `<a href="#">` with a URL to either another web page (such as the web map hosted on a server) or a static image or PDF file. You may want to create an additional directory named **maps/** for storing the larger, high-resolution versions of static maps. If this were the case for the spotlight map, you'd update the HTML to be something like this:

```html
<a href="maps/spotlight.pdf"><img class="card-img-top" src="images/spotlight.png" alt="spotlight map"></a>
```

### Hosting your portfolio on GitHub Pages

Within MAP672, you likely used GitHub Pages to host and share your "hometown map." GitHub Pages can be used to "serve" HTML/CSS/JavaScript within any repository as a web page rather than merely a collection of text-based files.  The client uses the URL **_username_.github.io/repository-name/** to access these rendered webpages. But GitHub reserves a particular repository you can create specifically for serving static websites (such as the one we've built using Bootstrap). This repository will be named **_username_.github.io** and you should place your portfolio at the root of this directory.

To create your GitHub Pages repository, follow the instructions provided on GitHub's website: [GitHub Pages](https://pages.github.com/). When answering the question, *What git client are you using?*, you'll likely want to choose either "GitHub for Windows" or "GitHub for Mac" unless you're using the terminal.

For their step 3 "Create an index file" &ndash; after you've cloned the new repository to your local machine &ndash; use the **index.html** file you created for your portfolio and copy into the new repository the associated **css/**, **js**, **vendor**, and other files/folders used by the index page.

Your file/directory structure should look something like this:
```text
- _username_.github.io/
    - index.html
    - css/
        - styles.css
    - js/
        - custom.js
    - vender/
        - bootstrap/
            - css/
                - bootstrap.min.css
            - js/
                - bootstrap.min.js
        - jquery/
            - jquery.min.js 
```

Note that your **map673-module-01-_username_/lesson-01/** directory should NOT be included within the **_username_.github.io/** directory, only the contents of the portfolio itself.

### Hosting web maps created in MAP672

To revisit the process we used to create a "hometown-map" web page rendered through GitHub Pages, I'll walk through an example. Locate your solution for map672 Lab 08 on your local file system to follow along.

Let's say for Lab 08 you created a [Proportional Symbol Map of Hydro Power](http://bl.ocks.org/rgdonohue/80ef203479b5f65db8e5) using some silly Hello Kitty icons as the symbols. Again, the **index.html** and associated data files may be buried within your NMP course repository at **map672-module-08-_username_/lab-08/** . You want to copy the contents of the **lab-08/** directory over to the new repository at the local level. But first, you need to create this new repository in GitHub and clone that down to your machine.

Logged to your GitHub account, create a new repository using the small plus drop-down at upper right. Give your new repository a descriptive name (no spaces!). You can add an optional description. Importantly, check the "Initialize this repository with a README" option. This will help you clone your repository down easily.

![Example portfolio web page layout](graphics/create-new-repo.gif)  
**Figure 01.** Creating a new repository in GitHub.

After you've created this new repository (currently empty, other than the the README.md file automatically created by GitHub), you're ready to clone it down to your machine. You do this in the same way as you cloned the NewMapsPlus course repo and your own MAP672 repo to your local machine (refer to MAP672 Lesson 01).

Clone your new repository down and save it to your local machine. For general organization, you'll likely want to clone it into the same directory as your other GitHub repositories. Do NOT clone in inside your *map673-module-01* repo directory, nor your *username.github.io* repo directory.

Many of us are working in the GitHub Desktop client application. This process will look like this:

![Cloning the new repository to the local machine](graphics/clone-new-repo.gif)  
**Figure 02.** Cloning the new repository to the local system.

After the cloning is complete, go into the file/directory structure on your local system, examine the new repository directory, and then **copy the contents** of the working web application/map (including any necessary data and asset files) from the **map672-module-08-username/lab-08/** directory into the new repository's directory.

**Caution**: Copy the **contents of** the *lab-08/* directory, not the entire directory itself. In other words, your file system should NOT be **_username_.github.io/us-renewable-energy/lab-08/index.html**, but rather **_username_.github.io/us-renewable-energy/index.html**. The key is to ensure the `index.html` file for your web application/map is at the root of your new repo directory (we call it "root" but it's also referred to as the "top" directory).

![Copying files to the new repository on the local system](graphics/copy-files-to-new-repo.gif)  
**Figure 03.** Copying files to the new repository on the local system.

Once we do this, we can check the Git status of our repository in GitHub Desktop to verify there are new uncommitted changes to our repository. We can go ahead and commit these, and sync up with our remove repository to verify.

![Committing changes to the repository](graphics/commit-new-to-repo.gif)  
**Figure 04.** Committing changes to the repository.

Within the web browser, refresh the GitHub repository to see we've added the new files to the repository and pushed them to the remote.

To do serve our map as rendered pages from the new repository, we'll use a technique known as [Simpler GitHub Pages publishing](https://github.com/blog/2228-simpler-github-pages-publishing) (again, we did this in Module 01 of MAP672). Go into the settings of your new repository and enable your master branch as the source for building GitHub Pages from that repository.

Now you can navigate your web browser to a URL address such as `https://username.github.io/us-renewable-energy/`. If all is working correctly, you should be seeing your rendered web page and map. Test the remotely-hosted page in your web browser (including all the links!).

You can then update the links within your portfolio to point toward this URL:

```html
<a target="_blank" href="https://username.github.io/us-renewable-energy/">US Renewable Energy<a>
```

