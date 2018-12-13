#advised O/S Ubuntu(any version) 
#pip install pocketsphinx  
#pip install SpeechRecognition  
# The SpeechRecognition library needs the PyAudio package to be installed in order for it to interact with the microphone input.
#The pocketsphinx library used is not as accurate as other engines like Google Speech Recognition as the google's is not free . There may be ways to tweak it to be more accurate, but I need to explore it further.
#If your code is not detecting speech when run, it's most probably due to the ambient noise the microphone might be picking up, start from simple alphabeths or musical sounds
#To run open python shell and type execfile('text2speech.py')
import speech_recognition as sr  

# obtain audio from the microphone  
r = sr.Recognizer()  
with sr.Microphone() as source:  
	print("Please wait. Calibrating microphone...")  
# listen for 5 seconds and create the ambient noise energy level  
	r.adjust_for_ambient_noise(source, duration=5)  
	print("Say something!")  
	audio = r.listen(source)  

# recognize speech using Sphinx  
try:  
	print("Frops thinks you said '" + r.recognize_sphinx(audio) + "'")  
except sr.UnknownValueError:  
	print("Frops could not understand audio")  
except sr.RequestError as e:  
	print("Frops error; {0}".format(e)) 

#code using Google Speech Recognition
#try:
    # for testing purposes, we're just using the default API key
    # to use another API key, use `r.recognize_google(audio, key="GOOGLE_SPEECH_RECOGNITION_API_KEY")`
    # instead of `r.recognize_google(audio)`
#    print("Google Speech Recognition thinks you said " + r.recognize_google(audio))
#except sr.UnknownValueError:
#    print("Google Speech Recognition could not understand audio")
#except sr.RequestError as e:
#    print("Could not request results from Google Speech Recognition service; {0}".format(e))
