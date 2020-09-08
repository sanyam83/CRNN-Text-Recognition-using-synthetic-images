# CRNN

## Text Recognition using CRNN with CTC loss

I have used CRNN with CTC loss for text recognition , required files present in crnn folder.

CRNN is a network that combines CNN and RNN to process images containing sequence information such as letters.

It is mainly used for OCR technology and has the following advantages.

End-to-end learning is possible.
Sequence data of arbitrary length can be processed because of LSTM which is free in size of input and output sequence.
There is no need for a detector or cropping technique to find each character one by one.
You can use CRNN for OCR, license plate recognition, text recognition, and so on. It depends on what data you are training.

I used a slightly modified version of the original CRNN model. (Input size : 100x30 -> 128x32 & more CNN Layer)

I have used VGG + Bidirectional LSTM layers

Text renderer is used for generating synthetic dataset (https://github.com/oh-my-ocr/text_renderer.git).

Read log.md to know about changes made in both the files.

### Run the Internship_Assignment.ipynb to get prediction and results.

Training accuracy and Loss -:

![alt text](https://github.com/sanyam83/sanyam_suri_9582061144-IITB-Assignment-Jul-Dec2020-Batch2/blob/train/download%20(1).png?raw=true)
![alt text](https://github.com/sanyam83/sanyam_suri_9582061144-IITB-Assignment-Jul-Dec2020-Batch2/blob/train/download.png?raw=true)
