---
layout: work-post
title: CSS and jQuery Sliding Menu 
type: Navigation Menu
site_url: 
permalink: /work/slidemenu.html
image: /images/work/slidemenu.png
github:
---


Someone curious about the capabilities of pure HTML and CSS asked me to build a navigation menu that would work without needing JavaScript or any form of additional programming. The result was interesting, if not a little obvious.

In preparing this code sample, I was asked to create a menu that fulfilled a few aesthetic requirements:

<ul>
  <li>A full-width menu,</li>
  <li>Full-width subnavigation menus that slid out from under the main menu,</li>
  <li>Submenus that stick to the top of the window after scrolling,</li>
  <li>No dynamic languages or back-ends,</li>
  <li>And no using front-end frameworks.</li>
</ul>

<p>The task sounded simple enough. After a while, I managed to achieve this.</p>

<iframe height='268' scrolling='no' src='https://codepen.io/cdvillard/embed/MYPEaw/?height=268' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/cdvillard/pen/MYPEaw/'>MYPEaw</a> by Charles V. (<a href='http://codepen.io/cdvillard'>@cdvillard</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

  <p>Sure, the whole thing was full width and the submenus slid out from under the main menu, but the links couldn't work when content was present on the page because of <a href="https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Understanding_z_index">the complex stacking orders caused by  z-index properties</a>. Plus, there was no way to tell the submenu to stay fixed to the top of the page. CSS, while growing more flexible and powerful, is only capable of simple math. It can't handle logic such as, "If the page is scrolled to this point, affix this submenu to the top. Otherwise, don't." So, in order to achieve that functionality, JavaScript was necessary and to further simplify things, jQuery.</p>

<iframe height='268' scrolling='no' src='https://codepen.io/cdvillard/embed/JoeMZo/?height=268' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/cdvillard/pen/JoeMZo/'>JoeMZo</a> by Charles V. (<a href='http://codepen.io/cdvillard'>@cdvillard</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<p>Using jQuery allowed me to add and remove classes and logic to serve the functionality required. Additionally, while this sample uses a hosted version of jQuery, this is still considered a static element because the dependency on jQuery can be served with a local file as well.</p>
