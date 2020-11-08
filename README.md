# DeepFake Detection using Deep Learning Methods for Synthesized Videos
Note: This is the thesis code for LJMU's degree of Master of Science in Machine Learning & Artificial Intelligence

**What do you mean by DeepFakes?**: ‘DeepFakes’ have gained massive popularity since it’s origin in 2017, from a Reddit user who developed a deep learning model to impose celebrity faces on pornographic videos. Since then the definition of DeepFakes has broadened to include any manipulation or doctoring of media such as image/video/sound with the help of deep learning techniques and artificial intelligence.

**Types of DeepFakes**: Category of DeepFakes can be divided into:
1. FaceSwap
2. Facial Reenactment
3. Attribute Manipulation
4. Computer Generated Faces

**Concerns posed by DeepFakes**: For the race that believes in what they see, DeepFakes pose a risk to the concept of truth and reality. With the improved quality of DeepFakes, it is increasingly harder to detect between DeepFakes and real content. These can be used to spread disinformation, propaganda, for revenge pornography and deceit. 

**Aims and Objectives of the Thesis**:
* To develop a generalized multi-class detection model by leveraging transfer learning
and DeepFake Model architecture
* To explore an approach to control the spread of disinformation on social media
* To demonstrate the model implementation and evaluate the two pronged approach

**Approach**: The thesis aims to use transfer learning and feature extraction for improved generalizability and classification of DeepFakes. The model flow and structure is seen in the image below
![Alt text](https://github.com/zeel97/DeepFakeDetection/blob/main/Model_Structure.png)

**Code and File Breakdown of the GitHub repo**
1. Data Analysis: the file creates a dataframe with the video properties of the FaceForensics++ dataset. Priliminary analysis of the dataset is performed in this file
2. PreProcess: the file performs the data preparation and processing steps. It concludes: file naming and moving to the planned folder structure and performs frame extraction, face cropping and adding of Gaussian noise
3. Models: the model folders are divided based on the feature exctractor used. Therefore it is divided into
- Base Model: the folder consists of the base CNN model and the best binary and mutli-class model weights
- ResNet: the folder consists of the python notebooks for the different classifiers built on the ResNet50 feature extractor (SVM, CNN and Random Forest)
- VGGNet: the folder consists of the python notebooks for the different classifiers built on the VGG16 feature extractor (SVM, CNN and Random Forest)
- FirstOrderMode: the folder consists of the python notebooks for the different classifiers built on the First Order Motion feature extractor. In this case files are divided for CNN and a single file for SVM and Random Forest classifier
4. Evaluation: The folder consists of 
- a pre-process file that extracts the single frames from the video from the Celeb-DF test set. It performs the other pre-processing steps before moving on to model testing.
- Eval_Model: this tests the best CNN model for VGG16 and ResNet50 feature extractors. 
- Eval_Model-FirstOrder: this evaluates the FirstOrderMotion CNN model for the Celeb-DF dataset

**Model Weights**: the pickle and hdf5 files of the different models can be accessed from the [Google Drive Link](https://drive.google.com/drive/folders/1c-hF_B-50AeZKsslMesVCFDWBnIQ1UkB?usp=sharing)
