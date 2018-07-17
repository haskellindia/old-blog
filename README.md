# Haskell Learning Trails
Haskell Learning Trails (HLT) is a series of learning materials aimed at beginners to intermediate Haskell Developers. The materials are grouped into "Trails" similar to how Java learning aids are, and each trail describes a specific concept. The tutorials are in the form of presentation slides, which need to be worked out along with actual practicals. The whole thing is meant as a self-paced and self-learning aid for Haskell.

# How to contribute to the HLT project
HLT slides are based on [reveal.js]. All slides are in the folder "slides", arranged by the HLT series that they belong to.

To begin contributing, do the following:

- Add your name in the "Credit" section of the content.md file (see slide organisation below)
- Install [node.js]
- Now, clone the HLT repository, and install relevant node modules:

```
    $ git clone https://github.com/haskellindia/haskellindia.github.io hlt
    $ cd hlt
    $ npm install
```
- Make a symbolic link to the reveal.js folder within reveal.js (so that you can test your
  changes with a local npm server before committing and pushing to github):
```
   $ cd reveal.js
```
   On Linux / UNIX flavours:
```
   $ ln -s ../reveal.js reveal.js
```
  On windows (start a command prompt as **_Administrator_**)
```
   $ mklink reveal.js ..\reveal.js
```  
- Finally, start the node server locally to serve your slides:
```
    $ npm start
```
 You can now check the changes to your slides at http://localhost:8000

# Slide organisation
The slides of HLT are in the "slides" folder, and templates for the slides are in the "templates" folder. An explanation of what each template is for, and how the slides are organised (or, to be organised if you start a trail, or contribute to an ongoing trail) is as follows:

```
     |
     +-- reveal.js <-- All reveal.js code is in here.
     |
     +-- slides <-- All slide contents are here
            |
            +-- hlt01  <-- HLT01 slides
            |    |
            |    +-- index.html   <-- This is the start slide of the series
            |    |
            |    +-- content.md <-- All slide contents get in here
            |    |
            |    +-- images    <-- Folder for images, if any
            |
            +-- hlt02 <-- HLT02 slides
            |    .
            |    .
            |
            +-- templates  <-- All templates in this directory
                   |
                   +-- _index.html  <-- Template for the start slide of a series
                   |
                   +-- _contents.md <-- Template for slide contents

```

# How to begin a new slide in an ongoing trail
- Create a new hlt<nn> directory under "slides"
- Copy the _index.html and _content.md in this new folder as index.html and content.md
- Decide on what gets into your slide: a single piece of information (such as bullet points, or a quote, etc.) or a double-column slide having two pieces of information on the left and the right side of your slides.
- Once decided, choose the template for your slide from the "templates" folder:
  - If your slide is a single-column slide, use the section for single-column from the template contents file.
  - If your slide is a double-column slide, use the section for double-column from the template contents file.
- In index.html of your HLT series, search for the HTML comment: `"<!-- ALL SLIDES BEGIN HERE -->"`
  - Change the title in the tile slide
- If there are any images in your slides, put them in the "images" directory within your HLT directory (create the
  directory if not yet present.)
- All contents of your slides will have to be in "content.md"
  - Begin each slide with a title: a line followed by `<!-- .element: id="title" -->`
  - Separate each slide with a `---`   
  - You can also have "vertical slides" - slides that need to be navigated using up/down arrows
    - Separate each vertical line with a `===`
  - Before starting a "section" in your learning trail, add a "section" slide that simply contains
    a section heading and its brief. Check the content.md template file for an example of a section slide.

The best way to create your slides is to use the formats in the template _content.md - it is actually pretty easy to create slides! And, of course, knowing how to use [markdown] is a pre-requisite - which is also very easy.    

# Advanced editing
Reveal.js has many more advanced editing features, and feel free to try them out! Only aspect that needs to be intact is the general template (the header, footer, logo and copyright elements): the content area can just go as you want it. This is just to have some uniformity in all our slides.

ENJOY!  


[reveal.js]: https://github.com/hakimel/reveal.js
[node.js]: https://nodejs.org/en/
[markdown]: https://daringfireball.net/projects/markdown/