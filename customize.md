In this article, I'm going to show you how to customize DayOne to look as a 
professional web site. Let's start by understanding the theme folder 
structures:

```
+-- dayone
    +-- images
    +-- public
    |   +-- main.css
    |   +-- css
    |   |   +-- ...
    |   +-- js
    |       +-- ...
    +-- theme
    |   +-- xxxx.html
    |   +-- xxxx.html
    |   +-- xxxx.html
    +-- WEB-INF
        +-- web.xml
        +-- web-servlet.xml
```

The most important folders for customization are the folder "public" and 
folder "theme". The folder "public" contains everything that user can access
publicly. By default, it starts with Bootstrap 4.x and follows by CSS from the
file "main.css".

Let's try to change the theme color from default to pink.


The folder "theme" contains only HTML files. The first 3 files that we will
going to explore are:
- header.html
- index.html
- footer.html

