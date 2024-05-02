# SafeGuardHer Design Document
## Introduction

### Background

Women's safety and security in public spaces, particularly when using public transportation or ride-sharing services, is a pressing and enduring concern. Instances of harassment, assault, and intimidation are distressingly common, and the need for an effective and accessible safety solution is paramount. Traditional methods of ensuring personal security often fall short, leaving women vulnerable and anxious about their well-being while commuting or traveling.
Current safety measures, such as emergency hotlines and self-defense training, offer limited reassurance and may not be readily accessible or effective in high-stress situations. Additionally, the rapid pace of urbanization and increased reliance on digital platforms for transportation have created new safety challenges that demand innovative solutions.
In light of these challenges, our project aims to address the critical issue of women's safety by introducing "SafeGuardHER," a cross-platform mobile application designed to empower and protect women during their journeys. SafeGuardHER leverages advanced audio analysis and machine learning technologies to detect potential threats and trigger swift emergency responses.
The problem at hand is clear: women need a proactive and accessible safety solution that can adapt to the modern urban landscape and the digital age. SafeGuardHER seeks to fill this gap by offering a comprehensive and user-friendly platform that leverages advanced technology to enhance women's safety and security, ultimately contributing to a safer and more inclusive society.

### Terminology
#### Definitions

| Term                        | Definition                                                                                     |
| --------------------------- | ---------------------------------------------------------------------------------------------- |
| Scream Detection Model      | A machine learning model, utilizing the Yamnet Model, designed to identify instances of screams or high-pitched vocalizations in audio data. |
| Hate Speech Detection Model | A machine learning model, utilizing BERT, trained to detect hate speech and offensive language in text data. |
| Speaker Identification Model| A machine learning model, utilizing Convolutional Neural Networks that trains itself on the user’s voice and performs binary classification verifying if the user is speaking or someone else. |
| Ensemble Modeling           | A technique that combines multiple models to improve predictive performance by aggregating their outputs. |
| Voice Activation            | A feature allowing users to trigger app actions or alerts by speaking predefined keywords, such as "Safeguard help me." |
| Speech Recognition         | The technology that converts spoken language into text or digital commands, enabling voice-activated features and interactions. |

#### Acronyms and Abbreviations

| Acronym/ Abbreviation | Meaning                   |
| ---------------------- | ------------------------- |
| ML                     | Machine Learning          |
| UI                     | User Interface            |
| UX                     | User Experience           |
| iOS                    | iPhone Operating System   |
| ERD                    | Entity Relationship Diagram |
| SOS                    | Modern-day slang to communicate discomfort or urgency |
| CNN                    | Convolutional Neural Networks |
| I/O                    | Input output              |

### Functional Requirements
    1. User Registration and Account Management: User sets up a personal profile where they can add, delete or modify emergency contacts.
    2. Audio Analysis: The app continuously analyzes audio input from the device's microphone.
    3. Threat Detection: Employing ensemble modelling approach to detect potential threats, including screams, crying, gunshots, and hate speech via scream and hate speech detection ML models.
    4. Alert Generation and Verification: When a potential threat is detected, the app generates an alert message which includes a countdown timer (e.g., 7 seconds) for user verification where user can cancel the alert in case of a false positive. 
    5. Emergency Actions: If threat confirmed, emergency actions initiated which includes sending a SOS message to preset emergency contacts with a danger alert and users’ current location in the message and initiates a call to the police station.  
    6. Voice Activated Alert: Users can trigger an alert by saying the predefined keyword, "Safeguard help me." The app performs voice recognition to verify the user's voice. Emergency actions are initiated if the user's voice is recognized.
    7. Fake Call Stimulator: Users can activate a fake call feature from the app which simulates a call from an official-looking police officer to deter potential threats. Users can interact with the fake call, creating the illusion of a genuine conversation.
    8. User Training for Predefined Keyword: Users can perform voice training for the predefined keyword during setup to improve recognition accuracy.
    9. Cross-Platform Compatibility: The app is compatible with both iOS and Android platforms, allowing a wide range of users to access its features.
    
### Non-Functional Requirements
    1. Usability: The app will have an intuitive and user-friendly UI to make it accessible to a wide range of users, including those with limited tech experience.
    2. Performance: The app will perform efficiently with an accuracy of 85%- above 90% as the models will be trained properly minimizing any delays in generating alerts or initiating emergency actions.
    3. Security: The app will perform user authorization to prevent unauthorized access and we will be using Firebase to store the data securely. 
    4. Maintainability: The product will be easily maintained because we would be using built-in modules for the specified features and if a module is to be updated or fixed the whole system doesn’t require change. 
    5. Modifiability: The product will be built in modules in such a way that modules will be independent and any additions or changes can be made without affecting the whole system.
    6. Reusability: Since each feature will be independent, therefore with a little change, they can be used in other similar systems. 
    7. Compatibility: The app will be developed using Flutter in Dart to make it compatible with a wide range of mobile devices and operating systems (iOS and Android) to ensure broad user adoption.
    8. Voice Recognition Accuracy: Using noise cancellation tools and high accuracy models the app will recognize the predefined keyword and the user's voice, even in noisy environments. 

### Target Audience
    1. Women of All Ages: Women of all age groups who use public transportation, ride-sharing services, or other means of commuting. The app is designed to cater to the safety and security needs of women across various life stages.
    2. Urban Dwellers: Women residing in urban and suburban areas where public transportation and ride-sharing services are commonly used. SafeGuardHER addresses safety concerns in urban environments.
    3. Frequent Travelers: Women who travel regularly for work, education, or leisure and rely on public transportation or ride-sharing for their journeys.
    4. Young Adults: College students and young professionals who commute to educational institutions and workplaces using public transportation and ride-sharing services.
    5. Parents and Caregivers: Women responsible for the safety and security of their families who may want to ensure their own safety during travel.
    6. Travel Enthusiasts: Women who enjoy traveling and exploring new places, as SafeGuardHER provides an additional layer of security during their journeys.
    7. Advocacy and Safety Organizations: Organizations and advocacy groups focused on women's safety and security, as they may recommend or partner with SafeGuardHER to promote safety measures.
    
## Proposed Design
SafeGuardHER is a cross-platform mobile application, compatible with both Android and iOS devices, designed with a primary focus on enhancing women's safety and security during public transportation, ride-sharing services, and various travel scenarios. 
To enable advanced audio analysis of the user's environment for threat detection, users will need to grant microphone access to the app via their device's permission settings and ensure the phone is placed in an open space for optimal analysis.
To enable the voice-activated feature, users will be required to input the key command, "SafeGuard help me," in various tones and accents. This step allows the speech recognition model to adapt to the user's voice, ensuring the feature is triggered only when the user speaks the keyword and not by others.
Setting up emergency contacts is a critical aspect of the app's functionality. For user convenience, there will be an option to either search for and select contacts from the user's existing phone contacts or manually enter contact information into the app.
To ensure user engagement and app activation, the app will send timed alert notifications as reminders to encourage users to enable the app before heading out or whenever they anticipate the need for its features. Once activated, the app will remain functional in the background, even when not actively in use on the user's device, ensuring continuous monitoring and safety support.  


### System Architecture
Present on the OnBoard page

### Data Model
# 3.2.1 Hate Speech Model in Roman Urdu
Developed a hate speech model specifically tailored for Roman Urdu with the following specifications:
## Model Architecture
The model architecture used for hate speech detection is based on transfer learning and deep learning. Specifically, we used a BERT model because it provides us with a powerful tool that can understand the context and semantics of text, adapt to specific tasks, and deliver high performance, especially when dealing with languages like Roman Urdu.
## Dataset
We acquired our dataset, written in Roman Urdu, from the Hugging Face website [5]. The dataset was created by gathering various tweets from Twitter and then classified it using binary labels of “1” being Normal and “0” being Abusive/Offensive as showcased in Figure attached below. (I've concealed the inappropriate text due to the offensive language used)


# 3.2.2 Scream Detection Model
Implemented a scream detection model with the aim of accurately identifying instances of screaming in audio data.
## Model Architecture
The model has a neural network architecture which is constructed using TensorFlow Keras. This model receives YAMNet embeddings as input, passed through a dense hidden layer with 512 units and ReLU activation. The output layer corresponds to the number of classes, with a softmax activation function applied for classification. The model is compiled using Sparse Categorical Crossentropy loss and the Adam optimizer.
## Dataset
The dataset we used to train our scream detection model. We've labeled the data in a binary manner, where "1" indicates the presence of a scream and "0" signifies the absence of a scream. By training our model on a diverse range of data, we have achieved a high level of accuracy and consistent prediction capabilities for scream detection.
## Inference
To showcase the model's predictive capability, a sample audio file (testing_wav_data_file) is loaded and processed using YAMNet as shown in Figure 4 attached below. The model then predicts the class based on the mean of the result, providing an inferred class for the given audio sample which in the illustrated case is “No-scream”.

# 3.3.3 Speaker Identification Model
The application features a speaker identification model designed for discerning the app owner during the utilization of the keyword activation functionality, specifically activated by the user saying 'Safeguard Help' to initiate emergency SOS actions. In order to ensure the authenticity of the said keyword, the app initially verifies that it is spoken by the registered user. To implement this process, users are prompted with a designated paragraph to be articulately recorded in their own voice during the initial account setup. Subsequently, these audio files are transmitted to the server, where the speaker identification model is deployed. The model undergoes fine-tuning based on the user's voice characteristics. Once the fine-tuning process is completed, the refined model's TensorFlow Lite (tflite) file is transmitted back to the application and stored locally for subsequent use.
## Model Architecture
The core building blocks of the model is residual blocks. These blocks are designed to facilitate the learning of hierarchical features and gradients throughout the network. Each residual block consists of multiple convolutional layers with a residual connection. This architecture helps mitigate the vanishing gradient problem, enabling the model to effectively learn intricate patterns in the audio data. After the residual blocks, an average pooling layer is applied to reduce the spatial dimensions, followed by flattening to prepare the data for the fully connected layers.
## Training
The model is trained using the Adam optimizer and sparse categorical crossentropy loss. Additionally, early stopping and model checkpointing callbacks are implemented to prevent overfitting and save the best model during training.

### Risks
Check out the [Google Document](https://docs.google.com/document/d/1Y2YtVAONh_GrqTm2o3M1Cancu20Mz6OUaIecOFyrm2Q/edit) for more information.


## Issues
To view additional project documentation, visit the [Google Docs document](https://docs.google.com/document/d/1MzgGkfLE-X0YPtWw_c3WecNsVp3VfxeMWIUjFpea45s/edit).
