This will not work directly with the online editor at slides.com. If you would like to use the online editor, you can build your html slides and copy and paste the slides content into the existing index file in this repository. Some of your inline styles may or may not be lost.

*Note: a Slides.com free account does not let you include custom CSS which means we cannot use our fonts, or add our logo in an anchored, out of the way area. We are also not afforded as much customization as if you create your deck manually.*

-----
# Palantir.net Reveal.js 3 Theme and Slides Template

Use this repository when creating a slide deck to present at conferences if you are representing Palantir.net.

-----
## How to Use

1. Install Reveal.js by following the instructions here: https://github.com/hakimel/reveal.js
2. Pull down this repo and place the contents in the root of your Reveal.js directory, replacing the index file from that repo with the index file from this repository. WARNING: If you have already written out your slide content in the reveal repository, make sure that you save that content and don't overwrite it by replacing the index file.
3. If you plan to write or modify the sass, install breakpoint: http://breakpoint-sass.com/
4. Update the Title, Author, and Description metadata in the head of the index.html file.
4. Edit the html within the index file to contain the content for your presentation. Place your slide content within ```<div class="slides"> Your Slides Here! </div>```.
4. Follow the rest of the instructions from the Reveal.js readme to serve your slide deck.

-----
## Options

### Change Theme Color Scheme
This will switch background colors, change out logos, and change your code syntax highlighting. There is a light and a dark option available, as well as the light option with a white background.
  1. Open your index.html file in the root.
  2. On [line 26](https://github.com/palantirnet/palantir-reveal/blob/master/index.html#L26) change the class on the body tag to "light", "dark", or "white".

          <body class="light">
            Slide content here
          </body>
  3. Save your file.

### Remove or Add Background color to inline code.
This will remove the background color from a code sample.
  1. Open your index.html file in the root.
  2. Wherever you are inputting the code, add "class="no-container" to the pre tag around the code you'd like to not have a background color. Example:
  
          <pre class="no-container">
           Your Code here
          </pre>
  <small>An example of this can be seen  [here](https://github.com/palantirnet/palantir-reveal/blob/master/index.html#L248)</small>
  3. Save your file.

### Change the font size of your code.
The default font size is 15px. Pre-baked font classes include "font--12", "font--14", "font--16", "font--18", "font--20", "font--22", "font--24", "font--26", "font--28", "font--30", "font--32", "font--34", and "font--36". All font classes are measured in pixels, so be sure your aspect ratio is set correctly before you adjust font sizes.
  1. Open your index.html file in the root.
  2. Wherever you are inputting the code, add the appropriate class to the pre tag around the code you'd like to change the font size for. Example:
  
          <pre class="font--12">
           Your Code here
          </pre>
<small>An example of this can be seen [here](https://github.com/palantirnet/palantir-reveal/blob/master/index.html#L248)</small>
  3. Save your file.

### Have your code break rather than scroll right
  1. Open your index.html file in the root.
  2. Find the code that you want to break rather than to scroll.
  3. Add "style="word-wrap: break-word;" to your &#060;code&gt; opening tag.
  <small>An example of this can be seen [here](https://github.com/palantirnet/palantir-reveal/blob/master/index.html#L248)</small>
  4. Save your file.

### Change your slide aspect ratio.
This will change your default scaling aspect ratio and your max height/width for your slide container. This change is global and will affect all slides.
  1. Open /assets/js/reveal.js file in the root.
  2. On [lines 38 and 39 of reveal.js](https://github.com/palantirnet/palantir-reveal/blob/master/palantirnet-theme/assets/js/reveal.js#L38-L39) change the width and height attributes to the width and height you require.
    * default is set to 960 x 700
    * for 16:9 recommended to set width to 1500 and height to 844.
    * for 4:3 recommended to set width to 1200 and height to 900.
    * or choose a custom aspect ratio that best fits your screen.
  3. Save your file and serve your presentation.

### Add or Remove Margin from your slides container.
This will change the default left and right margin for your slides container. This however, will not change the max-width of your container.
  1. Open js/reveal.js file in the root.
  2. On [lines 42 of your reveal.js file](https://github.com/palantirnet/palantir-reveal/blob/master/palantirnet-theme/assets/js/reveal.js#L42) change margin attribute. The default is set to 0.05. Remember, this is a percentage of your height, and width, and also takes into consideration your zoom.
  3. It is recommended that you do not set the margin below 0.025 or above 0.1 as then the margin may be too small or too large.
  4. Save your file and serve your presentation.

### Add layouts to your slides.
This provides the option of having 2 column, 3 column, or 4 column layouts on your slides.
  1. Open your index.html file in the root.
  2. Find the section that you'd like to add a layout to.
  3. on the section tag, add the class "l-2up" for a 2 column layout, "l-3up" for a 3 column layout, or "l-4up" for a 4 column layout.
  4. Create 2, 3, or 4 divs depending on the layout you chose and add content to each div. The class is directly targeting child divs of the section, so you can have additional divs within your wrapper div.

  #### Examples
  Additionally, an inline example of the 4up can be seen starting on [line 40](https://github.com/palantirnet/palantir-reveal/blob/master/index.html#L40-L61)
   1. Two Column Grid
  
  ```
           <section class="l-2up">
               <div> This is your first column of content </div>
               <div> This is your second column of content </div>
           </section>
  ```
   2. Three Column Grid
  
  ```
           <section class="l-3up">
               <div> This is your first column of content </div>
               <div> This is your second column of content </div>
               <div> This is your third column of content </div>
           </section>
  ```
   3. Four Column Grid
  
  ```
           <section class="l-4up">
               <div> This is your first column of content </div>
               <div> This is your second column of content </div>
               <div> This is your third column of content </div>
               <div> This is your fourth column of content </div>
           </section>
  ```
  
### Add a secondary or partner logo.
This provides the option of display 2 logos in the footer area in the case of a partner presentation.
  1. Open your index.html file in the root.
  2. On line 404 there is example markup, commented out for this additional logo, or you can use this example.

            <a class="logo-wrapper" href="url-to-partner.com" title="Link to Partner's website">
              <div class="logo--2" style="background: url('your/image/path.png') no-repeat; background-size: contain; background-position: left bottom;">
                <p>Describe the logo here.</p>
              </div>
            </a>
  3. Replace the link href, the background image url, and the description in the p tag.
  4. This functionality only allows you to have one additional logo currently.

-----
## License

Copyright (C) 2015 Palantir.net. All rights reserved. http://www.palantir.net/
