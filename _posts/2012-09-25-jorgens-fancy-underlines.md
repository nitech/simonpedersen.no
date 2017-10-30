---
ID: 12
post_title: 'Jørgen&#8217;s fancy underlines'
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2012/09/25/jorgens-fancy-underlines/
published: true
post_date: 2012-09-25 22:24:30
---
Jørgen Winsnes is one of the brightest designes I know. He recently asked me to make him some fancy hover effects that he wanted to make a standard on EVERY project (so he said). Specifically, he wanted the underline on a link to grow from left to right and then disappear to the right when hovering. <!--more-->I did some research, trying to make a solution without JavaScript for the simplicity of just including a few lines of CSS. However, it turned out that animating pseudo elements with transition in CSS3 is only supported in Firefox. Not even Chrome. So I ended up writing a jQuery plugin instead. And to be honest, it was incredibly much less work than fiddling with the pseudo classes. 

<span class="button button-white"><a title="hoverLineGrow is a jQuery plugin that makes fancy underline hover effects" href="http://jsfiddle.net/nitech/wph34/" target="_blank">Demo</a></span><span class="button button-green"> <a title="Download the source code from Github" href="https://github.com/nitech/hoverLineGrow" target="_blank">source</a></span>