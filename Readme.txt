Requirements:

Torch
numpy
pandas

data_dir : Define the data directory path of images of all class labels

data_set : https://data.mendeley.com/datasets/fwcj7stb8r/1
 - a total of 3355 images

- For data tranformations Random rotation, Resized and cropping, Horizontal and vertical flips were performed 
for all the three splitted datasets - Training, Validation , Testing 

- The split of dataset is as follows

train_data = 80 % - 2684 images
valid_data = 10 % - 335 images
test_data = 10 % - 336 images

- From pytorch library we load the pretrained googlenet model and store it.

- The model architecture is summarized and same no of inputs layers is taken from the pretrained model and 
last linear layer of size 4 (4 class labels) is added along with the pretrained model

- Loss function : Cross Entropy losss
- Optimizer : SGD with lr of 0.001

- For model training, in each epoches, it computes predicted outputs by passing the input and calculates loss
gradient and CE loss,batch loss. The same is repeated in model validation.

- Model is trained for 50 epoches and tested
- Test loss : 0.233102
- Test accuracy : 90 %

