Introduction 
When people are doing their own landscaping or gardening, they may notice different spots and patterns on their plants. 
These spots may correspond with different illnesses or problems with the plant, however there is not an easy way to diagnose the issue. We are creating a model that will be able to correctly identify the plant based off its leaves and align it with a specific issue. 

Initial Data 
The initial dataset contained 50,000 images. These images consisted of leaves of various plants and had matching labels. 

Data Cleaning 
There was not much cleaning that needed to be done to the images. 
Formatted the images to be a target size: 256x256. The images were then normalized as well. 

Model Creation 
Created a CNN to predict whether the leaf image corresponded with a certain label. 
Added a 3x3 convolutional layer with a RELU activation function and an input shape of 256 x 256 to correspond with the standardized image size. 
Next added another 3x3 64 convolutional layer with a RELU activation function. We next added a 2x2 pool layer with a dropout of .25. 
Then flattened the model. Added a dense function with a RELU activation function with a dropout of .5. 
Then added a final dense layer with a Soft max activation function. 

Used categorical cross entropy to calculate our loss function and Adam as our optimizer. 
Used an epoch of 20 and a batch size of 64, but it seemed to be over fitting the data. 
Tried a combination of different batch sizes and epoch sizes and determined that an epoch of 15 and batch size of 128 was the best for the model. 

Conclusion
For the result, had a validation accuracy of .8443. This indicates that the model built decently classified these images. 
20 epochs and batch size 64. 
