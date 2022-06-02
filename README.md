# PROPHECY-STEMI

## [Problem Definition]
![image](https://user-images.githubusercontent.com/97151697/171563811-d32765f4-b429-49be-944a-e53209ce917f.png)

build a deep learning algorithm to classify patients with STEMI or not using ECG and CNN 1d Model

- x = time-series data (ECG waveform)
- y = labels (STEMI or Not ; 0 or 1)

## [Data Preprocess]
(1) Setting
- AWS EC2 instance (type) : ecg_aws_jpt2 (g4dn.4xlarge)
- AWS S3 bucket : dr-you-ecg-20220420_mount

(2) Data Resource
- internal | Severance, Seoul (KOMATE)
- external | open ECG data (PTB_XL)

(3) Preprocessing Code
Code | preprocessing | make a label table | make datasets
---|---|---|---|
KOMATE | X (privacy) | O | O
PTB_XL | O | O | O
- [KOMATE](https://github.com/kyulee-jeon/PROPHECY-STEMI/blob/main/Code/Make%20label%20table%20and%20datasets%20of%20KOMATE.ipynb)
- [PTB_XL](https://github.com/kyulee-jeon/PROPHECY-STEMI/blob/main/Code/Preprocess%2C%20Make%20label%20table%20and%20datasets%20of%20PTB_XL.ipynb)

## [Model build, train and test]

- [Model and GradCam](https://github.com/kyulee-jeon/PROPHECY-STEMI/blob/main/Code/Model%20and%20Visualization.ipynb)
- [simple Model and GradCam](https://github.com/kyulee-jeon/PROPHECY-STEMI/blob/main/Code/simple%20Model%20and%20Visualization.ipynb)

(+) visualize the waveform of the data that algorithm tell us it's not STEMI but it was.
- [extract and show FN waveform](https://github.com/kyulee-jeon/PROPHECY-STEMI/blob/main/Code/extract%20and%20show%20FN%20waveform.ipynb)



