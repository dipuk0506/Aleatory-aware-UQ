# Aleatory-aware Deep Uncertainty Quantification for Transfer Learning

## Abstract
Without uncertainty quantification (UQ), the user does not have any idea about the credibility of outcomes from deep neural networks (DNN). However, current Deep UQ classification models capture mostly epistemic uncertainty. Therefore, this paper aims to propose an aleatory-aware Deep UQ method for classification problems. First, we train DNNs through transfer learning and collect numeric output posteriors for all training samples instead of logical outputs. Then we determine the probability of happening a certain class from K-nearest output posteriors of the same DNN in training samples. We name this probability as opacity score, as the paper focuses on the detection of opacity on X-ray images. That score reflects the level of aleatory on the sample. When the NN is certain on the classification of the sample, the probability of happening a class becomes much higher than the probabilities of others. Probabilities for different classes become close to each other for a highly uncertain classification outcome. To capture the epistemic uncertainty, we train multiple DNNs with different random initializations, model selection, and augmentations to observe the effect of these training parameters on prediction and uncertainty. During the test, for computation efficiency, we first obtain features from the pre-trained NN. Then we apply features to the ensemble of fully connected layers to get the distribution of opacity score. We also train several ResNet and DenseNet DNNs to observe the effect of model selection on prediction and uncertainty. The paper also demonstrates a patient referral framework based on the proposed uncertainty quantification. The scripts of the proposed method are available at the following link: https://github.com/dipuk0506/Aleatory-aware-UQ

###

<img src="https://github.com/dipuk0506/Aleatory-aware-UQ/blob/main/Opacity%20Score%20NN/TL_FC_Score.png" width="1000">
Figure : Transfer learning with ensembling of fully-connected layers for both aleatory and epistemic-aware uncertainty quantification. 

## Steps During Training:
#### 1. Data Preparation: DICOM to RGB
#### 2. Transfer Learning on Data and Saving Fully-Connected(FC) Layer and Output Posterior
#### 3. Opacity Score Computation from Training Output Posteriors
#### 4. Opacity Score Distribution for Different Labels
#### 5. Opacity Score Computation NN Training for Computation Efficiency
#### 6. Training and Saving N-number of FC Layers for Each Pre-trained NN
#### 7. Training and Saving Opacity Score Computation NN for Each FC



## Steps During Execution:
#### 1. Data Preparation: DICOM to RGB
#### 2. Apply Pre-trained Portion of Model and Saving Features
#### 3. Apply Features to N-number of FC Layers and Obtain N-number of Output Posteriors 
#### 4. Apply Output Posteriors to Opacity Score Computation NNs to Obtain Scores
#### 5. Discarding Extreme Samples and the Range Becomes Prediction Interval
#### 6. Median of Scores Indicate the Level of Aleatoric Uncertainty and Model Selection Uncertainty


Individual folders have separate readme files.

## Citation:


@article{kabir2022aleatory,

  title={Aleatory-aware deep uncertainty quantification for transfer learning},
  
  author={Kabir, HM Dipu and Khanam, Sadia and Khozeimeh, Fahime and Khosravi, Abbas and Mondal, Subrota Kumar and Nahavandi, Saeid and Acharya, U Rajendra},
  
  journal={Computers in Biology and Medicine},
  
  pages={105246},
  
  year={2022},
  
  publisher={Elsevier}
  
}
