# Hand-Gesture-Recognition-for-Deaf-People-based-on-CMSIS-NN-with-3-Axis-Accelerometer-Sensor #


## This project will provide the required steps, software, hardware and any other materials and apparatus that needed to build the device which prototyping the concept of implementing hand gesture recognition on STM32 NUCLEO-F446RE using CMSIS-NN and CMSIS-DSP with 3 Axis accelerometer, targeting for the one who having hearing disability. ##

***Note: this lab will be made application for Windows users only. MacOS might be similar but Linux user is not.***

============================================================================================

### What's needed? ###

**Equipments:**
1. One STM32 board, we are using NUCLEO-F446RE.
2. One Accelerometer, we are using ADXL337.
3. Mini USB to connect NUCLEO board to host computer.
4. Some jumpers/wires.
5. Breadboard

**Software/Application:**
1. Edge Impulse www.edgeimpulse.com
2. STM32CubeIDE
3. Windows Command Prompt

============================================================================================

### Preparation ###  
(maybe need re-arrange the sequence)

**Part A - Equipment Setup**
1. The ADXL337 bought come in the way that the pins are not soldered on to the ADXL337, solder carefully, make sure there must be gap between each solder to avoid short circuit, and make sure the size of solder is not too big to minimize the noise/resistance. 
2. Connect the ADXL337 with NUCLEO-F446RE using 5 jumpers for 5 pins. As well as connect the NUCLEO to host computer with mini USB. Connection as shown below. >>picture



**Part B - Software Installation / Configuation**
1. Install Node.js Python3, and Edge Impulse CLI tools
    1. go to https://docs.edgeimpulse.com/docs/cli-installation
    2. Under "Installation - macOS and Windows", click the highlighted "Node.js" to download Node.js.
    3. follow the installation instruction for Node.js
    4. Launch "install additional tools for Node.js". You can search this from your Windows start menu. By following this, Python3 should be installed also.

2. Install Edge Impulse CLI tools
    1. Launch the Windows command prompt.
    2. enter the command: npm install -g edge-impulse-cli --force
    3. you should have the CLI tools under npm folder at the path showed in the command prompt
    4. if you failed to install the CLI tools and required to reinstall, remove the existing npm folder first, then only reinstall.

3. Install STM32CubeIDE
    1. You may use STM32CubeMX for pin configuration, and use Keil MDK for coding. But for this project, we will need STM32CubeIDE, because this software consist both of the functions. Also, to use neural network model from Edge Impulse, CPP file is needed. If using MDK Keil, direct rename on the C file to CPP file is not gonna work.
    2. Go to https://www.st.com/en/development-tools/stm32cubeide.html
    3. Select desire software version, and host laptop OS, and download. Afterwards, install the IDE.


#### You are now got your hardware and software ready, next will be the hardware software integration to collect data, debug, and further actions. ####


###Connect Device to Edge Impulse###
