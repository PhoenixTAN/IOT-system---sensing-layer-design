# IOT system--sensing-layer-design

Abstract:
    In this paper, I design the sensing-layer of an Internet Of Things system. 
    
    The task of the sensing-layer is to collect related data of the environment, 
    such as temperature, humidity and light intensity.
    
    For the part of lower computer, I use the RTD-PT100, a thermistor to sense the change of the temperature, 
    PCF8591 to convert analog data to digital data, AT89C51 to process and control, LCD screen to display the temperature info, 
    and COMPIM to send datastream to upper computer. 
    For the part of upper computer, 
    
    Generally, the aforementioned lower computer is a special-purpose computer, 
    like a single chip microcontroller and its peripheral circuit.
    I use Proteus to simulate the lower computer and Keil uVision4 to program the AT89C51 microcontroller.
    Then, the upper computer is a general computer, i.e. a personal computer.
    I use Visual Studio 2017 C# to design the UI.
    For the communication between them, use Virtual Serial Port Driver to create a pair of virtual Serial Ports.
    
Index terms —— RTD-PT100, AT89C51, C#

Software we needed:
    1. Visual Studio 2017 C#.
    2. Proteus 8.0 Professional.
    3. Keil uVision4.
    4. ComAssistant.
    5. Virtual Serial Port Driver.

How to run this project:
    Step1: Use Virtual Serial Port to create a pair of virtual Serial Ports. 
           For example, we create COM2 and COM3.
    Step2: Open the Proteus project and click the run button on the bottom left part of the software.
    Step3: Open the VS2017 project and set the number of serial port of the upper computer.
           In From1.cs[Design], find the widget named "serialPort1" and change the attribute of COM of it.
    Step4: Run the VS2017 program.
    Finish!
    We can monitor the change of tempeture of the environment.
    
