---
ID: 399
post_title: XAML ALT+letter to focus textbox
author: nitech
post_excerpt: ""
layout: post
permalink: >
  http://simonpedersen.no/2016/02/17/wpf-alt-plus-letter-to-focus-textbox/
published: true
post_date: 2016-02-17 10:43:48
---
If you want the user to be able to focus a specific field with an ALT+Key - eg. ALT+F, you can do it the following way: [code language="xml"]<Label Target="{Binding ElementName=Username}">Enter _Username:</Label> <TextBox Name="UserName" Text="{Binding Username, Mode=TwoWay, UpdateSourceTrigger=LostFocus}"> </TextBox>[/code] 
*   Target of Label associates it with the TextBox.
*   Underscore _Before a letter makes it accessible via the ALT+Key If you are from the Web World, you are used to associating labels with inputs via the ID-attribute. Target looks similar.