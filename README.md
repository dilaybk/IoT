# IoT
Themasemester: Designing for Emerging Tech
Dilay Bayraktaroglu


## Adafruit IO - Budget Philips Hue
How I made a cheap version of Philips Hue

What you need:
  - Arduino NodeMCU
  - Led strip
  - Cable to connect to your pc

## Step 1: Installing Arduino IO
I installed Arduino IO by going to 'library manager' on the Arduino Software. 
I struggled a little by finding the proper library because the picture in the document that I followed showed something different than what I actually needed to install.

<img width="179" alt="Screenshot Arduino IO Library" src="https://user-images.githubusercontent.com/83424135/194088879-0ad06349-ec6e-40d6-b25b-69d5229751bf.png">
^This is the right one

I clicked on install as instructed and waited until it was done.
<img width="586" alt="Screenshot install all library" src="https://user-images.githubusercontent.com/83424135/194089601-4f9b0bee-ca04-4092-bdc9-03f33e438e3d.png">


## Step 2: Adafruit IO Setup
Once all of that was downloaded I went to https://io.adafruit.com/ and made a free account. After that, there should be a yellow round icon with a key in it. Click on it.
There should be a pop-up with your username and active key. Copy each.

## Step 3: Colorpicker
On the Adafruit IO website, I went to Dashboards > New dashboard.
I made a new dashboard and called it ToDo2. 
In this dashboard I created a New Block by clicking the gear icon in the right corner and chose 'color picker'. 

<img width="346" alt="Screenshot 2022-10-05 at 16 52 24" src="https://user-images.githubusercontent.com/83424135/194091782-aae8029e-650a-46f7-b971-79d0acff49ca.png">

I set the feed name to 'color' and accept

<img width="563" alt="Screenshot 2022-10-05 at 16 53 50" src="https://user-images.githubusercontent.com/83424135/194093545-e986531c-413a-478a-9d16-fc853b098f67.png">

Then you can manipulate the color within the circle

<img width="288" alt="Screenshot 2022-10-05 at 16 57 52" src="https://user-images.githubusercontent.com/83424135/194093004-f9204754-a16f-4531-bc5b-da8c8994165d.png">


## Step 4: Change the code in Arduino
- In Arduino > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
- Go to the tab 'config.h' within your sketch and paste your username and Key that you previously copied at step 2

<img width="683" alt="Screenshot 2022-10-05 at 17 11 01" src="https://user-images.githubusercontent.com/83424135/194096085-fcf4e831-c57f-4085-839d-b0615284ea23.png">

Paste username & key:

<img width="455" alt="Screenshot 2022-10-05 at 17 14 27" src="https://user-images.githubusercontent.com/83424135/194096898-8af7b3b2-7708-4515-9e7f-89a6b1eda318.png">


- Important! Scroll down in the sketch to write in your WiFi network name and password. 
  I made the mistake of not doing this so I struggled a lot trying to figure out what was wrong.
  
<img width="376" alt="Screenshot 2022-10-05 at 17 15" src="https://user-images.githubusercontent.com/83424135/194097041-ef1c8bf7-7561-4344-8c47-77a6c81c1c57.png">

> NodeMCU doesn't work with 5G WiFi, so connect to your hotspot. It doesn't use more than 0.1Mb data

In the tab adafruit_14_neopixel.io, I changed PIXEL_PIN 5 to PIXEL_PIN D5

## Step 5: Upload your code
1. Upload the code
2. Tools > Serial Monitor
3. Set serial monitor to 115200 baud
    - If you see this:
    
    <img width="775" alt="Screenshot 2022-10-05 at 17 21 50" src="https://user-images.githubusercontent.com/83424135/194098717-164a10c5-e8a3-49b7-a4a3-500117f8ff49.png">

      It means that you're probably doing something wrong. In my case I forgot to swtich to my hotspot. I was still connected to my 5G Wifi.
      
      Once your connected, you'll see this:
      
<img width="220" alt="Screenshot 2022-10-05 at 17 51 54" src="https://user-images.githubusercontent.com/83424135/194105946-235672c5-323e-4c9a-af26-39b37933c539.png">

When you edit the color you'll see the changes in the serial monitor like in the previous picture.

## Result
The results should look like this:

https://user-images.githubusercontent.com/83424135/194108734-9acf5fb3-1443-403d-b996-1d195792562c.MOV

(link to the video if it doesn't work: 
https://icthva-my.sharepoint.com/:v:/g/personal/dilay_bayraktaroglu_hva_nl/EdbtymE8qzVGleYlL138lnwBNAz8v5SISYWyu1w5OZrU9w?e=pb8fVb)



## References

https://docs.google.com/document/d/14jhaxaJUhuu0p6_u_oNj8_50Y6PAmtrvcePtKc0HDGs/edit#
