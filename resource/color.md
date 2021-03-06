# Color
>Spring 2017 | Geography 472/572 | Geovisualization: Geovisual Analytics
>
>Instructor: Bo Zhao, zhao2@oregonstate.edu | Office Hours: 3-4pm T or by appointment @ strand 347
>
>TA: Kyle R. Hogrefe, hogrefek@oregonstate.edu| Office Hours: 1-2pm MF @ WLKN 257 and 2-4pm W @ WLKN 210

## Lab

Lab (or CIE 1976 (L*, a*, b*), or CIELAB) is **a colour space that is designed for the human eye.** It is perceptually uniform, which means that the difference between two colour values correlates with the perceived degree of difference between the two colours (the difference between colours is measured by their Euclidean distance). Therefore, gradients between two colours using the Lab colour space will change very uniformly between the colours. L is the lightness of the colour, a is the position between green (negative values) and red/magenta (positive values), and b is the position between blue (negative values) and yellow (positive values). The idea is that colours cannot be both green and red, or blue and yellow, and that colours can be described by a combination of their green/redness and blue/yellowness, and the lightness.

Lab can describe all colours that the human eye can perceive, but also many beyond what can exist in the physical world (not to mention that computer displays can display a limited subset of real colours). One of the difficulties of Lab is that the valid ranges of L, a and b vary depending on the values of the other two values. L can be between 0 and 100, and a and b are normally within the range of -100 to 100, although a pure sRGB blue has a b of -108.

## Lch

Lch (or CIELCH) is a cylindrical version of Lab, which means that the two opponent colour dimensions (a and b) are represented by a hue, h, and chroma, c (if a and b are Cartesian coordinates, h and c are polar coordinates). Gradients interpolated in the Lch colour space will transition between hues, so a gradient between yellow and blue (opposing colours in Lab) will transition via green (or red/magenta) in Lch, but via grey in Lab.

## RGB

RGB is designed for screens, where colours are generated by individual red, green and blue elements. The actual colour of RGB colours depends on the device being used, although the sRGB colour space exists as a standardised colour space that the web nominally uses, and all RGB colours here are treated as sRGB. RGB values are easy to work with mathematically (they're all values between 0 and 255), and all colours on this page end up being converted to RGB values to be displayed, but they suffer from the problem of not being perceptually uniform nor intuitive to work with (it's hard to imagine what sort of colour you have just from RGB values, and it's also hard to modify colours intuitively with RGB).

## HSV and HSL

HSV and HSL are cylindrical versions of RGB, which are intended to be much more intuitive to use. HSV colours are represented by hue, saturation and value, while HSL colours are represented by, hue, saturation and lightness, except with different definitions of saturation. In HSL, a colour of maximum lightness will always be white, regardless of hue and saturation, while in HSV, a colour of maximum value will be the most intense colour given the hue and saturation (so pure red is a red hue with maximum saturation and value).

HSV and HSL suffer from RGB's lack of perceptual uniformity, so changing one dimension can result in apparent changes in other dimensions. For example, pure green and pure blue have the same saturation and lightness/value, but green appears to be a much lighter colour. Gradients interpolated in the HSV or HSL colour space are particularly prone to problems with this when they shift between many different hues. The is the problem that Lab and Lch overcome.

## Reference:

[1] http://davidjohnstone.net/pages/lch-lab-colour-gradient-picker
