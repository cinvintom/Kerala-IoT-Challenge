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


# Exp 2 : Traffic Light
>we have done the LED blinking experiment with one LED.Now its time for an upgrade, we use 3 LEDs with different colors to simulate working of an Traffic light

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) LED   
   - Red M5 LED x 1 Nos  
   - Yellow M5 LED x 1 Nos  
   - Green M5 LED x 1 Nos  
     
4) 220 OHM Resistor X 3 Nos  
5) Breadboard  
6) Jumper Wires (Male to Male ) X 4 Nos  

## Circuit Diagram
![traffic light](https://user-images.githubusercontent.com/65575529/147976179-3abaa884-c4fc-4ef0-a4b5-ccb97e9c7502.jpg)

![trafficlight 2](https://user-images.githubusercontent.com/65575529/147979370-63646366-d185-4c54-b813-931a617db978.jpg)



## Code

```
int redled = 8; // initialize digital pin 8.
int yellowled =5; // initialize digital pin 5.
int greenled = 2; // initialize digital pin 2.
void setup()
{
  pinMode(redled, OUTPUT); // set the pin with red LED as “output”
  pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
  pinMode(greenled, OUTPUT);  // set the pin with green LED as “output”
}

void loop()
{
  digitalWrite(greenled, HIGH); // turn on green LED
  delay(5000); // wait 5 seconds

  digitalWrite(greenled, LOW); // turn off green LED
  for(int i=0;i<3;i++) // blinks for 3 times
  {
    delay(500); // wait 0.5 second
    digitalWrite(yellowled, HIGH); // turn on yellow LED
    delay(500);
    digitalWrite(yellowled, LOW); // turn off yellow LED
  }
  delay(500);
  digitalWrite(redled, HIGH); // turn on red LED
  delay(5000);
  digitalWrite(redled, LOW); // turn off red LED
}

```

## Output
> The LED is blinked alternatively like a traffic light

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/147979458-9a51dab9-e971-4ce1-92a9-4c6d830328d5.mp4"
frameborder="0" 
 allow="autoplay;"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 3 : LED Chasing Effect
>Lets create something different than just blinking.Now, we are going to do an LED chasing Effect which often we see in billboards composed of colorful LEDs.Lets simulate LED chasing effect.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) LED (Any Color) x 6 Nos  
4) 220 OHM Resistor X 6 Nos  
5) Breadboard  
6) Jumper Wires (Male to Male ) X 7 Nos  

## Circuit Diagram
>![chassingled](https://user-images.githubusercontent.com/65575529/147982393-3f7de39e-75dd-4a33-ad05-b5ce8cf77d57.jpg)


>![chassingled 1](https://user-images.githubusercontent.com/65575529/147984256-e506289e-74b1-493e-bf39-91e353162bc2.jpg)


## Code

```
int BASE = 2; // the I/O pin for the first LED
int NUM = 6; // number of LEDs
void setup()
{
  for(int i= BASE; i < BASE + NUM; i++)
  {
    pinMode(i,OUTPUT);   // set I/O pins as output
  }
}

void loop()
{
  for(int i = BASE; i < BASE+NUM; i++)
  {
    digitalWrite(i, LOW);   // set I/O pins as “low”, turn off LEDs one by one.
    delay(200);            // delay
  }
  for(int i = BASE; i < BASE+NUM; i++)
  {
    digitalWrite(i, HIGH);   // set I/O pins as “high”, turn on LEDs one by one.
    delay(200);
  }
}

```

## Output
> The LEDs are turning ON and OFF  one by one  giving a chassing effect.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/147984271-15c6ac84-86ce-4f27-a67e-bfb62ce1d0c4.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 4 : Button Controlled LED
>In this expiriment we are going to learn how to add a Button Switch as INPUT in arduino circuit.

## Button Switch
>The Button is called pushbutton, tactile button or momentary switch, It is a basic and simple component used in arduino to give an INPUT.
### Pinout
>Button switch usually have four pins.  
>BUT These pins are internally connected in pairs, So we only need to use TWO of the four pins, WHICH ARE NOT INTERNALLY CONNECTED
### Working
#### When the button is not pressed
>pin A is NOT connected to pin B
><img src="https://user-images.githubusercontent.com/65575529/149669471-5a0970f1-f04e-42d5-ab77-c44ec2adbb98.jpg" width="200" />
#### When the button is pressed
>pin A is connected to pin B
><img src="https://user-images.githubusercontent.com/65575529/149669498-5c8db0f6-dd25-477a-a045-52c9e8fa94b9.jpg" width="200" />
#### IN arduino
>When using in a arduino circuit  
>One button's pin is connected to VCC or GND. The other pin is connected to an Arduino pin.  
>By reading the state of Arduino's pin(configured as INPUT pin),we can detect the button is PRESSED or NOT

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Red M5 LED x 1 Nos  
4) 220 OHM Resistor X 1 Nos  
5) 10k OHM Resistor X 1 Nos  
6) Breadboard  
7) Jumper Wires (Male to Male ) X 6 Nos  

## Circuit Diagram
### Circuit
>![wQGca_3102_1628160139](https://user-images.githubusercontent.com/65575529/149670082-71b1ec34-9ced-416d-a37c-35e51eebf66f.png)

### Breadboard Connection
>![button_switch_1](https://user-images.githubusercontent.com/65575529/149670135-5faed472-4734-4c47-a3e3-4448e6710812.jpg)
>![bswitch3](https://user-images.githubusercontent.com/65575529/149671192-804e6557-ffc0-44b4-a297-2e7177c003e8.jpg)

## Code

```
int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val

void setup()
{
  pinMode(ledpin,OUTPUT);// set LED pin as “output”
  pinMode(inpin,INPUT);// set button pin as “input”
}

void loop()
{
  val=digitalRead(inpin);// read the level value of pin 7 and assign to val
  if(val==LOW)// check if the button is pressed, if yes, turn on the LED
  {
    digitalWrite(ledpin,LOW);
  }
  else
  {
    digitalWrite(ledpin,HIGH);
  }
}

```

## Output
> The LED turns ON when the Button switch is PRESSED and turns OFF when the button is released.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/149671162-1ec5bcbf-2e64-4d7f-8e36-45534cfa6994.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

