# Kerala-IoT-Challenge
> "Kerala IoT Challenge 2021" is a program launched by Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala to mold IoT experts in Kerala.
# About Me
>Hello everyone👋, I am Cinvin Tom, a 3rd-year Computer Science and Engineering student from College of Engineering Chengannur, I  am participating in this IoT challenge to learn more about the IoT and help others to learn IoT and complete the Kerala IoT Challenge 2021.

# Level 1
>In level 1 we are using Arduino for the experiments,
>Arduino is an open-source electronics platform based on easy-to-use hardware and software. It's intended for anyone making interactive projects.  
>I am using Arduino UNO and Arduino IDE from https://www.arduino.cc/en/software for level 1

## Arduino UNO
>![arduino uno](https://user-images.githubusercontent.com/65575529/146658512-36951b05-7ce5-49ee-bada-169fc0a14437.jpg)
>Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Arduino Uno Components
>![pin out](https://user-images.githubusercontent.com/65575529/146658693-bcd22880-7c50-4188-a3f3-64237a42d9b6.jpg)

# Exp 1: Hello World LED Blinking
>we are starting our IoT journey by Hello World LED Blinking using the microcontroller Arduino UNO

## Components Required
1) Arduino Uno Board
2) USB Cable
3) LED (Any Color) x 1 Nos
4) 220 OHM Resistor X 1 Nos
5) Breadboard
6) Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram
>![image](https://user-images.githubusercontent.com/65575529/146659142-75ecce8f-be09-4d77-a3a5-df4cb21e082e.png)

>![cir](https://user-images.githubusercontent.com/65575529/146659971-4683808c-2495-493e-b4d9-8b30ebb6f8ea.jpg)


## Code

```
 int ledPin = 9; //for define digital pin 9
void setup() {
 
 pinMode(ledPin, OUTPUT);//define ledPin as an OUTPUT
 
}

void loop() {
  
 digitalWrite(ledPin, HIGH);//set LED on
 delay(1000);//wait for 1000 millisecond or 1 second
 digitalWrite(ledPin, LOW);//set the LED off
 delay(1000);
 
}

```

## Output
> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/146659989-f970ace2-8ddc-40f1-a1d1-3a8c3bb18319.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

