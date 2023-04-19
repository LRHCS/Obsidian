#jquery
## Adding jQuery to Your Web Pages

There are several ways to start using jQuery on your web site. You can:

-   Download the jQuery library from jQuery.com
-   Include jQuery from a CDN, like Google

---

## Downloading jQuery

There are two versions of jQuery available for downloading:

-   Production version - this is for your live website because it has been minified and compressed
-   Development version - this is for testing and development (uncompressed and readable code)

Both versions can be downloaded from [jQuery.com](http://jquery.com/download/).

The jQuery library is a single JavaScript file, and you reference it with the HTML `<script>` tag (notice that the `<script>` tag should be inside the `<head>` section):
```html
<head>  
<script src="jquery-3.5.1.min.js"></script>  
</head>
```
**Tip:** Place the downloaded file in the same directory as the pages where you wish to use it.  

---

## jQuery CDN

If you don't want to download and host jQuery yourself, you can include it from a CDN (Content Delivery Network).

Google is an example of someone who host jQuery:
```html
<head>  
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>  
</head>
```

