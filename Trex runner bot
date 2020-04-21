from PIL import ImageGrab, ImageOps
import pyautogui
import numpy
import time

playCoordinates = (505, 511)
dinasourCoordinates = (215, 525)

def start():
    pyautogui.click(playCoordinates)
def jump():
    pyautogui.keyDown("space")
    time.sleep(0.1)
    print("Jumping... ")
    pyautogui.keyUp("space")
def getBox():
    box = (dinasourCoordinates[0] + 150,
           dinasourCoordinates[1],
           dinasourCoordinates[0] + 190,
           dinasourCoordinates[1] + 30
    )
    image = ImageGrab.grab(box)
    grayImage = ImageOps.grayscale(image)
    arr = numpy.array(grayImage)
    return arr.sum()

start()
time.sleep(1)
jump()

while True:
    v = getBox()
    if v < 296400:
        print("an object detected !")
        jump()
