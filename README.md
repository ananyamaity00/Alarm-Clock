# Alarm-Clock

import datetime

from playsound import playsound

alarmHour = int(input("Enter Hour: "))
alarmMinutes = int(input("Enter Minutes: "))
alarmAm = input("am / pm: ")

if alarmAm == "pm":
    alarmHour += 12

while True:
    now = datetime.datetime.now()
    if alarmHour == now.hour and alarmMinutes == now.minute:
        print("Wake Up!")
        playsound("alarm.mp3")
        break
