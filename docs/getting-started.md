---
title: Getting Started
nav_order: 2
---

> This is the template for all the repository under the internal docs org.

### Contents
* TOC
{:toc}

## How to edit

Please check the post here: [How to edit](/docs/how-to-edit)

## How to add new posts or a new level
### Add single page on the top level
1. Add new .md file under folder `docs` like the `example.md` we had.
2. Add the [font matter](https://jekyllrb.com/docs/front-matter/) section, the nav_order defines the place it at on the side nav bar. As you can see, the example is located at the 3rd place at the sidebar.
```md
---
title: Example
nav_order: 3
---
```
3. Then you are ready to write.

### Add a 2nd level
1. Add a new folder under folder `docs` like the `example-folder` we had.
2. Add `index.md` file under the new folder you created like `example-folder/index.md`. You define the folder's configuration in the index.md file. Here is the example of the font matter block:
```md
---
title: Example Folder
nav_order: 4
---
```
3. Then add new posts under the new created folder like `example-folder-child1.md` we have here. The font matter looks like this:
```md
---
title: Example Folder Child1
nav_order: 1
parent: Example Folder
---
```
  you need to define the `parent` so it knows it is under which folder. And the parent name should be the title defind in the index.md, here it is "Example Folder".

### Add a 3rd level

This is the lowest level it can get.

1. Add a new folder under the folder where you desire to put, like the `example-2d-folder` we have.
2. Add `index.md` file under the new folder you created like `example-folder/example-2nd-folder/index.md`. You define the folder's configuration in the index.md file. Here is the example of the font matter block:
  ```md
  ---
  title: Example 2nd Folder
  nav_order: 3
  parent: Example Folder
  ---
  ```
  you need to specify the parent, also the nav_order, which is at the 3rd position of the Example Folder. It you want it to be top, set nav_order to 1, and set the original 1st to be 3rd.
3. Then add new posts under the new created folder like `example-2nd-folder-child1.md` we have here. The font matter looks like this:
```md
---
title: Example Folder Child1
nav_order: 1
parent: Example 2nd Folder
---
```
  Again you need to define the parent so it knows which folder it belongs to.

## Feaures
### Image pop up feature

Here we use [magnific-popup](https://dimsemenov.com/plugins/magnific-popup/) plugin to add image pop up feature to avoid image placement hassle.

#### Single image

<a class="image-link" href="/assets/media/mbot-logo.png">
  <img src="/assets/media/mbot-logo.png" alt="Image Description" width="75">
</a>

You only need to define the width, the height is autofit.

#### Image gallery
<div class="popup-gallery">
  <a href="/assets/media/mbot-logo.png">
    <img src="/assets/media/mbot-logo.png" alt="Image Description"  width="75"> 
  </a>
  <a href="/assets/media/mbot-logo.png">
    <img src="/assets/media/mbot-logo.png" alt="Image Description"  width="75">
  </a>
</div>


<div class="popup-gallery">
	<a href="http://farm9.staticflickr.com/8242/8558295633_f34a55c1c6_b.jpg" title="The Cleaner"><img src="http://farm9.staticflickr.com/8242/8558295633_f34a55c1c6_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8382/8558295631_0f56c1284f_b.jpg" title="Winter Dance"><img src="http://farm9.staticflickr.com/8382/8558295631_0f56c1284f_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8225/8558295635_b1c5ce2794_b.jpg" title="The Uninvited Guest"><img src="http://farm9.staticflickr.com/8225/8558295635_b1c5ce2794_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8383/8563475581_df05e9906d_b.jpg" title="Oh no, not again!"><img src="http://farm9.staticflickr.com/8383/8563475581_df05e9906d_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8235/8559402846_8b7f82e05d_b.jpg" title="Swan Lake"><img src="http://farm9.staticflickr.com/8235/8559402846_8b7f82e05d_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8235/8558295467_e89e95e05a_b.jpg" title="The Shake"><img src="http://farm9.staticflickr.com/8235/8558295467_e89e95e05a_s.jpg" width="75" height="75"></a>
	<a href="http://farm9.staticflickr.com/8378/8559402848_9fcd90d20b_b.jpg" title="Who's that, mommy?"><img src="http://farm9.staticflickr.com/8378/8559402848_9fcd90d20b_s.jpg" width="75" height="75"></a>
</div>

### Math

We are using Katex here, the syntax is similar to LaTex, details can be found [here](https://just-the-docs.github.io/just-the-docs-tests/components/math/katex/index/).

$$
\begin{aligned}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{aligned}
$$