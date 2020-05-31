# Images

## Controlling size of images in CSS
The height and width properties are used to set the height and width of an image.

The height and width properties do not include padding, borders, or margins. It sets the height/width of the area inside the padding, border, and margin of the image.

#### The height and width properties may have the following values:

  * auto - This is default. The browser calculates the height and width
  * length - Defines the height/width in px, cm etc.
  * % - Defines the height/width in percent of the containing block
  * initial - Sets the height/width to its default value
  * inherit - The height/width will be inherited from its parent value


## Aligning images in CSS

Rather than using the < img>
element's align attribute, web
page authors are increasingly
using the float property to align
images. The float property can be used
to move an element to the left or
the right of its containing block,
allowing text to flow around it.

#### Centering images Using CSS

In order to center an image, it
should be turned into a blocklevel element first, using the display
property with a value of block. Then  you can
use the use the margin property
and set the values of the left and
right margins to auto.

## Background Images

#### The background-image property:

Sets one or more background images for an element.
By default, a background-image is placed at the top-left corner of an element, and repeated both vertically and horizontally.

- CSS Syntax:
background-image: url|none|initial|inherit;

#### The background-repeat property: 

Sets if/how a background image will be repeated.

By default, a background-image is repeated both vertically and horizontally.

- CSS Syntax:
background-repeat: repeat|repeat-x|repeat-y|no-repeat|initial|inherit;

#### The background-position property:
Sets the starting position of a background image.

- CSS Syntax:
background-position: value;

#### The background-size property:
Specifies the size of the background images.

There are four different syntaxes you can use with this property: the keyword syntax ("auto", "cover" and "contain"), the one-value syntax (sets the width of the image (height becomes "auto"), the two-value syntax (first value: width of the image, second value: height), and the multiple background syntax (separated with comma).



# Practical Information

### Search Engine Optimization (SEO)

![img](https://www.jrtechnologiesweb.com/wp-content/uploads/2019/06/SEO.jpg)

SEO is an acronym that stands for search engine optimization, which is the process of optimizing your website to get organic, or un-paid, traffic from the search engine results page.

In other words, SEO involves making certain changes to your website design and content that make your site more attractive to a search engine. You do this in hopes that the search engine will display your website as a top result on the search engine results page.

In order to determine who comes first in the search results, search engines do not only look at what appears on your site. They also consider how many sites link to you (and how relevant those links are). For this reason, SEO is often split into two areas: on-page techniques and off-page
techniques.

* **on-page SEO** 

The **on-page SEO** factors are those elements that happen on your website. These are the things that you have complete control over, meaning that you can work to improve these factors over time by following best practices for SEO. This goes beyond just your content marketing to the deeper levels of your siteâ€™s HTML.

Here are just a few of the on-page SEO factors that can help you improve your search ranking:


   1. **Title Tag** â€“ The title tag on each page tells the search engines what your page is about. This should be 70 characters or less, including both the keyword your content focuses on and your business name.

   2. **Meta Description** â€“ The meta description on your website tells search engines a little bit more about what each page is about. This is also used by your human visitors to better understand what the page is about and if itâ€™s relevant. This should include your keyword and also provide enough details to tell the reader what the content is about.

   3. **Sub-headings** â€“ Not only do sub-headings make your content easier for visitors to read, but it can also help improve your SEO. You can use H1, H2, and H3 tags to help search engines better understand what your content is about.

   4. **Internal Links** â€“ Building internal links, or hyperlinks to other content on your site, can help search engines learn more about your site. For example, if you are writing a post about the value of a specific product or service, you can link to the product or service page in your blog post.

   5. **Image Name and ALT Tags** â€“ If you are using images on your website or within your blog content, you will also want to include your keyword or phrase in the image name and alt tag. This will help search engines better index your images, which may appear when users perform an image search for a certain keyword or phrase.

* **Off-Page SEO**

In addition to the on-page SEO elements that your organization has control over, there are also **off-page SEO** factors that can impact your ranking. Though you do not have direct control over these off-page factors, there are ways that you can improve your chances of having these factors work out in your favor. 

Here are a few of the different off-page SEO factors that can impact your search engine rankings:

  1. **Trust** â€“ Trust is becoming an increasingly important factor in a siteâ€™s Google ranking. This is how Google determines whether you have a legitimate site that visitors can trust. One of the best ways to improve trust is by building quality backlinks from sites that have authority.

  2. **Links** â€“ One of the most popular ways to build off-page SEO is through backlinks. You want to be careful here as spamming sites with your links is a quick and easy way to get your site banned from the search engines. Instead, take the time to build relationships with influencers and fans who create quality content and will link back to your site in their own content.

  3. **Social** â€“ Another important off-page SEO factor are social signals, such as likes and shares. When it comes to boosting SEO, you want to look for quality shares from influencers. The more quality content you publish, the more likely you will be to get people to share your content with others.


# Video and Audio APIs
### The HTML < video> Element

HTML5 comes with elements for embedding rich media in documents â€” < video> and < audio> â€” which in turn come with their own APIs for controlling playback, seeking, etc.  

To show a video in HTML, use the < video> element; for example:

                        < video width="320" height="240" controls>
                         < source src="movie.mp4" type="video/mp4">
                         < source src="movie.ogg" type="video/ogg">
                        < /video>

- The controls attribute adds video controls, like play, pause, and volume.

- It is a good idea to always include width and height attributes. If height and width are not set, the page might flicker while the video loads.

- The < source> element allows you to specify alternative video files which the browser may choose from. The browser will use the first recognized format.


### The HTML < audio> Element

To play an audio file in HTML, use the < audio> element:

Example:

                        < audio controls>
                          < source src="horse.ogg" type="audio/ogg">
                          < source src="horse.mp3" type="audio/mpeg">
                        </ audio>

- The controls attribute adds audio controls, like play, pause, and volume.

- The < source> element allows you to specify alternative audio files which the browser may choose from. The browser will use the first recognized format.

---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)
