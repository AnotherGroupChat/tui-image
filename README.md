# An image display widget for [tui-rs](https://github.com/fdehau/tui-rs)

This widget displays an image using ASCII art.

*Beware: This is work in progress and the API is very likely to change.*

There are currently two modes:

* Luma: Single color display using block intensity
* RGB: Relies on a RGB compatible terminal to show filled blocks with full RGB color.

You can either provide an image using `Image::with_img` which will be resized to fit in the container, or you can provide a function with `Image::with_img_fn` which receives the container size and returns an image of the correct dimensions.

At the moment it only accepts RGBA images and will halve the vertical resolution since terminal characters are roughly twice as high as wide.

## Options

* `block`: Use this block instead of filling the container
* `color_mode`: `ColorMode::Luma` or `ColorMode::Rgb`
* `alignment`: The horizontal alignment of the image within the container
* `style`: The Style used to composite the image against the background
