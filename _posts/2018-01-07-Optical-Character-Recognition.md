---
layout: post
title: Optical Character Recognizer
gh-repo: nikku1234/Optical-Character-Recogonizer
gh-badge: [star, fork, follow]
tags: [ocr]
image: /img/ocr/ocrlogo2.png

---
# Optical-Character-Recogonizer
To develop a system that can recognize handwritten characters from an image.

![](/img/ocr/ocr1.png)  

# OCR is a process of converting images of typed, handwritten or printed text into machine-editable text.

It is a common method of digitizing the handwritten characters and printed text in an image.A digit can be written in number of ways differing in shape and properties, such as tilt, stroke, cursivity and overall shape.Humans can easily recognize and read each digit. This is because the human perception processes the information by the features that define a digit’s shape in an overall fashion. Thus, while modelling the human perception model in machines an ANN can be applied for classification of characters.

*Artificial Neural Networks(ANN)is one of the best ways to build an OCR.

Artificial neural networks (ANNs)  are computing systems inspired by the biological neural networks that constitute human brains. Such systems "learn" (i.e. progressively improve performance on) tasks by considering examples.

# Dataset used: letter.data.gz
This dataset contains handwritten words dataset collected by Rob Kassel at MIT Spoken Language Systems Group.
The tab delimited data file contains a line for each letter, with its label, pixel values, and several additional fields listed in letter.names file. 
Fields
id: each letter is assigned a unique integer id
letter: a-z
next_id: id for next letter in the word, -1 if last letter
word_id: each word is assigned a unique integer id (not used) 
position: position of letter in the word (not used)
fold: 0-9 -- cross-validation fold
p_i_j: 0/1 -- value of pixel in row i, column j

# MODULE 1 – DIGIT RECOGNITION
![](/img/ocr/module1.png)
# DIGIT RECOGNITION
# Block Diagram
![](/img/ocr/module1block.png)

The dataset is imported. The matrix of each image in the dataset are stored in arrays. Then the image is taken as input. Pre-processing is done such that the image is converted to grey-scale image. Then the image is converted to array and is matched with the arrays of dataset. Thus, the digit is recognized.

# INPUT IMAGE
![](/img/ocr/module1input.png)

# OUTPUT
![](/img/ocr/outputocr1.png)

# MODULE 2 – ALPHABET RECOGNITION
![](/img/ocr/module2.png)

# ALPHABET RECOGNITION

# BLOCK DIAGRAM

This module matches the handwritten alphabets present in a dataset. This application takes a string as input and segments the string into separate alphabets. Matrix is formed for each alphabet. A feed forward neural network is created using neurolab. 
The feed forward neural network is trained with a part of the dataset and is tested with the alphabets present in the input. 
The neural network predicts the alphabets that matches the alphabets in the input string.

![](/img/ocr/module2block.png)

# OUTPUT

![](/img/ocr/ocr2out.png)

