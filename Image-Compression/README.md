# Image Compressing

A notebook that compress a color input image with a custom JPEG method (with different coding step), and the transform being the DCT.

We first read the input, extracting information such as height, width and number of channels. Considering the possibility that the height and/or height are not multiples of the block size for the DCT (defined in this work as 8), we generate a new image that contains the original image, filling the remainder with 0's. Finally, we convert the image from the RGB color space to YCrCb, and perform a level shift of -128.

In the compression step, for each 8x8 block of the image, we apply the DCT to the block, divide it by the respective quantization matrix, traverse the block in zig-zag and perform a coding process of replacing a sequence of 0's by the number of 0's that occurred (similar to to the run length method). We save the result in a '.txt' file.

In the decompression step, we take the size of the image at the beginning of the compressed file, reconstruct the quantized image based on the encoding, and for each block, we traverse it in inverse zigzag, dequantize and apply the inverse-DCT. We end up performing a level shift of +128 (because of what we did initially), and converting the image back to the RGB color space. Finally, we show the compression rate and the PSNR.
