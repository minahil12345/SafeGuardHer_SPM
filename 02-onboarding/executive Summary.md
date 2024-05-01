# Executive Summary

**Project Name:** SafeGuardHER

**Objective:** Revolutionize women's safety during public transportation and ride-sharing journeys through an innovative cross-platform mobile application.

**Overview:** SafeGuardHER is designed to address the pressing need for enhanced safety for women during travel. Unlike existing safety applications in Pakistan, which require manual activation in emergencies, SafeGuardHER employs automated audio analysis and voice activation, among other unique features, to provide comprehensive safety solutions. This approach addresses the challenge where manual activation might not be possible due to the urgency or intensity of threatening situations.

## Core Features

- **Automated Threat Detection:** SafeGuardHER continuously analyzes the user's environment, using ensemble modeling techniques to detect signs of hate speech and screams. If a threat is predicted, a 7-second countdown timer is triggered. If the timer reaches zero without cancellation, the app sends alerts to pre-saved emergency contacts, shares the user's location, and initiates a call to the police.

- **Voice-Activated Alerts:** Users can trigger an emergency alert by saying "Safeguard help me." This feature uses voice recognition to confirm the user's identity and then initiates emergency actions.

- **Fake Call Simulator:** This feature allows users to simulate a call from a police officer, creating the appearance of a genuine conversation to deter potential threats.

## Project Vision

SafeGuardHER aims to empower women by providing a reliable and intuitive safety companion that supports them during their journeys. By offering automated threat detection, voice-activated alerts, and the fake call simulator, SafeGuardHER addresses critical gaps in existing safety applications.

## Project Components

The project is structured into four major components:

1. **Data Gathering and Model Testing**
   - Develop robust hate speech and scream detection models, with a target accuracy of 85% or higher.
   - Collect and label a diverse dataset to train the models, categorizing audio inputs as threats or non-threats.

2. **Developing Ensemble Model Architecture**
   - Utilize ensemble modeling bagging techniques to enhance accuracy and reliability.
   - Refine the evaluation metric to ensure accurate threat prediction.

3. **App Development and Model Integration**
   - Develop prototypes in Figma and build the app using Flutter.
   - Integrate the detection and voice recognition models into the app.

4. **App Testing and Refining Process**
   - Test the app for usability, reliability, and effectiveness in real-world scenarios.
   - Collect user feedback to refine and improve the app's features.

## Initial Project Goals

In the first iteration, the focus is on achieving the following:

- Develop and test the hate speech and scream detection models to meet the accuracy target.
- Build the voice recognition model using a limited set of audio inputs provided by users.
- Create prototypes for the app and commence development.
- Conduct initial testing to ensure the app's core features function as intended.

By achieving these initial goals, SafeGuardHER will lay a strong foundation for future iterations, focusing on enhancing women's safety and security during their journeys.
