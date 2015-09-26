Easy Youtube Embed for Jekyll
==============

A plugin for Jekyll to easily embed Youtube videos into your site. Updated to support playlist embedding.

## Demo
[Jekyll Youtube Plugin](https://pibby.com/jekyll-youtube-plugin/)

## Installation Instructions
Download the file `youtube.rb` and place it in your `_plugins` folder of your Jekyll installation.

## Usage Instructions
In your Markdown post, simply include the following command:  
`{% youtube VIDEO_ID %}`

And for playlists (new as of September 25, 2015):
`{% youtube VIDEO_ID?list=PLAYLIST_ID %}`

For example, `{% youtube prFohBWIdQg %}` will render as:  
```html
<div class="video">
    <figure>
        <iframe width="640" height="480" src="//www.youtube.com/embed/prFohBWIdQg" frameborder="0" allowfullscreen></iframe>
    </figure>
</div>
```

A playlist example, `{% youtube yFTvbcNhEgc?list=RDyFTvbcNhEgc %}` will render as:

```html
<div class="video">
    <figure>
        <iframe width="640" height="480" src="//www.youtube.com/embed/yFTvbcNhEgc?list=RDyFTvbcNhEgc" frameborder="0" allowfullscreen></iframe>
    </figure>
</div>
```

---

If you're interested in the CSS, you can add it to your stylesheet and your videos will resize responsively for users on mobile devices.

```css
/* responsive videos */
.video figure {
	position: relative;
	nowhitespace: afterproperty;
	padding-bottom: 56.25%;
	height: 0;
	overflow: hidden;
}

.video iframe, .video object, .video embed {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
}
```
