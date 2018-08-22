# OCMOD remove 'Compare this Product'

Remove 'Compare this Product' buttons and links from OpenCart 3.x template. This modification is applicable for default OpenCart template. Probably will work also for other tepmlates based on default template. For removal is used OCmod modification system, which can be easly installed.

## Install

1. Download remove-compare-button-1-0-1.ocmod.zip modification package from this repozitory
2. In OpenCart admin go to Extension -> Install -> Upload and install downloaded modification package
3. Go to Extensions -> Modifications, you should see an entry 'Remove compare buttons and links from template'
4. Click on the Refresh button (top right of the page)

## CSS edit

Modification can make small glitch in CSS. Default template has at product thumb box 3 buttons and now we removed one. *Wishlist* button is moved next to *Add to cart* button and remain blank space next to *Wishlist* button. Fix is easy, edit `catalog/view/theme/default/stylesheet/stylesheet.css` and find element `.product-thumb .button-group button` and change **width** properties to value **80%**. Whole element can look like this:

~~~css
.product-thumb .button-group button {
        width: 80%;
        border: none;
        display: inline-block;
        float: left;
        background-color: #eee;
        color: #888;
        line-height: 38px;
        font-weight: bold;
        text-align: center;
        text-transform: uppercase;
}
~~~
