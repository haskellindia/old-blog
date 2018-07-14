# Haskell Learning Trails
Haskell Learning Trails (HLT) is a series of learning materials aimed at beginners to intermediate Haskell Developers. The materials are grouped into "Trails" similar to how Java learning aids are, and each trail describes a specific concept. The tutorials are in the form of presentation slides, which need to be worked out along with actual practicals. The whole thing is meant as a self-paced and self-learning aid for Haskell.

# How to contribute to the HLT project
HLT slides are based on [reveal.js][1]. All slides are in the folder "slides", arranged by the HLT series that they belong to.

To begin contributing, do the following:

- Add your name in the "Credit" section of the content.md file (see slide organisation below)
- Install [node.js][2]
- Now, clone the HLT repository, and install relevant node modules:

```
    $ git clone https://github.com/haskellindia/haskellindia.github.io hlt
    $ cd hlt
    $ npm install
```
- Make a symbolic link to the slides folder within the reveal.js folder (so that you can test your
  changes with a local npm server before committing and pushing to github):
```
   $ cd reveal.js
```
   On Linux / UNIX flavours:
```
   $ ln -s ../slides slides
   $ ln ../index.html index.html
```
  On windows (start a command prompt as **_Administrator_**)
```
   $ mklink slides ..\slides
   $ mklink /h index.html ..\index.html 
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
- Decide on what gets into your slide: a single piece of information (such as bullet points, or a quote, etc.) or a double-column slide having two pieces of information on the left and the right side of your slides.
- Once decided, choose the template for your slide from the "templates" folder:
  - If your slide is a single-column slide, use the section for single-column from the template contents file.
  - If your slide is a double-column slide, use the section for double-column from the template contents file.
- In index.html of your HLT series, search for the HTML comment: `"<!-- ALL SLIDES BEGIN HERE -->"`
  - Change the title in the tile slide
- If there are any images in your slides, put them in the "images" directory within your HLT directory (create the
  directory if not yet present.)   

# Advanced editing
Reveal.js has many more advanced editing features, and feel free to try them out! Only aspect that needs to be intact is the general template (the header, footer, logo and copyright elements): the content area can just go as you want it. This is just to have some uniformity in all our slides.

ENJOY!  


[1]: https://github.com/hakimel/reveal.js "reveal.js"
[2]: https://nodejs.org/en/ "node.js"