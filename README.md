# Attendance-System-using-Face-Recognition

## Table of Content
  * [Demo](#demo)
  * [Synopsis](#synopsis)
  * [Appendix](#appendix)
  * [Directory Tree](#directory_tree)
  * [Color Reference](#color_reference)
  * [Features](#features)
  * [Run Locally](#run_locally)
  * [License](#license)
  * [Technology Used](#technology_used)

## Demo

![](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/Result%20images/Result%202%20navaneeth.jpeg)
![](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/Result%20images/Excel%20Result.png)

## Synopsis

A mini project that I completed in 2021 that is used to record attendance using the faces of the class students. So, essentially, due to the pandemic, our class lectures were taught online in 2021, and as a result, much of the teaching time was spent on attendance. I considered using a computer vision model to take attendance in the class, so that there would be less time spent on attendance and the model would keep a record of attendees in an excel sheet.

So, Let’s dive deep into the technical side of the project, basically, according to online class, the attendance can be taken by two ways:

1. Using a screenshot of all the students, present in a single frame.
2. By providing the link to screen, where the class is being held and taking a snapshot of the class students that are present.

So, based on this, my project is done in both the ways, which recognizing the faces based on a single picture, and also recognizing the face of the students using the live feed link.

Let’s first talk about the implementation of the project for a screenshot, import the basic libraries that are required, then make a folder of images that consist of all the student faces in different dimensions, once that is done, then capture the encodings of all the faces, don’t forget to save the folder name as same as the student’s name.

Once your data has been prepared then, use the face_recognition module, to import the face encodings of all the students, then store the encodings in a list along with the folder name that is the name of the student in a separate list, once all the face encodings have been collected then dump it as a file, so that you can able to use those encodings for later use.

Now comes the recognition part, import the required and first open the class screenshot using the imread function, then do some preprocessing on the image, by changing the default image into gray-scale and then detect the faces in the image using the haarcascase_frontaface_default.xml file.

With the faces that are detected by the model, now, try to find if any of the face encodings matches with the encoding that we have stored in a file, and if it matches then print a bounding box over the face image of the student, and print the name of the student below the bounding box, the name of the student is obtained by the name of the folder, in which we have stored all the particular student images.

Also, print the name of the student in a excel sheet, with the time he had attended the class, and the name of the excel workbook will be the date and time on which the class has happened, this is how my AI engine tries to make attendance for the students.

In case of the second implementation using live feed, just paste the link instead of the image to the cv2.VideoCapture function, then the video will be available, just capture the different frame of images and then do the necessary preprocessing to find if any face available in the frame of images, once if any face are found then get the face encodings, and match it with our available encodings, then repeat the same procedure until you export a excel sheet of your students attendance.

## Appendix

The development of the model is present in the [opencv.ipynb](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/opencv.ipynb) file.

The dataset for the model i.e the students images are present in [Pictures](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/tree/main/Pictures) folder.

The face encodings of all the students are made in the [face_enc](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/face_enc) file.

The results for the AI engine or the excel attendance sheet is located in the [27-10-2021 CSE (AI & ML).xlsx](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/27-10-2021%20CSE%20(AI%20%26%20ML).xlsx) file.
 
## Directory Tree <a name='directory_tree'></a>

```
├── Pictures
│   ├── Ananth
        ├── Ananth 1.jpeg
        ├── Ananth 2.jpeg
        ├── Ananth 3.jpeg
        ├── Ananth 4.jpeg
    ├── Navaneeth
        ├── Navaneeth 1.jpeg
        ├── Navaneeth 2.jpeg
    ├── Veda
        ├── Veda 1.jpg
        ├── Veda 2.jpg
        ├── Veda 3.jpg
        ├── Veda 4.jpg
├── Result images
│   ├── Excel Result.png
    ├── Result 1 ananth.jpeg
    ├── Result 2 navaneeth.jpeg
    ├── Result Unkown.jpeg    
├── 27-10-2021 CSE (AI & ML).xlsx
├── README.md
├── LICENSE
├── datafile.txt
├── face_enc
|── haarcascade_frontalface_default.xml
├── opencv.ipynb
```
 
## Color Reference <a name='color_reference'></a>

| Color                    | Hex                                                                  |
| -------------------------| ---------------------------------------------------------------------|
| Bounding box and name    | ![#00ff00](https://via.placeholder.com/15/00ff00/00ff00.png) #00ff00 |



## Features

- Live prediction analysis.
- Fullscreen mode supports in mobile, pc.
- Used to predict for both pictures and videos.
- Can support links too.

## Run Locally <a name='run_locally'></a>

Clone the project

```bash
  git clone https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition.git
```

Install dependencies

```bash
  pip install opencv
  pip install face-recognition
```

Start the server

```bash
  python opencv.ipynb
```

Run the app on server by the local link provided


## License

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/Vedakeerthi/Attendance-System-using-Face-Recognition/blob/main/LICENSE)

## Technology Used <a name='technology_used'></a>

<a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> &nbsp;
<a href="https://opencv.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/> </a> &nbsp;
<a href='https://pypi.org/project/face-recognition/' target="_blank" rel="noreferrer"><img src="https://upload.vectorlogo.zone/logos/pypi/images/329bd0f1-2f74-44ca-bb75-a02e685e4a16.svg" alt="face_recognition" width="40" height="40"> </a> &nbsp;
