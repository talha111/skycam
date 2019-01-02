<!DOCTYPE html>
<html lang="en-us">
  <head>
    <meta charset="UTF-8">
    <title>SolarIrradiance using DL</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <link rel="stylesheet" href="css/normalize.css">
    <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,700' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="css/cayman.css">
  </head>
  <body>
    <section class="page-header">
      <h1 class="project-name">Solar Irradiance forecasting with Deep Learning</h1>
      <h2 class="project-tagline">Project Page for our paper titled "A deep learning approach to solar-irradiance forecasting in sky-videos"</h2>
      <h2 class="project-tagline">Talha Ahmad Siddiqui, Samarth Bharadwaj, Shivkumar Kalyanaraman (2019)</h2>
      <a href="https://drive.google.com/file/d/1fKMXoaWLJaR985eILwY1nfaxXB2x7x5Y/view?usp=sharing" class="btn">View Paper</a>
      <!-- <embed src="https://sumanbogati.github.io/sample.pdf" type="application/pdf"> View Paper</embed> -->
      <a href="#" class="btn">Code (releasing soon)</a>
      <a href="#" class="btn">Data (releasing soon)</a>
    </section>

    <section class="main-content">
      <p> Ahead-of-time forecasting of incident solar-irradiance on a panel is indicative of energy yield and is essential for efficient grid distribution and planning. Typical approaches are based on meteorological physics models whose parameters are tuned by coarse-grained radiometric tiles sensed from geo-satellites.
      </p>


      <p><center><img src="conceptDiagram.png" style="max-width:70%;"></center></p>

      <p>
      This research presents a deep learning approach to observe and estimate short-term weather effects from sky-videos obtained with upward facing wide-lensed cameras and directly forecast solar irradiance. Our approach utilizes dilating convolution filters to learn a full-sky representation at varying scales via joint-training aided by auxiliary weather parameters that are sensed simultaneously. Multiple LSTMs with soft attention then leverage the full-sky representation to forecast the total surface irradiance by estimating flow, density and illuminance of clouds. We showcase results on two datasets obtained from weather stations in North America that captured sky-videos with relatively inexpensive optical hardware. They contain over a million images that span for one and 12 years respectively. Our deep learning approach significantly reduces the mean absolute percentage error for both nowcasting and forecasting. The architecture is illustrated below.
      </p>

      <p><center><img src="proposedApproach.png" style="max-width:80%;"></center></p>

      <p>
        Here are two sample videos in the month of April from each of the two datasets obtained from two different locations in the United States. We chose these videos, as they illustrate the challenges of irradiance forecasting (torrential rainy days in early summer).
      </p>

      <p>
        Corresponding to each frame, the interpolated mean of the <a href="https://arxiv.org/abs/1411.5752">hypercolomns</a> is plotted that is indicative of the focus of convolution filters. Further, the measured irradiance is plotted along with the nowcast prediction and ahead of time forecast (+1, +2, +3, & +4) hours. Specific observations are made on each video in the caption text.
      </p>

      <p><center><img src="Gif_Arizona.gif" style="max-width:60%;"></center></p>
      <p><center><img src="videograph_Arizona.gif" style="max-width:60%;"></center></p>
      
      <p>
        The Colorado video setup (TSI) consists of a sun tracker to protect the lens and equipment from direct exposure to the sun. Hence, the autofocus allows the camera to capture the clouds more clearly. We pick a challenging video from the dataset with large intra-day variations in solar irradiance. Notice, that the error in nowcasting is higher, when the sun tracker miss-fires.
      </p>

      <p><center><img src="Gif_Colorado.gif" style="max-width:60%;"></center></p>
      <p><center><img src="videograph_Colorado.gif" style="max-width:60%;"></center></p>


      

      <!-- <p>Text can be <strong>bold</strong>, <em>italic</em>, or <del>strikethrough</del>. <a href="https://github.com">Links</a> should be blue with no underlines (unless hovered over).</p>

      <p>There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.</p>

      <p>There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.</p>

      <blockquote>
      <p>There should be no margin above this first sentence.</p>

      <p>Blockquotes should be a lighter gray with a gray border along the left side.</p>

      <p>There should be no margin below this final sentence.</p>
      </blockquote>

      <h1>
      <a id="user-content-header-1" class="anchor" href="#header-1" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 1</h1>

      <p>This is a normal paragraph following a header. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.</p>

      <h2>
      <a id="user-content-header-2" class="anchor" href="#header-2" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 2</h2>

      <blockquote>
      <p>This is a blockquote following a header. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.</p>
      </blockquote>

      <h3>
      <a id="user-content-header-3" class="anchor" href="#header-3" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 3</h3>

      <pre><code>This is a code block following a header.</code></pre>

      <h4>
      <a id="user-content-header-4" class="anchor" href="#header-4" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 4</h4>

      <ul class="task-list">
      <li>This is an unordered list following a header.</li>
      <li>This is an unordered list following a header.</li>
      <li>This is an unordered list following a header.</li>
      </ul>

      <h5>
      <a id="user-content-header-5" class="anchor" href="#header-5" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 5</h5>

      <ol class="task-list">
      <li>This is an ordered list following a header.</li>
      <li>This is an ordered list following a header.</li>
      <li>This is an ordered list following a header.</li>
      </ol>

      <h6>
      <a id="user-content-header-6" class="anchor" href="#header-6" aria-hidden="true"><span class="octicon octicon-link"></span></a>Header 6</h6>

      <table>
      <thead>
      <tr>
      <th>What</th>
      <th>Follows</th>
      </tr>
      </thead>
      <tbody>
      <tr>
      <td>A table</td>
      <td>A header</td>
      </tr>
      <tr>
      <td>A table</td>
      <td>A header</td>
      </tr>
      <tr>
      <td>A table</td>
      <td>A header</td>
      </tr>
      </tbody>
      </table>

      <hr>

      <p>There's a horizontal rule above and below this.</p>

      <hr>

      <p>Here is an unordered list:</p>

      <ul class="task-list">
      <li>Salt-n-Pepa</li>
      <li>Bel Biv DeVoe</li>
      <li>Kid 'N Play</li>
      </ul>

      <p>And an ordered list:</p>

      <ol class="task-list">
      <li>Michael Jackson</li>
      <li>Michael Bolton</li>
      <li>Michael Bublé</li>
      </ol>

      <p>And an unordered task list:</p>

      <ul class="task-list">
      <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox" checked="" disabled=""> Create a sample markdown document</li>
      <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox" checked="" disabled=""> Add task lists to it</li>
      <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox" disabled=""> Take a vacation</li>
      </ul>

      <p>And a "mixed" task list:</p>

      <ul class="task-list">
      <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox" disabled=""> Steal underpants</li>
      <li>?</li>
      <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox" disabled=""> Profit!</li>
      </ul>

      <p>And a nested list:</p>

      <ul class="task-list">
      <li>Jackson 5

      <ul class="task-list">
      <li>Michael</li>
      <li>Tito</li>
      <li>Jackie</li>
      <li>Marlon</li>
      <li>Jermaine</li>
      </ul>
      </li>
      <li>TMNT

      <ul class="task-list">
      <li>Leonardo</li>
      <li>Michelangelo</li>
      <li>Donatello</li>
      <li>Raphael</li>
      </ul>
      </li>
      </ul>

      <p>Definition lists can be used with HTML syntax. Definition terms are bold and italic.</p>

      <dl>
          <dt>Name</dt>
          <dd>Godzilla</dd>
          <dt>Born</dt>
          <dd>1952</dd>
          <dt>Birthplace</dt>
          <dd>Japan</dd>
          <dt>Color</dt>
          <dd>Green</dd>
      </dl>

      <hr>

      <p>Tables should have bold headings and alternating shaded rows.</p>

      <table>
      <thead>
      <tr>
      <th>Artist</th>
      <th>Album</th>
      <th>Year</th>
      </tr>
      </thead>
      <tbody>
      <tr>
      <td>Michael Jackson</td>
      <td>Thriller</td>
      <td>1982</td>
      </tr>
      <tr>
      <td>Prince</td>
      <td>Purple Rain</td>
      <td>1984</td>
      </tr>
      <tr>
      <td>Beastie Boys</td>
      <td>License to Ill</td>
      <td>1986</td>
      </tr>
      </tbody>
      </table>

      <p>If a table is too wide, it should condense down and/or scroll horizontally.</p>

      <table>
      <thead>
      <tr>
      <th>Artist</th>
      <th>Album</th>
      <th>Year</th>
      <th>Label</th>
      <th>Awards</th>
      <th>Songs</th>
      </tr>
      </thead>
      <tbody>
      <tr>
      <td>Michael Jackson</td>
      <td>Thriller</td>
      <td>1982</td>
      <td>Epic Records</td>
      <td>Grammy Award for Album of the Year, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&amp;B Album, Brit Award for Best Selling Album, Grammy Award for Best Engineered Album, Non-Classical</td>
      <td>Wanna Be Startin' Somethin', Baby Be Mine, The Girl Is Mine, Thriller, Beat It, Billie Jean, Human Nature, P.Y.T. (Pretty Young Thing), The Lady in My Life</td>
      </tr>
      <tr>
      <td>Prince</td>
      <td>Purple Rain</td>
      <td>1984</td>
      <td>Warner Brothers Records</td>
      <td>Grammy Award for Best Score Soundtrack for Visual Media, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&amp;B Album, Brit Award for Best Soundtrack/Cast Recording, Grammy Award for Best Rock Performance by a Duo or Group with Vocal</td>
      <td>Let's Go Crazy, Take Me With U, The Beautiful Ones, Computer Blue, Darling Nikki, When Doves Cry, I Would Die 4 U, Baby I'm a Star, Purple Rain</td>
      </tr>
      <tr>
      <td>Beastie Boys</td>
      <td>License to Ill</td>
      <td>1986</td>
      <td>Mercury Records</td>
      <td>noawardsbutthistablecelliswide</td>
      <td>Rhymin &amp; Stealin, The New Style, She's Crafty, Posse in Effect, Slow Ride, Girls, (You Gotta) Fight for Your Right, No Sleep Till Brooklyn, Paul Revere, Hold It Now, Hit It, Brass Monkey, Slow and Low, Time to Get Ill</td>
      </tr>
      </tbody>
      </table>

      <hr>

      <p>Code snippets like <code>var foo = "bar";</code> can be shown inline.</p>

      <p>Also, <code>this should vertically align</code> <del><code>with this</code></del> <del>and this</del>.</p>

      <p>Code can also be shown in a block element.</p>

      <pre><code>var foo = "bar";
</code></pre>

      <p>Code can also use syntax highlighting.</p>

      <div class="highlight highlight-Javascript"><pre><span class="pl-k">var</span> foo <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>bar<span class="pl-pds">"</span></span>;</pre></div>

      <pre><code>Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.</code></pre>

      <div class="highlight highlight-Javascript"><pre><span class="pl-k">var</span> foo <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>The same thing is true for code with syntax highlighting. A single line of code should horizontally scroll if it is really long.<span class="pl-pds">"</span></span>;</pre></div>

      <p>Inline code inside table cells should still be distinguishable.</p>

      <table>
      <thead>
      <tr>
      <th>Language</th>
      <th>Code</th>
      </tr>
      </thead>
      <tbody>
      <tr>
      <td>Javascript</td>
      <td><code>var foo = "bar";</code></td>
      </tr>
      <tr>
      <td>Ruby</td>
      <td><code>foo = "bar"</code></td>
      </tr>
      </tbody>
      </table>

      <hr>

      <p>Small images should be shown at their actual size.</p>

      <p><a href="https://camo.githubusercontent.com/16a9d5241f679b6429fc0597f10816dd2665bbb2/687474703a2f2f706c6163656b697474656e2e636f6d2f672f3330302f3230302f" target="_blank"><img src="https://camo.githubusercontent.com/16a9d5241f679b6429fc0597f10816dd2665bbb2/687474703a2f2f706c6163656b697474656e2e636f6d2f672f3330302f3230302f" alt="" data-canonical-src="https://placekitten.com/g/300/200/" style="max-width:100%;"></a></p>

      <p>Large images should always scale down and fit in the content container.</p>

      <p><a href="https://camo.githubusercontent.com/afe46418285497605cf4f6376b75f8c818658fb1/687474703a2f2f706c6163656b697474656e2e636f6d2f672f313230302f3830302f" target="_blank"><img src="https://camo.githubusercontent.com/afe46418285497605cf4f6376b75f8c818658fb1/687474703a2f2f706c6163656b697474656e2e636f6d2f672f313230302f3830302f" alt="" data-canonical-src="https://placekitten.com/g/1200/800/" style="max-width:100%;"></a></p>

      <pre><code>This is the final element on the page and there should be no margin below this.</code></pre>
 -->
      <footer class="site-footer">
        <span class="site-footer-owner"><a href="#">This page</a> is maintained by <a href="#">IBM</a>.</span>
        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a>.</span>
      </footer>

    </section>

  </body>
</html>
