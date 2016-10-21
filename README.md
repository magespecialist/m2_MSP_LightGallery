# Magento 2 LightGallery module

[![PHP version](https://badge.fury.io/ph/msp%2Flightgallery.svg)](https://badge.fury.io/ph/msp%2Flightgallery)

This module lets you use [LightGallery](https://github.com/sachinchoolur/lightGallery) with Magento 2 throught requirejs.

## Installation
```
composer require msp/lightGallery
bin/magento module:enable MSP_LightGallery
bin/magento setup:upgrade
```
## Usage
You must include the css via layout XML, for example if you want to use the gallery in the product page add to ```catalog_product_view.xml```:

    <head>
        ...
        <css src="MSP_LightGallery::css/lightgallery.min.css"/>
        ...
    </head>

You can init the gallery with `data-mage-init`:
```
<div id="your-gallery" data-mage-init='{
    "LightGallery": {
        "thumbnail":true
    }
}'>
    <a href="img/kitten1.jpg">
        <img src="img/kitten1-thumb.jpg" />
    </a>
    <a href="img/kitten2.jpg">
        <img src="img/kitten2-thumb.jpg" />
    </a>
    <a href="img/kitten3.jpg">
        <img src="img/kitten3-thumb.jpg" />
    </a>
</div>
```
or with a `<script type="text/x-magento-init">`:
```
<div id="your-gallery">
    <a href="img/kitten1.jpg">
        <img src="img/kitten1-thumb.jpg" />
    </a>
    <a href="img/kitten2.jpg">
        <img src="img/kitten2-thumb.jpg" />
    </a>
    <a href="img/kitten3.jpg">
        <img src="img/kitten3-thumb.jpg" />
    </a>
</div>
<script type="text/x-magento-init">
     {
         "#your-slider": {
             "LightGallery": {
                "thumbnail":true
             }
         }
     }
 </script>
```
