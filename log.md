# Day 1
I spend the day figuring out the problem and approach to take for the problem .Also, made some changes in text renderer taken from https://github.com/oh-my-ocr/text_renderer.git
1. Changed cn.txt in [text_renderer-master/example_data/char](text_renderer-master/example_data/char)
2. Edited chn_text.txt and enum_text.txt files 

The reason for above was to reduce the time of working that is instead of editing whole code for english and remove chinese text , I replaced all chinese text file content to english.

# Day 2
Figured out how to create TFRecord still has some work left to do. 
Uploaded the notebook in whcih various operations are being held 

# Day 3
1. Edited main.py in text_renderer to generate images in sequential manner as previously after every 2000 images index starts from zero.

  So used pickle to dump count when the program closes and load the last dumped count value to continue the index.
  See master branch notebook for previous and tfrecord branch notebook for after using pickle and effect on dataset.

2. Generated tfrecord file containing image , image name, size and label as features.
   Check training dataset variable at the end of notebook.

3. Notebook code is a bit unorganized , but will be in organized manner by tomorrow

# Day 4 
1. Faced Challanges in decoding tfrecord file , still need some more time.(I have less experience in tfrecord file)

2. Figured out the model of ctc based CRNN . Also figured out type of input required for the model.(thats why decoding tfrecord file in required format is challenging).

3. Also edited text_renderer file according to allowed characters i.e. A-Z,0-9.

# Day 5
1. Created a crnn model using VGG CNN and Bi-LSTM networks code taken from - https://github.com/qjadud1994/CRNN-Keras.git

2. Edited Image_generator.py -:
  
    i) Addded function to read image files from multiple directories.
  
    ii) Edited the function to read labels from the dataframe passed (instead of image name)

3. Edited Parameter.py - according to maximum allowed length and range of characters allowed.

4. Also, model worked well

Refer to master brach to compare changes.

# Day 6-7

1. Trained model with 100 epochs with batch size of 128 .
2. got loss of 0.6 
3. Trained model for another 100 epochs with same batch size.
4. Got loss of 0.26 , loss does not go lower than 0.26
