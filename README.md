<H1 ALIGN=CENTER> IMPLEMENTATION OF SPEECH RECOGNITION </H1>
<H3> NAME : SOUVIK KUNDU</H3>
<H3> REGISTER NUMBER : 212221230105 </H3>
<H3>EXPERIMENT NO : 08 </H3>
<H3>DATE  : 29.04.2024 </H3>

## AIM:
To implement the conversion of live speech to text.

## ALGORITHM:
Step 1: Import the speech_recognition library<Br>
Step 2: Initialize the Recognizer<Br>
Step 3: Create an instance of the Recognizer class, which will be used for recognizing speech.<Br>
Step 4: Set the duration for audio capture<Br>
Step 5: Define a variable to specify the duration (in seconds) for which the program will capture audio from the microphone.<Br>
Step 6: Display a message in the console to prompt the user to speak.<Br>
Step 7: Capture audio from the default microphone<Br>
Step 9: Use the default microphone as the audio source.<Br>
Step 10: Record audio for the specified duration using the Recognizer instance.<Br>
Step 11: Perform speech recognition with exceptional handling:<Br>
•	Attempt to recognize speech from the captured audio using the Google Speech Recognition service.<Br>
•	If successful, print the recognized text.<Br>
•	Handle specific exceptions: If the recognition result is unknown or if there is an issue with the request to the Google Speech Recognition service, print corresponding error messages.<Br>
•	A generic exception block captures any other unexpected errors.<Br>

## PROGRAM:
```python
import speech_recognition as sr
r = sr.Recognizer()
duration = 30
print("Say something")
with sr.Microphone() as source:
    audio_data = r.listen(source,timeout=duration)

try:
    text= r.recognize_google(audio_data)
except sr.UnknownValueError:
    print("Sorry, couldn't understand the audio")
except sr.RequestError as e:
    print(f'Error with request tp Google Speech Recognition service: {e}')
except Exception as e:
    print(f'Error : {e}')

```

## OUTPUT:
![image](https://github.com/Shrruthilaya-Gangadaran/Ex-8--AAI/assets/93427705/8d8a5a9d-f09a-4410-b725-7e6bae6c9f6f)


## RESULT:
Thus the python program for Speech Recognition is implemented successfully.
