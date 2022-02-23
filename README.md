# Hanger, changing the images in the showcase
Changing the images of the product in the certain showcase/place.
Example. Changing the all point of view / positions of clothing (or product) to show the users/customers on shopping website.

## Features
- No dependencies
- Easy setup
- Optional duration

## Installation
download assets/js/hanger.min.js and include the script on your page like shown below.

## Usage
Firstly, add your images array as the value of `data-images` attribute for the JS hook.

Use `$hanger()` as below and pass an element reference or a querySelector. For best performance include the script just before the closing \</body> element.

```HTML
<div class="YOUR-ITEM-CLASS" data-images='["PATH-OF-YOUR-IMAGE/YOUR-IMAGE-1.png", "PATH-OF-YOUR-IMAGE/YOUR-IMAGE-2.png", "PATH-OF-YOUR-IMAGE/YOUR-IMAGE-3.png"]'>
</div>

<script src="hanger.min.js"></script>
<script>
    $hanger({
        items: '.YOUR-ITEM-CLASS'
    });
</script>
```

The following options are available to pass to the adjustty method.
| Option        | Default           | Description  |
| ------------- |:-----------------:| -----:|
| duration       | 1000 miliseconds   | Default duration to change images |


You can pass the arguments for duration as below.

```javascript
$hanger({
    items: '.YOUR-ITEM-CLASS',
    duration: 1500
});
```

## Requirements
The CSS properties of selected element should have `transition-delay: 0s;transition-duration: 0.3s;transition-timing-function: ease-in-out;background-size: cover;background-repeat: no-repeat;background-position: center center;`. If not, the performance of adjustty may be slow by restyling the elements.
<br/>

You can simply apply as below:
```CSS
.YOUR-ITEM-CLASS {
    transition-delay: 0s;
    transition-duration: 0.3s;
    transition-timing-function: ease-in-out;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
}
```

## Version
1.0.0