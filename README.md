[Orange Open Source](http://adobe.github.com)
=======================

Presenting [Orange Github Homepage v2.0](http://orange-opensource.github.com), the new central hub for **Orange Open sources** projects.

Allowing you to **search through Adobe Github repositories**, you can focus on what you are really passionate about.

- You are a *web developer*? Search the repositories only containing *Javascript* code, because it rocks!
- You love doing *technology watching*? Order by *Popularity*, by *Last Push* or select only the *5 stars (>1k followers)* projects to get the hottest repos!
- You are a *web designer* and want the perfect code editor? Search *brackets* and get all the repositories related to this awesome project!
- You are a *researcher*? Check out the project pushed in Open Source by the *Adobe Research* organization!

It was made with the help of adobe, see the original project from: https://github.com/adobe/adobe.github.com

## Architecture

Hummm... you want to learn more about how all this is structured? A good sketch is better than a long speech, so here is a little schema:

<p align="center"> <img src="https://raw.github.com/adobe/adobe.github.com/master/img/schema_adobe_open_source.png"  alt="Adobe Open Source schema" /></p>

The information is pulled directly from the [Github API](http://developer.github.com/v3/) and aggregated by a [NodeJS](http://nodejs.org) server (its code source is available [in this repository](https://github.com/Orange-OpenSource/server.adobe.github.com)). It is available through an simple REST API, thanks to [restify](http://mcavage.me/node-restify/).

[AngularJS](http://angularjs.org/) then makes a unique API call to the server and inject the data on your browser, based on the [Foundation](http://foundation.zurb.com/) CSS framework and using [dc.js](http://nickqizhu.github.io/dc.js/) for the graphs. The filtering engine for the repositories was built on top of Angular.

## For Orange employee

### Add a new org to the list

Edit the file [data/org.json](/data/org.json) inside this project.

### Add new featured project and org to see it in carousels

Edit the file [data/featured.json](/data/featured.json) inside this project.

### Change the backend target

Edit the line 18 in the file [js/script.js](js/script.js#L18) inside this project.