# Computer Vision

## Color Spaces
- **RGB**: Images are commonly represented using an RGB color space, in which each pixel can be is represented by combining the amount of red, green, and blue light coming from it. The more light that comes out, the lighter it is, and when the amount of each color of light emitted is equal and maximal, the result is white. Conversely, no light equates to black. _But, this can represent only 40% of the colors humans can percieve!_
- **XYZ**: Instead, we can represent images as follows: each pixel has an amount of red stimulation, luminance, and blue stimulation, corresponding to x, y, and z, respectively. We can convert from RGB to XYZ as via
  $$
    \begin{bmatrix} X \\ Y \\ Z \end{bmatrix} = \frac{1}{0.17697} \begin{bmatrix}  0.49 & 0.31 & 0.2 \\ 0.17697 & 0.8124 & 0.01063 \\ 0 & 0.01 & 0.99 \end{bmatrix} \begin{bmatrix} R \\ G \\ B \end{bmatrix}
  $$
  Interestingly, 
- 
