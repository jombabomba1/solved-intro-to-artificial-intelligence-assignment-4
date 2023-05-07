Download Link: https://assignmentchef.com/product/solved-intro-to-artificial-intelligence-assignment-4
<br>
<strong>General Instructions</strong>

<strong>Teams: </strong>Assignment can be completed by teams of two or three students. No additional credit for working individually.

<strong>Submission: </strong>Submit a PDF file to Sakai. For the programming questions, submit your code in a compressed file. DO NOT submit documents in <em>Word</em>, raw text, images, etc. One submission per team is enough. Be sure to submit before the deadline (see Sakai). You have unlimited submission, partial submissions are encourage! Code submitted must run on <em>ilab </em>machines in order to the be graded.

<strong>L<sup>A</sup>TEX: </strong>Extra credit (10%) for submitting answers using <em>L<sup>A</sup>TEX</em>. If you choose to do this, submit all files (*.tex) as a separate compressed file.

<strong>Plagiarism: </strong>Each team must implement and answer questions independently. Indicate any external sources used for your submission. If plagiarism is detected, the assignment will receive 0 points.

<strong>Project Description:</strong>

<strong>Acknowledgement: </strong>This project is based on the one created by Dan Klein and John DeNero that was given as part of the programming assignments of Berkeley’s CS188 course.

In this project, you will design three classifiers: a naive Bayes classifier, a perceptron classifier and a classifier of your choice. You will test your classifiers on two image data sets: a set of scanned handwritten digit images and a set of face images in which edges have already been detected. Even with simple features, your classifiers will be able to do quite well on these tasks when given enough training data.

Optical character recognition (OCR) is the task of extracting text from image sources. The first data set on which you will run your classifiers is a collection of handwritten numerical digits (09). This is a very commercially useful technology, similar to the technique used by the US post office to route mail by zip codes. There are systems that can perform with over 99% classification accuracy (see LeNet-5 for an example system in action).

Face detection is the task of localizing faces within video or still images. The faces can be at any location and vary in size. There are many applications for face detection, including human computer interaction and surveillance. You will attempt a simplified face detection task in

1

CS440: Intro to AI

which your system is presented with an image that has been pre-processed by an edge detection algorithm. The task is to determine whether the edge image is a face or not.

Please refer to <a href="http://inst.eecs.berkeley.edu/~cs188/sp11/projects/classification/classification.html">http://inst.eecs.berkeley.edu/~cs188/sp11/projects/classification/ </a><a href="http://inst.eecs.berkeley.edu/~cs188/sp11/projects/classification/classification.html">classification.html</a> for a brief description of the Perceptron and Naive Bayes classifiers.

Which are Faces? Which Digit?

Which Digit?                                                             Face or not face?

Figure 1: Examples of the data points in the data set.

<strong>What you should do:</strong>

<ol>

 <li>Implement three classification algorithms for detecting faces and classifying digits:

  <ul>

   <li>Perceptron</li>

   <li>Naive Bayes Classifier</li>

   <li>Any other algorithm of your choice (Neural Networks, Decision Trees, or any other you are interested in).</li>

  </ul></li>

 <li>Design the features for each of the three problems, and write a program for extracting the features from each image.</li>

 <li>Train the three algorithms on the part of the data set that is reserved for training. First, use only 10% of the data points that are reserved for training, then 20%, 30%, 40%, 50%, 60%, 70%, 80%, 90%, and finally 100%. All the results should a function of the number of data points used for training.</li>

 <li>Compare the performances of the three algorithms using the part of the data set that is reserved for testing, and report:

  <ul>

   <li>The time needed for training as a function of the number of data points used for training.</li>

   <li>The prediction error (and standard deviation) as a function of the number of data points used for training.</li>

  </ul></li>

 <li>Write a report describing the implemented algorithms and discussing the results and the learned lessons.</li>

</ol>

2/3

CS440: Intro to AI

<strong>Please keep in mind that:</strong>

<ul>

 <li>You can use existing libraries, but not for the learning algorithms. You should implement yourself the learning algorithms as well as the feature extraction.</li>

 <li>It’s OK to share ideas, but not code or writing.</li>

 <li>Part of your score will depend on the accuracy of the predictions made by your program.</li>

 <li>Your algorithm should not look at the testing data before the training is over. If you use any testing data point for training, that would be considered as cheating.</li>

</ul>

<strong>Additional information:</strong>

<ul>

 <li>You are allowed to use any external resources you like, including the code on the Berkeley page. The only things you need to implement are the core operations of Naive Bayes and Perceptron (probabilistic calculation and weight updates).</li>

 <li>How will you be graded? a) Show the TAs that you correctly implemented and understood Naive Bayes and Perceptron, b) Show that the code runs without issues (reads an image from the test data file, and returns a predicted label), c) Write a short report describing what you did, how the different algorithms performed (time and accuracy), and how did they improve as you used more and more of the training data (10%, 20%, …, 100%).</li>

 <li>There is no standard definition of “good enough” here. Typically, if you have less than 70% accuracy even when you use 100% of your training data then that means that you could do a better job on the features or that something was wrong. Once you hit that barrier of 70%, don’t spend more time on the algorithm.</li>

 <li>It’s OK if you have a bad performance (less than 70%) on a single type of data and algorithm. Example: everything is above 70% except Naive Bayes on Digits.</li>

 <li>Regarding the features, don’t spend too much time on designing complicated features that require a lot of coding. You would be surprised that the simplest features could be great predictors. For instance, you could just use the pixels directly as features (i.e. one binary feature per pixel in the image). You could also just divide the image into a regular grid (say 10×10). Each square in the grid defines a binary feature that indicates whether there is anything marked inside the square.</li>

 <li>How to compute the average prediction error (or accuracy) and its standard deviation? What we want is a metric for how consistent our prediction accuracy will be if we use a certain number of training points. Thus, we need to vary which training points are used and see the spread of results. The following pseudocode would accomplish this:</li>

</ul>

For i=1:5 (you can use more iterations, if time permits)

Train on 10% of randomly selected data points

Test on test data and save the accuracy in acc[i]

End

Return mean(acc) and std(acc).

Repeat the same for 20%, 30%, etc.

You may find the random module in Python to be especially convenient in choosing your random samples. Please let us know if you have any questions.

3/3