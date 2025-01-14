# HowTo - NAO
![Nao](https://badgen.net/badge/Robot/Nao/blue)

---

## Content

- [Installing Choreographe - Windows](#installing-choreographe---windows)
- [Installing Choreographe - Linux](#installing-choreographe---linux)
- [Connecting Choreographe to physical robot](#connecting-choreographe-to-physical-robot)
- [Choreographe UI](#choreographe-ui)
- [Setting up a virtual robot](#setting-up-a-virtual-robot)
- [Creating and running a project](#creating-and-running-a-project)
- [YouTube tutorials](#youtube-tutorials)
- [Resources](#resources)

---

### Installing Choreographe - Windows

1. **Download the setup file**\
  If you're installing Choreographe on a Windows machine, the setup file is easier to install.\
  You can download the setup file [here](https://www.softbankrobotics.com/emea/en/support/nao-6/downloads-softwares).
 
 2. **Run the installer**\
  Run the file you just downloaded.
   
  *For a more detailed guide to the installation check the [official documentation](http://doc.aldebaran.com/1-14/software/installing.html).*

---

### Installing Choreographe - Linux

1. **Download the binaries**\
  If you're installing Choreographe on a Linux machine, it's better to donwload the binaries and install them by command line.\
  You can download the binaries [here](https://www.softbankrobotics.com/emea/en/support/nao-6/downloads-softwares).
 
 2. **Install the binaries by command line**
  - Type this command in your terminal:

        choregraphe-suite-2.8.6.23-linux64$ ./choregraphe

  - If this error occurs: 
  
        choregraphe-suite-2.8.6.23-linux64/bin/../lib/libz.so.1: version `ZLIB_1.2.9' not found (required by /lib/x86_64-linux-gnu/libpng16.so.16)
  
    Type the following commands:
  
        choregraphe-suite-2.8.6.23-linux64/lib$ sudo mv libz.so.1 libz.so.1.old
        choregraphe-suite-2.8.6.23-linux64/lib$ sudo ln -s /lib/x86_64-linux-gnu/libz.so.1
        choregraphe-suite-2.8.6.23-linux64/lib$ ./choregraphe
   
   *For a more detailed guide to the installation check the [official documentation](http://doc.aldebaran.com/1-14/software/installing.html).*

---

### Connecting Choreographe to physical robot

1. **Cable connection**\
  Connect NAO to the router with an Ethernet cable. Attach it from the back of its head to a spare port of the router or to a switch connected to the router.

2. **NAO's IP address**\
  When you turn on NAO, he will start saying his IP address. Note it down and type it in a browser. You will access a webpage, from there you'll be able to configure his WIFI connection.

3. **Authentication**\
  Once you loaded the webpage, you will be asked for authentication.
    - Username: nao
    - Default password: nao
    
    If login fails or if you have lost your password, visit this [link](http://doc.aldebaran.com/2-1/nao/webpage_access.html#opennao-password-lost-nao).

4. **Network Settings**\
  When you reached NAO's webpage, select the network settings option and connect it to the WIFI.

- **Why choosing a WIFI connection instead of a cable connection?**\
  Connecting NAO to a WIFI network is highly recommended because he'll be able to move more freely, whithout having to pay attention to cables attached to him.

---

### Choreoghrape UI

![UI](img/UI.png)

- **Commands**\
  Here you can find all the commands that your NAO robot can execute. These are blocks that can be attached together to form a script, kind of like Scratch.

- **Robot view**\
  Here you can see the state of your NAO robot.\
  If you don't have a physical robot connected to your computer, this window will be your virtual robot and with it you'll be able to see how your script is behaving.

- **Connection**\
  Here you can connect Choreographe to your phisical robot or to a virtual robot.

- **Run/Stop**\
  These buttons allow you to run or stop your script.

---

### Setting up a virtual robot

- Click on <kbd>Edit > Preferences</kbd>\
  ![Edit](img/virtual1.png)

- Choose the correct NAO model and click <kbd>Ok</kbd> to confirm.\
  ![Nao version](img/virtual2.png)

---

### Creating and running a project

To start creating a script, go into the *Commands* section and choose the commands that your NAO robot will have to execute.

Make sure to connect the first block to the <kbd>onStart</kbd> connector and the last block to the <kbd>onStopped</kbd> connector.

Below is a video tutorial to better understand how to create your first script.

https://user-images.githubusercontent.com/42480082/163725934-db118552-6b19-4fc0-bb5b-30d7e319fb8b.mp4

---

### YouTube tutorials

Here is the [link](https://youtube.com/playlist?list=PLma9tC7VHPpi8Bz4i2P5FuMlfMhjZ3nJ-) to a YouTube playlist that I found really useful to start learning how to use Choreographe.

It includes tutorials on:
  - NAO's sensors and parts
  - Choreographe basics
  - Python programming in Choreographe
  - Vision (Face recognition and NaoMarks)
  - Audio and Speech Recognition

I strongly recommend to check it out!

---

### Resources
 - [Choreographe's official documentation](http://doc.aldebaran.com/1-14/software/choregraphe)
 - [Connecting NAO to the Internet](http://doc.aldebaran.com/2-1/nao/nao-connecting.html#connect-to-ethernet)
 - [Projects you can try on Nao](https://funlab.nd.edu/the-nao-base/special-movements/)
 - [YouTube tutorials](https://youtube.com/playlist?list=PLma9tC7VHPpi8Bz4i2P5FuMlfMhjZ3nJ-)
