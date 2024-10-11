# Real-Time-Image-Analysis-and-Auditory-Guidance-for-the-Visually-Impaired

This project focuses on creating an interactive image analysis and feedback system tailored for visually impaired users. By leveraging the BLIP (Bootstrapping Language-Image Pre-training) model from Salesforce, which has been optimized for CPU performance, the system is capable of processing images on a Raspberry Pi and providing real-time auditory descriptive feedback.

<div align=center>
 <img src="./images/Image_1.png" width=400 >
</div>


## System Overview

The system uses the Raspberry Pi Camera Module 2 to capture images, then processes them through the BLIP model to generate descriptive captions. These captions are delivered via a USB speaker for auditory feedback. Additionally, system information and generated captions are displayed on an LCD screen for users who have some degree of vision. The system also integrates with a custom Azure server to upload images and their associated captions for storage and further analysis.




## Key Features
- **Immediate Image Processing**: Images are processed on the Raspberry Pi to generate captions with minimal delay, ensuring a smooth and responsive experience for visually impaired users.
- **Auditory Output**:  The system provides descriptive feedback and status updates through a USB-connected speaker, making it more accessible for those with vision impairments.
- **LCD Display Support**: Captions and system statuses are displayed on an LCD screen, catering to users who may have partial vision and prefer visual feedback.
- **Cloud Connectivity**: The system uploads both images and their captions to a dedicated Azure server, enabling remote access and potential for additional analysis or record-keeping.

<br/>

 


## Hardware Components
- **Raspberry Pi 4**
- **Raspberry Pi Camera Module 2**
- **Button**
- **LCD Display (Model LCD1602)**
- **USB Speaker**
<br/>


<div align=center>
 <img src="./images/complete_hardware.png" width=400 >
</div>
<br/>


## Software Architecture
- **Operating System**: Raspberry Pi OS
- **Machine Learning Model**: BLIP model for image captioning
- **Audio Feedback**: gTTS library for text-to-speech conversion
- **Cloud Services**: Microsoft Azure for backend infrastructure
<br/>


## Pre-requisites

##### Conda Environment
Create a separate conda environment with the python version 3.11 using the following command:

```
conda create -n visioncaster python=3.11
```

then activate the environment:

```
conda activate visioncaster
```
 
and install the required libraries using the following command:

```
pip install -r requirements.txt
```
<br/>


## Usage


```bash
# activate the conda environment
conda activate visioncaster

# run the flask application
python run.py
```

<br/>
