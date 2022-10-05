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

##Step 2: Adafruit IO Setup
Once all of that was downloaded I went to https://io.adafruit.com/ and made a free account. After that, there should be a yellow round icon with a key in it. Click on it.
There should be a pop-up with your username and active key. Copy each.

##Step 3: Colorpicker
On the Adafruit IO website, I went to Dashboards > New dashboard.
I made a new dashboard and called it ToDo2. 
In this dashboard I created a New Block by clicking the gear icon in the right corner and chose 'color picker'. 
<img width="346" alt="Screenshot 2022-10-05 at 16 52 24" src="https://user-images.githubusercontent.com/83424135/194091782-aae8029e-650a-46f7-b971-79d0acff49ca.png">
I set the feed name to 'color' and accept
<img width="563" alt="Screenshot 2022-10-05 at 16 53 50" src="https://user-images.githubusercontent.![Uploading Screenshot 2022-10-05 at 16.57.09.png…]()
com/83424135/194092132-ac4256ef-bcf7-49ed-b555-b59c30e13431.png">
Then you can manipulate the color within the circle
<img width="288" alt="Screenshot 2022-10-05 at 16 57 52" src="https://user-images.githubusercontent.com/83424135/194093004-f9204754-a16f-4531-bc5b-da8c8994165d.png">

