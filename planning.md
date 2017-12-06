Planning:

<!-- Ideas: -->
-----------
Music - Band 1 page site {
  large hero images and spacings
  long scroll
  music dates - table
  releases
  videos
}

Magazine Publication {
  video header
  large article snippets with images
  gallery of issue covers
}

Record Label {
  header
  socialmedia links
  cart nav
  navigation
  search
  large hero carousel
  new releases gallery
  article snippets
  sidebar - preorders, sale, videos
  footer: site map, mailing list form
}

Journal{
  built wireframe1
  built scss structure
  added grid function
  researched flexbox
}

# Project Goals

Create a landing page for a record label, which displays text, images and video  content in mobile, tablet, and desktop views.

## Site Sections
* Navigation: contains site logo, primary navigation, secondary navigation, and social media links.

* Header: Hero image with text.

* Main Content: contains a gallery of images with text, such as for album covers for new releases.

* Secondary Content: container for other site content, such as a sidebar containing paragraph text, image, or image with text.

* Footer: container for site map as an unordered list, and a form for signing up for the label's email list.

## Wireframes:

## Site version 1:

Mobile:
* Navigation: Logo centered, secondary nav and social media links on either side. Hamburger menu opens to drop-down primary navigation.
* Header: Hero image is full width, without text
* Main Content: Image gallery is centered, with rows of 2 images.
* Secondary Content: Sidebar content is stacked on top of eachother at full width each.
* Footer: Site map links are on one line, with email sign up form on the line below.


Tablet and Desktop:
* Navigation: Logo centered secondary nav and social media links on either side. Primary navigation on next line.
* Header: Hero image is full page width, with featured text on top.
* Main Content: Image gallery is on the left side of the main content area, with rows of 4 images.
* Secondary Content: Sidebar content is stacked on top of eachother in the right side of the main content area.
* Footer: Site map links are in a column on the left, with email sign up form on the right.


## Site Version 2:

Mobile:
* Navigation: Logo centered, secondary nav and social media links on either side. Hamburger menu opens to drop-down primary navigation. Navigation is fixed to top of page when scrolling.
* Header: Hero image is full width, with fixed nav on top.
* Main Content: Primary content is stacked on top of eachother at full width each.
* Secondary Content: Secondary content displays one image per row, with an info paragraph alternating on the left and right between rows.
* Footer: Site map links are on one line, with email sign up form on the line below.

Tablet:
* Navigation: Logo centered, secondary nav and social media links on either side. Primary navigation on next line.  Navigation is fixed to top of page when scrolling.
* Header: Hero image is full width, with fixed nav on top.
* Main Content: Main content displays in a 2 column grid in between secondary content rows.
* Secondary Content: Secondary content displays in two rows, with image on one side and paragraph text inline. Rows sandwich the primary content.
* Footer: Site map links are on one line, with email sign up form on the line below.

Desktop:
* Navigation: Logo centered, secondary nav and social media links on either side. Primary navigation on next line.  Navigation is fixed to top of page when scrolling.
* Header: Hero image is full width, with fixed nav on top.
* Main Content: Main content displays in a 2 column grid in between secondary content rows.
* Secondary Content: First secondary content item is in top left of main content area, in line with two primary content items, with text on right and image on left. Second secondary content item is in bottom right of main content area, in line with two primary content items.
* Footer: Site map links are on one line, with email sign up form on the line below.

## Site Version 3:
Mobile:
* Navigation: Logo on the left side. Hamburger menu opens to drop-down primary navigation.
* Header: Hero image carousel, full page width. Displays multiple featured images. No text on hero image.
* Main Content: Primary content (images with heading and paragraph text) display 1 per line at full page width.
* Footer: Email sign up form on line above secondary navigation and social media links.

Tablet:
* Navigation: Logo on the left side. Hamburger menu opens to drop-down primary navigation.
* Header: Hero image carousel, full page width. Displays multiple featured images. Feature text on hero images.
* Main Content: Primary content (images with heading and paragraph text) display in a 3 column grid in the center of the page.
* Footer: Email sign up form on line above secondary navigation and social media links.

Desktop
* Navigation: Logo on the left side. Hamburger menu opens to drop-down primary navigation.
* Header: Hero image carousel, full page width. Displays multiple featured images. Feature text on hero images.
* Main Content: Primary content (images with heading and paragraph text) display in a 3 column grid in the center of the left side the page.
* Secondary Content: Email sign up form displays on right side of page next to 3 column grid, on the right.
* Footer: Email sign up for inline with secondary navigation and social media links.

## Using SASS to meet project goals:
| SASS use                                                                                                                                                                                                                                                                                | Description                                                                                                           | Implementation                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FOR loop                                                                                                                                                                                                                                                                                | Loops through index a set number of times, returning a result each time.                                              | Looping through a sequence of 12, to appends index to column class name and divides the width of the column by the number of the loop. We used this to create a 12 column grid layout. |
| Variable                                                                                                                                                                                                                                                                                | Stores a value that can be changed in one place to impact every place it was refrenced.                               | Store $breakpoint  variables to reference in media queries.                                                                                                                            |
| extend                                                                                                                                                                                                                                                                                  | Using @extend lets you share a set of CSS properties from one selector to another                                     | this can be used to extend some constant formatting throughout our project so that the sidebar/ secondary objects have matching formatting.                                            |
| & nested selectors                                                                                                                                                                                                                                                                      | SASS lets you select an element nested in the parent styling.                                                         | this is used in the nav class so far and can be used to keep the code dry throughout the rest of the project                                                                           |
| partials                                                                                                                                                                                                                                                                                | A partial is simply a Sass file named with a leading underscore. It is used to split up the scss files into modules   | We use partials to connect all of our subfolders together into our Main.scss file to be converted to css by sass                                                                       |
| @import                                                                                                                                                                                                                                                                                 | Used to import the partials into the other scss documents                                                             | we import all of our partials into the main.scss file                                                                                                                                  |
| % placeholder selector                                                                                                                                                                                                                                                                  | Placeholder selectors act like class selectors, but they do not show up in the generated css.                         | We used %clearfix with @extend to clear floats                                                                                                                                         |
| mixin push auto                                                                                                                                                                                                                                                                         | To quickly centre a block element without having to worry about if there is any top or bottom margin already applied. | this can be used to center our nav logos or other content in our project                                                                                                               |
| mixin Truncate @mixin truncate($truncation-boundary) {    max-width: $truncation-boundary;    white-space: nowrap;    overflow: hidden;    text-overflow: ellipsis;}                                                                                                                    | a mixin that can be called upon to easily wrap the text and content to the confines of the object                     | this can be used in our text content areas to assure everything will fit and move correctly with the screen                                                                            |
| @mixin responsive-ratio($x,$y, $pseudo: false) { $padding: unquote( ( $y / $x ) * 100 + '%' ); @if $pseudo { &:before { @include pseudo($pos: relative); width: 100%; padding-top: $padding; } } @else { padding-top: $padding; } }                                                     | responsive aspect ratio mixin that allows you to easily set a ratio for a video, image, or background-image           | this would be a useful tool in our project for out hero section if the website used a video to the hero.                                                                               |
| @mixin font-source-sans($size: false, $colour: false, $weight: false, $lh: false) { font-family: 'Source Sans Pro', Helvetica, Arial, sans-serif; @if $size { font-size: $size; } @if $colour { color: $colour; } @if $weight { font-weight: $weight; } @if $lh { line-height: $lh; } } | mixin allows you to set the font fall back settings for the entire page                                               | useful to the page to ensure the correct font settings are available for the possibles browsers                                                                                        |
| Collapsable Menu                                                                                                                                                                                                                                                                        | Using Media Queires and Css this will make for an easier view on mobile options                                       | this isnt a sass specific item but will be a new concept implemented in our project.                                                                                                   |
