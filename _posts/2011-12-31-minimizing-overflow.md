---
layout: post
categories: post
title:  "Minimizing Overflow"
excerpt: An alternative in laying out elements without the use of float/overflow.
---

Laying out elements with CSS's float, combined with the overflow property are vastly used, and this can result in display issues from rendered scrollbars, to cut off text - affecting readability.

Applying display's inline-block value results in more control, and cleaner CSS.

Take case for this sample navigation menu, having a background color, and centered text can be accomplished with the following:

    <ul>
    	<li><a>Services</a></li>
    	<li><a>About</a></li>
    	<li><a>Contact</a></li>
    </ul>

Styled like so:

    ul {
    	text-align: center;
    	background-color: #111;
    }
    li { display: inline; }
    a {
    	display: inline-block
    	padding: 10px;
    	color: white;
    }

Styling the same navigation menu using float/overflow will require an additional div, to address the background color:

    div { background-color: #000; }
    ul {
    	width: 300px;
    	margin: 0 auto;
    	overflow: hidden;
    }
    li { float: left; }
    a {
    	padding: 5px 10px;
    	color: white;
    }

Other issues involve the centering of the menu, and handling dynamic content will require for the CSS to be updated - ul's width.

Display inline-block can also be used to align icons, have column layouts, and works great with the positioning property, for advanced alignment.

Changing our floating ways reduces CSS, and cleaner markup.

Thanks for taking your time,
