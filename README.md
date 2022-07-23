# NER_Tasks
## N2C2 2018 ADE and Medication Extraction Dataset
Follow the process of [N2C2_Medication_Token_Classification_BioMegatron.ipynb](N2C2_Medication_Token_Classification_BioMegatron.ipynb) to implement NER task for N2C2 dataset
### Rebuild steps, and intructions
#### 1. Environment Setting
  Follow the steps in environment setting section, and before building apex step, notices that we need to modify /apex/apex/transformer/tensor_parallel/layers.py line 340 and 343 ```.view()``` to ```.reshape``` and than run the next code to install the apex
#### 2. Task description
  Showed some information and data examples in this section
#### 3. Preprocessing Data
  Need to modify the MAIN_DIR to the path of your own directories with where you wanna save the task, and change ```n2c2_training = 'PATH_TO_BRAT_N2C2_DATA_FOLDER'``` with the original n2c2 dataset folder path.
  However, if you already have the NeMo input data you can skip the process, or if you have BIO files which in .tsv, you can jump to CONVERT BIO to NeMO format subsection
#### 4. Model Configuration
  Modify the hyperparameter in this section( Change epochs number, learning rate, batch size, etc.)
#### 5. Model Training
  Choose the pretrain models in the Setting up Pretrain Models section, and train the model in this section
#### 6. Inference
  Use ```model_ner.half().evaluate_from_file``` to inference and evaluate the model

## CHIA Dataset
Follow the process of [CHIA_Token_Classification-BioMegatron.ipynb](CHIA_Token_Classification-BioMegatron.ipynb) to implement NER task for CHIA dataset
### Rebuild steps, and intructions
#### 1. Environment Setting
  Follow the steps in environment setting section, and before building apex step, notices that we need to modify /apex/apex/transformer/tensor_parallel/layers.py line 340 and 343 ```.view()``` to ```.reshape``` and than run the next code to install the apex
#### 2. Task description
  Showed some information and data examples in this section
#### 3. Preprocessing Data
  Need to modify the MAIN_DIR to the path of your own directories with where you wanna save the task, and change ```chia_training = 'PATH_TO_BRAT_CHIA_DATA_FOLDER'``` with the original chia dataset folder path.(The processing process is different from N2C2)
  However, if you already have the NeMo input data you can skip the process, or if you have BIO files which in .tsv, you can jump to CONVERT BIO to NeMO format subsection
#### 4. Model Configuration
  Modify the hyperparameter in this section( Change epochs number, learning rate, batch size, etc.)
#### 5. Model Training
  Choose the pretrain models in the Setting up Pretrain Models section, and train the model in this section
#### 6. Inference
  Use ```model_ner.half().evaluate_from_file``` to inference and evaluate the model
