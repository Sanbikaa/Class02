# Chart.js API  
- To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:
- The great things about Chart.js are that it’s simple to use and really very flexible. Plus, once you’ve mastered the basics here, you’ll discover that there are tons of optionslisted in the documentation.
 
 <hr />
 <h2>Basic usage of canvas</h2>
 <ul>
  <li>The id attribute isn't specific to the <canvas> element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance). It is always a good idea to supply an id because this makes it much easier to identify it in a script.</li>
  <li>The <canvas> element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas. We'll see how this is done in a dedicated chapter of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.</li>
  <li>The <canvas> element differs from an (img) tag in that, like for (video), (audio), or (picture) elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers.</li>
  <li>As a consequence of the way fallback is provided, unlike the (img) element, the (canvas) element requires the closing tag (canvas).</li>
  <li>The (canvas) element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.</li>
  <li>he fallback content is displayed in browsers which do not support (canvas). support programmatically by testing for the presence of the getContext() method.</li>
  </ul>
  
 <hr />
 <h2>Drawing shapes with canvas</h2>
 <ul>
  <li>Now that we have set up our canvas environment, we can get into the details of how to draw on the canvas. By the end of this article, you will have learned how to draw rectangles, triangles, lines, arcs and curves, providing familiarity with some of the basic shapes.</li>
  <li>Unlike SVG, <canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. Luckily, we have an assortment of path drawing functions which make it possible to compose very complex shapes</li>
  <li>Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.</li>
  <li>The fillRect() function draws a large black square 100 pixels on each side. The clearRect() function then erases a 60x60 pixel square from the center, and then strokeRect() is called to create a rectangular outline 50x50 pixels within the cleared square.</li>
  <li> In upcoming pages we'll see two alternative methods for clearRect(), and we'll also see how to change the color and stroke style of the rendered shapes.</li>
  <li> Now let's look at paths. A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:<li>
  </ul>
  <ol>
  <li>First, you create the path.</li>
  <li>Then you use drawing commands to draw into the path.</li>
  <li>Once the path has been created, you can stroke or fill the path to render it.</li>
  </ol>
  
  <hr />
  <h2>Applying styles and colors</h2>
  <ul>
  <li>fillStyle = color: Sets the style used when filling shapes.</li>
  <li>strokeStyle= color: Sets the style for shapes' outlines.</li>
  <li>color is a string representing a CSS (color), a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).</li>
  </ul>
  
  <hr />
  <h2>Drawing text</h2>
  <ul>
  <li>fillText(text, x, y [, maxWidth]) Fills a given text at the given (x,y) position. Optionally with a maximum width to draw</li>
  <li>strokeText(text, x, y [, maxWidth]) Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.</li>
  </ul>
  


    
    
    
    
