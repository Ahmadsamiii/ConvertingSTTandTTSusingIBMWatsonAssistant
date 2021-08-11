# Software and Internet of Things Track | Task-4

## Converting Speech to Text and Speech to Text using IBM Watson Assistant

- Description:

This is repository aims to convert speech to text using python and IBM Watson Assistant.


## Step.(1): Open - [IBM Watson Assistant from here](https://cloud.ibm.com/catalog), then create your account if you don't have, if you already have one please login:




![image](https://user-images.githubusercontent.com/85820553/128946628-622d6498-2d94-4632-adbd-09a770dd1d6a.png)


## Step.(2): Get your Credentials:


![image](https://user-images.githubusercontent.com/85820553/129007700-c8bcf783-a1d6-4c3e-a88a-5ac3c08d0b46.png)





## Step.(3): Clone IBM Watson Streaming STT Project:
For this step I used Pycharm IDE and created a new project, then I used its terminal to run this following code which clones the github project files into my pycharm project:

```
git clone https://github.com/IBM/watson-streaming-stt
```

![image](https://user-images.githubusercontent.com/85820553/129009483-5e0d9501-5ade-4dd1-9b49-f4fbd894d273.png)


## Step.(4): Install Dependencies
Running this project requires specific packages written in (requirements.txt) file so use the following line of code to download then from the requirements file:

```
pip install pipwin
```

![image](https://user-images.githubusercontent.com/85820553/129009418-c4eec00e-471b-4b48-946b-9ae0fa9bc624.png)



```
pipwin install pyaudio
```

![image](https://user-images.githubusercontent.com/85820553/129010048-f727b0b3-42d0-4953-98ee-ee803f9a74fd.png)




## Step.(5): Update Region & API key

In your cloned project, go to line number 2 in (speech.cfg) file, erase the old API and replace it with your own (the ones you got from step 2):

![image](https://user-images.githubusercontent.com/85820553/129014594-3cb7440c-1782-440b-a549-8d6f53bb02b6.png)



![image](https://user-images.githubusercontent.com/85820553/129014640-8c98b046-7e3a-478a-87c9-3d9118b5dc6f.png)



Then, go to line number 175 in (transcribe.py) file and erase the old region and replace it with your own (the ones you got from step 2):
you can git your region model [from here](https://cloud.ibm.com/docs/speech-to-text?topic=speech-to-text-models)



## Step.(6): Speech To Text File
In the following lines of code I started by creating a text file named (STT.txt) followed by the function 'write' which writes the text content into the text file, and finally closing the file, and the text file will be found with the rest of the project files after running the code:

```
fo = open('STT.txt', 'w')
fo.write(transcript)
fo.close()
```

![image](https://user-images.githubusercontent.com/85820553/129075753-b6483a67-af6f-4427-b445-2932ac1a2a9b.png)



## Step.(7): Text To Speeh (TTS)

In the step we want to convert our text into an audio using the following code lines, I started by creating passing the text into gTTS function which will convert the text into the audio file and then save it under the name (TTS.mp3) and the mp3 file will be found with the rest of the project files after running the code:


```
output = gTTS(text=transcript, lang='en', slow=False)
output.save("TTS.mp3")
```

![image](https://user-images.githubusercontent.com/85820553/129075753-b6483a67-af6f-4427-b445-2932ac1a2a9b.png)



## Step.(8): Run The Code
Now that everything is ready we will run the code using the following command where we use -t to specify how long we want to record (ex: 20 sec)
Note: mke sure you are in the correct directory otherwise use (cd ./watson-streaming-stt) 

```
python transcribe.py -t 20
```


## SPEECH
As i run the program i started speaking and the program started showing my speech in the terminal, and it showed a correct result as i was saying (hello everyone I'm speaking English only I cannot speak any other languages thank you )

![image](https://user-images.githubusercontent.com/85820553/129100588-0e6cf521-5b5e-4f70-9d34-dfb796604442.png)





https://user-images.githubusercontent.com/85820553/129101402-e658ca6f-70bc-4fac-a86e-ed42331809a6.mp4



## MP3 FILE
After running the program it converted the output text automatically into mp3 file as you can hear in this video:



https://user-images.githubusercontent.com/85820553/129102272-b5e0d3fe-2541-439d-8c12-275f9db5e159.mp4




## TEXT FILE
After running the program it converted my final speech automatically into a text file 

![image](https://user-images.githubusercontent.com/85820553/129101820-6467b135-57aa-4b8d-a224-46bd80eda7b5.png)


