# Machine Learning
Document
```bash

```

## Table of Content
* [Detectron](https://github.com/facebookresearch/Detectron)
* [DeepReinforcementLearning](https://github.com/AppliedDataSciencePartners/DeepReinforcementLearning)
* [Caire](https://github.com/esimov/caire)
* [Minigo](https://github.com/tensorflow/minigo)
* [AlphaPose](https://github.com/MVIG-SJTU/AlphaPose)
* [Person Blocker](https://github.com/minimaxir/person-blocker)
* [Annvisualizer](https://github.com/Prodicode/ann-visualizer)
* [Caffe64](https://github.com/dfouhey/caffe64)
* [Fast Pandas](https://github.com/mm-mansour/Fast-Pandas)
* [MLDB](https://mldb.ai/)

## Application
* Signal and Image Processing
* Handwritten text/digits recognition
* Natural Object Classification (Photo & Video)
* Segmentation
* Face Detection
* Recommender System
* Speech Recognition
* Natural Language Processing

## Goal
* Machine Learning
* Convolution Neural Network

## Convolution Neural Network (CNN)
เป็นส่วนหนึ่งในหัวข้อ Natural Object Classification โดยปกติสมองของมนุษย์เราเมื่อเห็นภาพผ่าน Retina เข้ามาก็จะถูกส่งมายังสมองส่วนต่าง ๆ ไปจนถึง Visual Cortex ทำให้เราเห็นเป็นรูปภาพหรือข้อความ

![](/Images/Hemisphere.png)

แนวคิดนี้จึงถูกนำมาสร้างเป็น High-Level Syntax Model เพื่อให้สามารถนำไปใช้งานได้จริง Convolution Neural Network ซึ่งจะประกอบไปด้วย
* Input Image           เป็นภาพต่าง ๆ
* Primitive Features    จะเป็นการวิเคราะห์ภาพจาก Oriented edges and Shapes
* Object Parts          ก็จะแบ่งเป็น Object เช่น หน้าต่าง, ประตู
* Object                เราก็จะสรุปได้ว่าเป็นรูปตึก

## Sequential Problem
เป็นการแก้ปัญหาของข้อมูลที่มีการเรียงลำดับ อย่างเช่น ลำดับเลขอนุกรม แต่เป้นข้อมูลที่มี Data Point ที่เป็นอิสระต่อกันหรือเป็นข้อมูลแบบ Time Series ซึ่งไม่สามารถ Handle ได้ด้วย Neural Network แบบเดิม เรามาดูวิะีการแก้ปัญหาของ Sequential Problem กันเลย ยกตัวอย่าง สภาพอากาศ วันนี้อุณหภูมิเท่าไหร่ แดดออกฝนตก ถ้าเป็น Traditional Neural Network แบบเดิมมันสามารถ Predict ได้อยู่แล้ว โดยใช้ Straightforward task สำหรับ Neural Network

![](/Images/Sequential-01.png)

![](/Images/Sequential-02.png)

## Recurrent Neural Network (RNN)
เป็นการแบ่งการทำ Image Processing จากรูปภาพใหญ่เป้นรูปภาพย่อย ๆ เพื่อนำไปวิเคราะห์ว่าส่วนนั้นเป็นรูปอะไร ส่วนใหญ่จะนำไปใช้กับ Image Captioning หรือสามารถนำไปใช้กับ Music Composing โดยเทรนจากไฟล์ MIDI

![https://cs.stanford.edu/people/karpathy/deepimagesent/](/Images/RNN-02.png) ![https://cs.stanford.edu/people/karpathy/deepimagesent/](/Images/RNN-03.png)

นอกจากนั้นยังสามารถนำไปประยุกต์ใช้กับ Language Model เพื่อทำนายรูปประโยค ซึ่งก็เป็นข้อมูลแบบ Sequential แต่สามารถเป็นคำอะไรก็ได้ไม่แน่นอน

![](/Images/NLM-02.png)

![](/Images/NLM-03.png)

## Approaches Train Neaural Network
วิธีการ Train จะถูกแบ่งออกเป็น 3 ประเภท ได้แก่
* Supervised Learning
* Reinforcement Learning
* Unsupervised Learning

#### Unsupervised Learning  
จะเป็นการจัดกลุ่มข้อมูล โดยอาศัย Algorithm ต่าง ๆ
* Pattern Recognition
* Data Clustering
* Object Recognition
* Feature Extraction
* Data Dimensionality Reduction

และยังขึ้นอยู่กับเทคนิคที่เลือกใช้
* Restricted Boltzmann Machine (RBM)    จะใช้ 2 Layer ในการหา Pattern ของข้อมูล โดยใช้ Reconstructing Input
* Autoencoders
* Self-Organizing Maps (SOM)
* Principle Component Analysis (PCA)
* K-Means

![](/Images/Unsupervised.png)

## Project
* Image Captioning Tensorflow
* Pix2Code

## Pix2Code
* DSL (Domain-Specific Language) ภาษาที่ใช้กับงานที่เฉพาะเจาะจง เช่น SQL, HTML, CSS ส่วน Java, C, C++ จะไม่เรียก DSL ตอนนี้ยังไม่สามารถจัดการเรื่อง text ได้อ้างอิงจากงานวิจัย เพื่อลดปริมาณ Token ใน Code ประกอบไปด้วย (Reserved Word, Operators, Identifiers, Constants, Separators)
* One-Hot Encoding การเข้ารหัสข้อมูลเป็น Binary 0 กับ 1 
* CNN (Convolutional Neural Network) เป็น Neural Network ประเภทหนึ่ง เก่งเรื่องทำนายภาพ
* LSTM (Long-Term Memory) เป็น Neural Network ประเภทหนึ่ง เก่งเรื่อง Predictive

## Ordinary Least Sqaure (OLS) Regression จาก Statement Model
* เป็น Linear Regression สมการเส้นตรง
* ใช้หา Model ที่เป็นตัวแทนกลุ่มข้อมูลที่เรามี
* ใช้ผลลัพธ์ทำนายข้อมูลใหม่

สมการ y = a + bx

## Credit
* [Neuroph Java Framework](https://www.ibm.com/developerworks/library/cc-artificial-neural-networks-neuroph-machine-learning/index.html)

## License
Codeinsane license.