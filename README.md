# Wav2Lip
Wav2Lip is a new state of art model for lip synchronization and using deepfake voice with the faces of others. Wav2Lip uses a standard encoder-decoder architecture that takes the target pose and target speech as input and generates a lip-synced face 

<img align="center" alt="Wav2Lip" width="600" src="https://miro.medium.com/v2/resize:fit:828/1*UVCxlFq409CPYns7uxSOww.gif">


# Models
I have used many versions of Wav2Lip for lip synchronizing like:
* Wav2Lip
* Wav2Lip_Hq - Gan
* Wav2Lip_Hq + Gan
* Wav2Lip_CodeFormer
* Wav2Lip_Simple

Note:- Before Expalining each model first take note of Wav2Lip was trained on low resolution video and its need face in each frame of video (if you provide video which contain images without face then it won't accept it!). 

# Wav2Lip (Original)
This model was made by rudrabha and i got it reference to test how are the results i get if i uesd original code.
* Step-1
I downloaded audio and video file from task pdf and took code from github and tried in colab. Importing necessary libaries, but beforing fetching input i trimmed both audio and video at 9 seconds as it was the best test sample with face in each frame.
* Step-2
I  uploaded both audio and video and start inference file. I got my results.

# Wav2Lip_Hq - Gan
This model also know as Wav2Lip_Hq which has multiple pre-trained files which i tried to use to get result more in sync and better. I used a wav2lip.pth, face_segmentation.pth, and esrgan_yunying.pth in this model you can use video even without having faces in each frame but i still use original inputs as in my above model. Here change audio from wav to mp4.
* Step-1:
Same step importing required libraries.
* Step-2:
In this step i uploaded all pth file and input in drive. In drive click an individual file and select share option in share option change setting from restrited to anyone with link and copy link.
copy only part of link which is start after d/ and ends before /view part and paste it in code uner urls. Now do same for all other pth file and inputs files.
* Step-3:
Run the inference file and you get your output.

# Wav2Lip_Hq + Gan
In this model only difference is the pth file we use is with gan trained like wav2lip_gan.pth and remaining are all same file and input file. Here change audio from wav to mp4.
* Step-1:
Same step importing required libraries.
* Step-2:
Same step as above model but link path of wav2lip_gan.pth will be there to use.
* Step-3:
Run the inference file and you get your output.

# Wav2Lip_CodeFormer
This model is modified by a langzizhixin he tried to improve lip syncronizing and make it look like real.
* Step-1:
Here phase 1 is same as wav2lip original code.
* Step-2:
After getting output he tried to takes images of each frames and store it.
* Step-3:
he is using blur methods of image processing with opencv to remove blur part from each frame and merge each frame together.
* Step-4:
The merge frame video has no audio so again adding audio in the end and we got our output.

# Wav2Lip_Simple
This is a simple version of all the above codes in very convient way made by justinjohn0306 based on wav2lip original code develop by rudrabha.
* Step-1:
By providing youtube Url your video gets downloaded and trimmed with start and end seconds. Note: video with max 60 seconds!
* Step-2:
Uploading audio file.
* Step-3:
Selecting padding custom settings you can change the parts.
* Step-4:
after running inference on it you get your output.

# Results
As we see each results are different from other but in each video i got is not as expected as i want. In each video i can see a blur part on lips and in some video i can see some lips are different from original as i had use pre-trained model but i still got results which can says that the model frameworks is realiable but i can try with custom data to trained a model for the persons who has beard on it.


