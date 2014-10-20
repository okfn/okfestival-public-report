# How to use and edit this site

## The quickest way

Get permissions on this repository, and edit it straight from the github interface. All simple text editing can be done this way - once you save (write a message then commit changes) you should be able to see it live.

## The slower way

If you are making complex changes or you want to be sure about how this will look before it goes live, check out the repository and run (jekyll)[http://jekyllrb.com/docs/quickstart/].

    ~ $ git clone https://github.com/okfn/okfestival-public-report.git
    ~ $ cd okfestival-public-report
    ~/okfestival-public-report $ jekyll serve
    # => Now browse to http://localhost:4000

 Make sure when you commit that you do it to the gh-pages branch as this is how github knows to compile the jekyll site.

## Page structure

All content is in the 'pages' folder, each item in the first level navigation is stored in a folder named after the navigation item.

Content for the homepage and 'What you did' is generated from the [front matter](http://jekyllrb.com/docs/frontmatter/) that is contained in the sub-content pages. Front matter is the metadata contained between the --- at the top of every file.

All the rest of the subpages are in markdown files nested within the folders named after the navigation items.

## Page formatting - markdown

Content in the pages are described with [markdown](http://daringfireball.net/projects/markdown/), HTML or small includes. The main page heading is generated from the title or parent_title in the front matter.

### Simple markdown used

    # Main heading

    ## Secondary heading

    ### Tertiary heading

    --- for hard rules

    [Link Text](URL)

### Simple includes

Because the markup for Images and Quotes can be cumbersome to copy and paste, they use includes. The includes are formatted as follows.

Images:

    {% include image.html filename="NameOfImage.jpg" alt="Accessible alternate text" caption="Caption that goes under the image" %}

Quotes:

    {% include quote.html cite="Person, Publication" link="http://www.linktoquotedtext.com" quote="Here goeth the quote thing." %}

(NB. unfortunately the includes need to be all on one line as the line breaks confuse Jekyll )

### Simple formatting

    <span class="summary">Page summaries</span>

    <div class="pull">
        Images that need to be floated
    </div>



### Gallery

Images for anything described as a gallery are stored in the 'img' folder in the directory of the page.

For the 'What you did' page this is generated from the front matter on each subpage. The items are generated from the gallery_item description on each subpage.

    gallery_item:
        photos:
            -
              file: filename.jpg
              alt: Jane Doe
            -
              file: filename.jpg
              alt: John Smith
        caption_header: Communities
        caption: Some caption text


For the small image gallery on the 'How it was' page, the images are described in the /how-it-was/index.md front matter.

    gallery:
    photos:
        -
          img: https://regular_image.jpg
          thumb: https://small_image.jpg
          alt:
        -
          img: https://regular_image.jpg
          thumb: https://small_image.jpg
          alt:

## Front matter

Layout describes the default layout for the page

    layout: page

Page title or subpage title references the parent page

    parent_title: What You Did
    title: Communities

Identifier helps with the section specific styling

    identifier: what-you-did

Order controls the order that this page appears in the navigation

    order: 3


## Navigation

The main navigation and sub-navigation are generated. If you add new pages and sections these should appear automatically.

The sub-navigation is generated from the _includes/navigation.html with a flag in the _layouts/page.html.
