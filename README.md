## Aleatory-aware Deep Uncertainty Quantification for Transfer Learning

### Steps During Training:
#### 1. Data Preparation: DICOM to RGB
#### 2. Transfer Learning on Data and Saving Fully-Connected(FC) Layer and Output Posterior
#### 3. Opacity Score Computation from Training Output Posteriors
#### 4. Opacity Score Distribution for Different Labels
#### 5. Opacity Score Computation NN Training for Computation Efficiency
#### 6. Training and Saving N-number of FC Layers for Each Pre-trained NN
#### 7. Training and Saving Opacity Score Computation NN for Each FC

### Steps During Execution:
#### 1. Data Preparation: DICOM to RGB
#### 2. Apply Pre-trained Portion of Model and Saving Features
#### 3. Apply Feature to N-number of FC Layers and Obtain N-number of Output Posteriors 
#### 4. Apply Output Posteriors to Opacity Score Computation NNs to Obtain Scores
#### 5. Discarding Extreme Samples and the Range Becomes Prediction Interval
#### 6. Median of Scores Indicate the Level of Aleatoric Uncertainty
