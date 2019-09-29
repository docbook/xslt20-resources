# DocBook XSLT 2.0 Resources

These are resources (CSS, JavaScript, images, etc.) used by the
[XSLT 2.0 stylesheets](https://github.com/docbook/xslt20-stylesheets).

Releases are published on [the DocBook CDN](http://cdn.docbook.org/).

Share and enjoy.

## Brief summary

There are three sets of resources: `base` resources, used by all
documents. `publishers` resources for the Publishers customization
layer, and `slides` for the Slides customization layer.

### Base resources

The `base` resources include `css`, `img`, `js`, and `xml` resources.

* CSS:

    * [normalize.css](https://github.com/necolas/normalize.css) and
      [prism.css](https://prismjs.com/) are third-party libraries.
    * `default.css` contains the default formatting for HTML generated
      from DocBook. It includes `normalize.css`.
    * `db-prism.css` includes and extends `prism.css`. This handles the
      case where you’re using Prism JavaScript to do syntax highlighting.
    * `db-noprism.css` styles verbatim environments where Prism isn’t
      being used.
    * `paged-media.css` adapts the styling for paged media. It includes
      `default.css` and `db-noprism.css`.
    * `paged-bw.css` adapts `paged-media.css` for black-and-white output.
      It includes `paged-media.css`.
    * `paged-color.css` exists only as an alternative to `paged-bw.css`.
      It does nothing more than include `paged-media.css`.

    For HTML output, you should link to `default.css` and either `db-prism.css`
    or `db-noprism.css` depending on whether or not you want to use JavaScript
    syntax highlighting.

    For paged media, you should use `paged-media.css` or
    `paged-bw.css`, if you want only black-and-white output.

* IMG:

    Contains a variety of default images:

    * Callout numbers ![1](blob/master/base/img/1.png), ![2](blob/master/base/img/1.png), etc.
    * Admonitions ![Note](blob/master/base/img/note.png), ![Caution](blob/master/base/img/caution.png), etc.
    * Navigation images ![Next](blob/master/base/img/next.gif), ![Next](blob/master/base/img/next.png), etc.
    * ToC controls ![Plus](blob/master/base/img/toc-plus.png), ![Minus](blob/master/base/img/toc-minus.png), etc.
    * Annotation controls ![Open](blob/master/base/img/annot-open.png), ![Close](blob/master/base/img/annot-close.png), etc.
    * A “draft” image suitable for watermarking draft documents.

    And a few other odds-and-ends.

* JS:

    * `dbmodnizr.js` a third party library of polyfills.
    * `prism.js` the third party syntax highlighter
    * `annotations.js` a library to support annotations (somewhat crudely)
    * `nhrefs.js` a library to support multi-ended links (also somewhat crudely)

* XML:

    * An empty `$bibliography.collection` document
    * An empty `$glossary.collection` document

### Publishers resources

The `publishers` resources consist entirely of a single CSS file that
adds styling for some of the new elements in the Publishers extension.

### Slides resources

The `slides` resources include `css`, `img`, and `js` resources.

* CSS:

    * `slides.css`, additional styling for slides.

* IMG:

    * Header and footer images and some alternate navigation elements.

* JS:

    * `slides.js` supports navigation around the slide deck
