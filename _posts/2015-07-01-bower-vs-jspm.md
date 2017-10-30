---
ID: 376
post_title: Bower vs JSPM
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2015/07/01/bower-vs-jspm/
published: true
post_date: 2015-07-01 06:04:56
---
We are in the middle of a major shift in the web development world, and seeing the greatest change in about 15 years with ECMAScript 2015 (ES6) just released and and 2016 (ES7) on its way. Because of this rapid change, a myriad of tools are popping up every day and it can be hard to keep up with all the fancy acronyms. This post explains the differences between the [Bower package manager][1] and [JSPM][2] or JavaScript Package Manager. 
## Package Manager? A package manager lets you search for and install software packages that your application depends on. So there is usually a web site, like 

[bower.io/search][3] that shows you what kind of packages the manager has available, and you can also use the CLI (command line interface) to search for packages. When you install a package, you can choose to save what package you installed to a config file, so your app will remember its dependencies. 
## Bower vs JSPM So what is the difference between Bower and JSPM? The short answer is that while both managers let you install and update dependencies, JSPM is more future oriented. It automatically downloads 

[SystemJS][4], which is a universal dynamic module loader that loads both ES6 modules, AMD, CommonJS and global scripts and maintains config.js to help SystemJS know where to find the dependencies. [This StackOverflow question][5] has further details. Watch this recording from the London React Meetup where Jack Franklin talks about SystemJS and demonstrates how it works: https://www.youtube.com/watch?v=NpMnRifyGyw 
##

 [1]: http://bower.io
 [2]: http://jspm.io
 [3]: http://bower.io/search/
 [4]: https://github.com/systemjs/systemjs
 [5]: http://stackoverflow.com/questions/25416813/package-manager-bower-vs-jspm