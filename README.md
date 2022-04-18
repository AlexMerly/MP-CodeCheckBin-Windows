Thank you for visiting Merly's MP-CodeCheck BETA GitHub repository! We are happy you are here! If you enjoy using MP-CodeCheck and find it useful, we would greatly appreciate your feedback. 

Please email us with any questions, comments, issues, or anything related to MP-CodeCheck to support@merly.ai or debugging@merly.ai. We would love to hear from you!

![merlydog_favicon](https://user-images.githubusercontent.com/92695077/163842195-66aabaa5-9db3-4499-8593-ae40fbef6e97.png)

# What is MP-CodeCheck?
MPCC is a self-supervised, iterative learning, anomaly detection system for code. MPCC was designed to learn good and bad code syntax, patterns, and semantics from a large corpora of existing code. Once trained, MPCC’s model can be used for a variety of tasks such as: (i) detecting potential anomalies in existing code,
(ii) grading the quality of an existing repository, and (iii) guiding programmers through the important aspects of an unfamiliar or updated code
repository, to name a few.

At its core, MPCC is a machine programming (MP) system that autonomously identifies anomalous logical expressions directly
in source code. These anomalous expressions, also known as anomalies, are often latent defects in the existing code that
programmers have failed to identify or correct. MPCC helps programmers find these anomalies and correct them, thereby
improving the overall quality of the existing software. For this limited release version of MPCC, we only include MPCC the
ability to perform inference (i.e., detect good or bad patterns) on code. In subsequent releases of MPCC, we may also include
the ability to train new models on other code bases, including users’ own proprietary ones.


## Setup Instructions
Prior to running inference and reviewing the results, let’s set up the environment. To run MPCC, you’ll need the following three
things (at a minimum):
1. A model trained on code (provided by Merly).
2. The MPCC executable (provided by Merly).
3. A code base to run inference against (provided by you, the user).

Please ensure you place both the MPCC model and the executable files in the same folder. Then, to simplify inference, we
recommend you place the code repository folder in the same directory as MPCC. Your setup is now complete!



## Launching MP-CodeCheck
Now that setup is complete, let’s launch MPCC to perform inference analysis. From the command line interface (CLI), type the
following (where ”[code base folder]” is a directory that contains the code you want to analyze):

*MPCC.exe infer -D [code base folder]*

When run successfully, MPCC will display information that looks similar to the following screen. This shows the progress of MPCC extracting the code DNA from the training data.

![TrainingScreen](https://user-images.githubusercontent.com/92695077/163841808-0721b703-4883-455d-8323-91759bc10c1e.png)

When MPCC has loaded its trained model and processed the code DNA, it begins inference analysis on all source code that
it finds in the files of the directory (or subdirectories) you have supplied when launching it. The image below shows an example of
MPCC’s inference progress in analyzing a code repository, how much work it has completed, and how much work is remaining.

![Inference](https://user-images.githubusercontent.com/92695077/163842630-a1778d96-12e5-4294-8639-40482fc8b0ea.png)

When inference analysis has completed, the Code View screen will appear (see image below), which will allow a user to
analyze the inference results as discussed in the next section.

<img width="705" alt="CodeView" src="https://user-images.githubusercontent.com/92695077/163842762-71dd7e1f-4f25-4be2-a59c-b51bec239480.png">



