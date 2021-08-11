# Software and Internet of Things Track | Task-4

## Converting Speech to Text using IBM Watson Assistant

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
