# Machine-Learning-EMG-hand-movements-Classifi-cation-system

1   Main Project Idea
It is required to build an EMG-based hand movements Classification system. The classifier is a 
binary classifier; meaning that we have  only 2 classes to decide between:  The required system 
needs to state  whether the patient is doing lateral or palmar motion based on some features in 
his/her EMG.
In such a classification problem, one passes through certain standard    steps:

• EMG data collection and labeling for training (Generate your ground truth).
• Extracting some features from the EMG signal to encode the information contained in the signal in 
a finite set of variables.
• Choose a classifier model to train it with the data you obtained.
• After training your classifier, you can use it to give you a decision on a new patient EMG 
whether the movement is lateral or palmar!.
• You also need to provide some metric to assess the performance of your classifier on unseen data 
(The generalization problem)

2    The Project Requirements
• Obtain the EMG annotated data from your dropbox in .mat format. In order to read .mat format in 
python, check scipy.io.loadmat
• Filtrate the acquired EMG signals to eliminate the AC noise [60 Hz] using a notch filter.
• Extract the following features from the EMG signal: [these features are known in the literature 
as being good features for the EMG signal in such kind of problem].
  xi2                                                        (1)
4thP ower =       xi4                                                            (2)
NonlinearEnergy =      −xixi−2 + xi−12                                                        (3)
CurveLength =      xi − xi−1                                                        (4)
• You will construct a Naive Bayes based classifier for EMG based movement classification.
• You will need to assume that all the used features in Naive Bayes model have Gaussian 
distribution (use pdf value as an estimate for the conditional probability) and you can estimate 
the mean and standard deviation of these distributions from the data [this is the training step].
• Test your system on new EMG data (don’t use the signals used in the training process).

Note:  I Did not  use the built in functions of Naive Bayes classifier in Python, but constructed my own 
  model.
