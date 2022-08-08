# Getting Started with PlatformIO on Wio Terminal

Eventhough Arduino IDE is the most famous platform for Arduino programming and development, there are other alternatives as well which offers better features. [PlatformIO IDE](https://platformio.org) is one of those where it enriches your development experience. PlatformIO supports some of the most popular [IDEs and text editors](https://docs.platformio.org/en/latest/integration/ide/index.html) as an extension/ plugin. In this wiki, we will use PlatformIO extension with Microsoft Visual Studio Studio to help you get started developing applications for Wio Terminal!

## What is PlatformIO?

[PlatformIO](https://platformio.org) is a cross-platform, cross-architecture, multi-framework professional IDE tool for embedded system and software engineers who write embedded applications. By providing a universal IDE interface using PlatformIO, you are able to program your hardware in a more developer-friendly way!

<div align=center><img width=400 src="https://files.seeedstudio.com/wiki/platformIO/platformIO.png"/></div>

## Set up PlatformIO for Wio Terminal

- **Step 1.** Download and install [Microsoft Visual Studio Code](https://code.visualstudio.com) according to your operating system

- **Step 2.** Open VS Code, click **Extensions** from the left navigation pane, type **platformio** in the search bar and click **Install**

<div align=center><img width=1000 src="https://files.seeedstudio.com/wiki/K1100-pio/1.png"/></div>

- **Step 3.** Now you will see a new icon appear on left navigation pane. Click on it, click **Open** and click **+ New Project**

<div align=center><img width=1000 src="https://files.seeedstudio.com/wiki/K1100-pio/2.png"/></div>

- **Step 4.** Fill in a project name, select **Seeeduino Wio Terminal** as the Board and Framework as **Arduino** and click **Finish**

<div align=center><img width=500 src="https://files.seeedstudio.com/wiki/K1100-pio/3.png"/></div>

Wait patiently until the initialization process is finished.

<div align=center><img width=500 src="https://files.seeedstudio.com/wiki/K1100-pio/4.png"/></div>

After the initialization is finished, you will see the following result with **platformio.ini** file already opened for you. This is the platformio configuration file.

<div align=center><img width=1000 src="https://files.seeedstudio.com/wiki/K1100-pio/5.png"/></div>

## Run an example code

Now we will test the PlatformIO installation by running a simple example code 

- **Step 1.** Open **main.cpp** under **src folder**

- **Step 2.** Copy the following codes inside main.cpp

```cpp
#include <Arduino.h>
 
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  Serial.begin(9600);
  pinMode(LED_BUILTIN, OUTPUT);
}
 
// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

- **Step 3.** Click the **Build** button on the bottom toolbar to build the project.

<div align=center><img width=500 src="https://files.seeedstudio.com/wiki/K1100-pio/6.png"/></div>

You can also use the below keyboard combinations to build the project 

    - Windows: CTRL + ALT + B
    - Mac: CMD + SHIFT + B

You will see the following output if the build is successful

<div align=center><img width=650 src="https://files.seeedstudio.com/wiki/K1100-pio/7.png"/></div>

- **Step 5.** Click the **Upload** button on the bottom toolbar to upload the project to Wio Terminal

<div align=center><img width=500 src="https://files.seeedstudio.com/wiki/K1100-pio/8.png"/></div>

You can also use the below keyboard combinations to upload the project 

    - Windows: CTRL + ALT + U
    - Mac: CMD + SHIFT + U

You will see the below output after a successful upload

<div align=center><img width=650 src="https://files.seeedstudio.com/wiki/K1100-pio/9.png"/></div>

Now you will see the built-in LED on the Wio Terminal blinking!