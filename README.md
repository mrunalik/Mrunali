# Mrunali

import speech_recognition as sr

print("Speak something")

r = sr.Recognizer()


with sr.Microphone() as source:
	audio = r.listen(source)
try:
	print("Your said:  "+r.recognize_google(audio))
except Exception:
	print("something went wrong")
