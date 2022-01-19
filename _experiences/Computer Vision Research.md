---
layout: experience
title: "Computer Vision Research"
categories: misc
location: "University of California, Irvine"
priority: "2"
excerpt: "Summer Undergraduate Research Fellowship conducting research on semi-supervised machine learning."
---
<figure>
    <img class="img-responsive" src="/assets/img/obj_detection_image.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Example of Object Detection</i></figcaption>
</figure>

The Summer Undergraduate Research Program is a research fellowship awarded to UCI students who participate in intensive summer research at UCI. I collaborated with another student to develop a research idea and write a proposal (<a href="https://docs.google.com/document/d/1aCVz-9pm7h563E9TA3dwUZpdooERTreSLzyK3a5oxlY/edit?usp=sharing" target="_blank">link</a>), which was ultimately selected for funding.

Our research centered around measuring the effectiveness of pseudolabeling, a semi-supervised machine learning technique that we applied to object detection. Object detection is the process of detecting and identifying objects in an image. We take in a raw image from a phone or camera, process it and output the location of certain objects within the image. This technology is used in numerous applications such as self-driving cars, medical imaging, and robotics.

<div class="row">
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/obj_detection_example_unlabeled.jpg" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="400" height="300"/>
    <figcaption style="text-align:center"><i>Input</i></figcaption>
    </figure>
  </div>
  <div class="column">
    <figure>
    <img class="img-responsive" src="/assets/img/obj_detection_example_labeled.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" width="400" height="300"/>
    <figcaption style="text-align:center"><i>Output</i></figcaption>
    </figure>
  </div>
</div>

Specifically, we studied pseudolabeling, a simple semi-supervised learning method. Most machine learning methods are reliant on a large training dataset that is labeled and formatted in a very particular manner. Thousands of images are required per object class, and labelling all of these images can take hundreds of hours. Services exist that will label images for you, but these can cost tens or hundreds of thousands of dollars. Semi-supervised learning methods attempt to exploit certain features of object detection to reduce the amount of manual labeling required. 

### **Semi-Supervised Learning**
Pseudolabeling is the process of using predictions the model makes to train itself. We feed images the model has never seen before through our software and allow it to make predictions about where objects are within the image. We then take the predictions the model is confident about, and treat these instances of detection as additional training data. These additional data will be used to retrain the model, increasing its accuracy.

<figure>
    <img class="img-responsive" src="/assets/img/pseudolabel_flowchart.png" alt="" style="display:block;float:none;margin-left:auto;margin-right:auto" />
    <figcaption style="text-align:center"><i>Pseudolabel Flowchart</i></figcaption>
</figure>

The primary advantage of using this method is that large amounts of unlabeled images can be used to benefit the model. Only the initial set of training data has to be labeled, and any subsequent data will be labeled by the model. It is important for this initial set of training data to be sufficient to give the model a good baseline, where it can make predictions with a reasonable accuracy.

This technique can be used effectively in situations where large amounts of unlabeled data can be collected. For example, a stationary wildlife camera in the forest or stills from a public video feed. Researchers and programmers that previously did not have access to large amounts of labeled data can use pseudolabeling to increase accessibility to object detection.
<style>

/* Create two equal columns that floats next to each other */
.column {
  float: left;
  width: 45%;
  padding: 10px;

}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
</style>