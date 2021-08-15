---
layout: post
title: Automating Zoom Login
category: Python
tags: Python
published: True
---
<style>
  .preDefault {
    font-family: Andale Mono, Lucida Console, Monaco, fixed, monospace;
    color: #000000;
    background-color: #eee;
    font-size: 15px;
    border: 1px dashed #999999;
    line-height: 16px;
    padding: 5px;
    overflow: auto;
    width: 100%
  }
  .codeDefault {
    color:#000000;
    word-wrap:normal;
  }
</style>

Video conferencing or web conferencing has been a staple of
how we socialize and carry out business meetings ever since COVID19.

We have so many online meetings now that it can be a hassle to remember the meeting IDs
and the meeting passwords.

So to manage the new normal, I wrote two short scripts to automate logging into Zoom
and joining a meeting. You can create multiple scripts for the various regular meetings
you have throughout the week!

The script is written in python and makes use of pyautogui. You can access the repo [here](https://github.com/ye-song/zoom-automation) and follow the instructions in the script
to use it on your PC or laptop.

The first script is mouseXY.py. This script will help you to locate the coordinates of your mouse on the screen. This will be helpful in modifying the next script for your personal setup because where the buttons are for the click action is dependent on your screen resolution.

<pre class="preDefault">
  <code class="codeDefault">
  #! python3
  # mouseXY.py - Displays the mouse cursor's current position.
  import pyautogui
  print ("Press Ctrl-C to quit.")

  try:
      while True:
          # Get and print the mouse coordinates.
          x, y = pyautogui.position()
          positionStr = 'X: ' + str(x).rjust(4) + ' Y: ' + str(y).rjust(4)
          pixelColor = pyautogui.screenshot().getpixel((x, y))
          positionStr += ' RGB: (' + str(pixelColor[0]).rjust(3)
          positionStr += ', ' + str(pixelColor[1]).rjust(3)
          positionStr += ', ' + str(pixelColor[2]).rjust(3) + ')'
          print(positionStr, end='')
          print('\b' * len(positionStr), end='', flush=True)
  except KeyboardInterrupt:
      print('\nDone.')
  </code>
</pre>

The second script is Zoom.py. This script can be modified and it need not be for zoom only.
As long as you know the path to the video conferencing software you are using, you should be able to trigger it and automate the login.

<pre class="preDefault">
  <code class="codeDefault">
  #! python3
  # Zoom.py - opens up zoom and login the meeting session.

  import subprocess
  import pyautogui
  import time

  '''
  This is a sample code. To use this sample code:
  1. Replace the path of zoom application on your machine
  2. Replace the coordinates of where each mouse click will be
  ** Note that this depends on the screen resolution of your machine.
  3. Replace the 'meeting ID' placeholder
  4. Replace the 'password' placeholder
  The times are added because pyautogui runs too fast before the
  GUI is loaded. Increase the sleep time if you find that the mouse
  click is triggered before the GUI can be loaded.
  '''
  subprocess.Popen('C:\\Users\\AppData\\Roaming\\Zoom\\bin\\Zoom.exe')
  time.sleep(1)
  pyautogui.click((1300, 713))
  time.sleep(1)
  pyautogui.typewrite('meeting ID')
  time.sleep(1)
  pyautogui.click((1305, 908))
  time.sleep(2)
  pyautogui.typewrite('password')
  time.sleep(1)
  pyautogui.click((1295, 906))
  </code>
</pre>

You can also take a look at this short video demo on the scripts that I have created [here](https://www.youtube.com/watch?v=MACX3xcvvYg). Enjoy!
