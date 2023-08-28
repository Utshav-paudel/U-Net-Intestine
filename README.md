# U-Net-Intestine
This will show how U-net works to segment the image
U-Net is the model use to create image segmentation i.e Labelling each pixel of image
 * Encoding part : At first image is taken by conv_block() which downsamples the image by performing normal convolution and return next_block and skip_connections, where next_block is used by upcoming convolution that also downsamples and skip_connections is used by corresponding decoding block.
      ![](https://github.com/Utshav-paudel/300DaysOFMachineLearning-DeepLearning/blob/9a189ddc298de55a7b545b3b00176d19f65cc46c/images/day119%20U-net_encoding.png)
    * Decoding part : It takes previous layer as first parameter and skip connection as second paramter and  performs Transpose convolution to upscale the image and at last convolution the number of filters of convolution is equal to number of classses to be labeled.
    * ![](https://github.com/Utshav-paudel/300DaysOFMachineLearning-DeepLearning/blob/9a189ddc298de55a7b545b3b00176d19f65cc46c/images/day119%20U-net_decoding.png)
    * U-Net Model : It uses this encoding and decoding to create the segmenetation of image .
      ![](https://github.com/Utshav-paudel/300DaysOFMachineLearning-DeepLearning/blob/9a189ddc298de55a7b545b3b00176d19f65cc46c/images/day119%20U_net%20final%20model.png)
