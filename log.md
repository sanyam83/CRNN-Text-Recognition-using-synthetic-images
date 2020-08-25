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

3. Notebook code is a bit unorganized , but will be in organized manner by tomorroq

