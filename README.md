https://cinvintom.github.io/Kerala-IoT-Challenge/
# Kerala-IoT-Challenge
> "Kerala IoT Challenge 2021" is a program launched by Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala to mold IoT experts in Kerala.
# About Me
>Hello everyone , I am Cinvin Tom, a 3rd-year Computer Science and Engineering student from College of Engineering Chengannur, I  am participating in this IoT challenge to learn more about the IoT and help others to learn IoT and complete the Kerala IoT Challenge 2021.

# Level 1
>In level 1 we are using Arduino for the experiments,
>Arduino is an open-source electronics platform based on easy-to-use hardware and software. It's intended for anyone making interactive projects.  
>I am using Arduino UNO and Arduino IDE from https://www.arduino.cc/en/software for level 1

## Arduino UNO
>![arduino uno](https://user-images.githubusercontent.com/65575529/146658512-36951b05-7ce5-49ee-bada-169fc0a14437.jpg)
>Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over conventional microcontrollers. It comes with pre-tested software and hardware libraries and has an integrated development environment (IDE). Also, it is less expensive & beginner-friendly.

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
>we have done the LED blinking experiment with one LED. Now its time for an upgrade, we use 3 LEDs with different colors to simulate the working of a Traffic light

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
  pinMode(greenled, OUTPUT);  // set the pin with green LED as “output”
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
> The LED has blinked alternatively like a traffic light

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/147979458-9a51dab9-e971-4ce1-92a9-4c6d830328d5.mp4"
frameborder="0" 
 allow="autoplay;"
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 3 : LED Chasing Effect
> Let's create something different than just blinking. Now, we are going to do an LED chasing Effect which often we see in billboards composed of colorful LEDs.Let us simulate the LED chasing effect.

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
    pinMode(i,OUTPUT);   // set I/O pins as output
  }
}

void loop()
{
  for(int i = BASE; i < BASE+NUM; i++)
  {
    digitalWrite(i, LOW);   // set I/O pins as “low”, turn off LEDs one by one.
    delay(200);            // delay
  }
  for(int i = BASE; i < BASE+NUM; i++)
  {
    digitalWrite(i, HIGH);   // set I/O pins as “high”, turn on LEDs one by one.
    delay(200);
  }
}

```

## Output
> The LEDs are turning ON and OFF  one by one giving a chasing effect.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/147984271-15c6ac84-86ce-4f27-a67e-bfb62ce1d0c4.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 4 : Button Controlled LED
>In this experiment we are going to learn how to add a Button Switch as INPUT in the Arduino circuit.

## Button Switch
>The Button is called a pushbutton, tactile button, or momentary switch, It is a basic and simple component used in Arduino to give an INPUT.
### Pinout
>Button switch usually has four pins.  
>BUT These pins are internally connected in pairs, So we only need to use TWO of the four pins, WHICH ARE NOT INTERNALLY CONNECTED
### Working
#### When the button is not pressed
>pin A is NOT connected to pin B
><img src="https://user-images.githubusercontent.com/65575529/149669471-5a0970f1-f04e-42d5-ab77-c44ec2adbb98.jpg" width="200" />
#### When the button is pressed
>pin A is connected to pin B
><img src="https://user-images.githubusercontent.com/65575529/149669498-5c8db0f6-dd25-477a-a045-52c9e8fa94b9.jpg" width="200" />
#### IN Arduino
>When using in an Arduino circuit  
>One button's pin is connected to VCC or GND. The other pin is connected to an Arduino pin.  
>By reading the state of Arduino's pin(configured as INPUT pin), we can detect the button is PRESSED or NOT

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

# Exp 5 : Buzzer
>In this experiment we are going to learn how to add a Buzzer as OUTPUT in the Arduino circuit for sound feedback.

## Buzzer
![gHdtK_3102_1628160269](https://user-images.githubusercontent.com/65575529/149671618-35d7097a-d164-4325-a644-529410974dd6.png)
>An Arduino buzzer is also called a piezo buzzer. It’s a tiny speaker that you can connect to an Arduino board and make it sound the tone we set. The buzzer generates sound based on the reverse of the piezoelectric effect. Buzzers are used to make beep alarms and tones. They were designed to help technicians integrate their alarm systems or other automated systems for sound feedback.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Buzzer x 1 Nos   
4) Breadboard  
5) Jumper Wires (Male to Male ) X 2 Nos  

## Circuit Diagram
### Circuit
>![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/65575529/149671705-09f74ef2-2603-4125-b601-3521b1615cb0.png)

### Breadboard Connection
>![buzzer1](https://user-images.githubusercontent.com/65575529/149672332-02ef2746-f2c2-4349-b977-35b1f3c9e248.jpg)

>![buzzer2](https://user-images.githubusercontent.com/65575529/149672335-304f9762-5950-42cc-b67f-b827ccc0457e.jpg)


## Code

```
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup()
{
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
}
void loop()
{
  digitalWrite(buzzer,HIGH);// produce sound
}


```

## Output
> The buzzer starts making a sound when the Arduino is connected to the power supply. When the RESET switch has pressed the buzzer restarted after 1 sec.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/149672340-460ec5e3-e8bc-4bc4-b402-690c4b059678.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 6 : RGB LED
>In this experiment we are going to learn how to add an RGB LED as OUTPUT in the Arduino circuit.

## RGB LED
>![tGwYE_3102_1628160546](https://user-images.githubusercontent.com/65575529/149672732-9c578614-0fb0-47fd-b0e5-5dd12d753cf8.png)
>  The RGB led consists of three different led’s, from the name you can guess that these LEDs are red, green, and blue. We can obtain many other colors by mixing up these colors.   
>The Arduino has an analog write function which will help us in obtaining different colors for Arduino RGB led.
#### Pinout 
>![image](https://user-images.githubusercontent.com/65575529/149673473-7e9c06eb-8cd8-44b6-9016-ba84e8574ca4.png)


## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) RGB LED x 1 Nos   
4) Breadboard  
5) Jumper Wires (Male to Male ) X 5 Nos  

## Circuit Diagram
### Circuit
>![rgb2](https://user-images.githubusercontent.com/65575529/149672805-1a75bdcd-2f97-4a4d-acb1-b2baff04cf27.png)

### Breadboard Connection
>![rgb1](https://user-images.githubusercontent.com/65575529/149674781-c9d78e24-3007-4103-9e73-8fb5457065fa.jpg)


>![rgb4](https://user-images.githubusercontent.com/65575529/149674747-b65afd18-76ba-4c6f-addd-4694e8d95b2b.jpg)


## Code

```
int redpin = 11; //select the pin for the red LED
int bluepin = 10; //select the pin for the blue LED
int greenpin = 9; //select the pin for the green LED
int val;

void setup()
{
  pinMode(redpin,OUTPUT);
  pinMode(redpin,OUTPUT);
  pinMode(redpin,OUTPUT);
  Serial.begin(9600);//to begin serial communication
}

void loop()
{
  for(val=0;val<255;val++)
  {
    analogWrite(11, val);
    analogWrite(10, 255-val);
    analogWrite(9, 128-val);
    delay(1);
  }
  Serial.println(val, DEC);
}

```

## Output
> The RGB LED started blinking in different colors.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/149674754-a64eba40-5a82-42ab-af19-88cd843172a8.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 7 : LDR Light Sensor
>In this experiment, we are going to learn how to use an LDR light sensor to create an Arduino circuit that gives a response to variation in light.

## LDR Light Sensor
>![ldr 1](https://user-images.githubusercontent.com/65575529/151667911-be762301-51fe-4416-becd-a3f65e94bee2.jpg)

>  An LDR is a component that has a (variable) resistance that changes with the light intensity that falls upon it. This allows them to be used in light sensing circuits. Light Dependent Resistors (LDR) is also called photoresistors. They are made of high-resistance semiconductor material.

#### working 
> when light falls on the LDR then the resistance decreases and increases in the dark. When it is placed in a dark room then the resistance will be infinite(high) and act as an open circuit. As the intensity of light increases, the resistance will decrease and act as a closed circuit.


## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Red M5 LED x 1 Nos  
4) 10KΩ Resistor x 1 Nos  
5) 220Ω Resistor x 1 Nos  
6) Breadboard  
7) Jumper Wires (Male to Male ) X 5 Nos  

## Circuit Diagram
### Circuit
>![H7NxL_3102_1628756051](https://user-images.githubusercontent.com/65575529/151670509-864c40c6-439c-4711-94af-16d9c7228f53.png)

### Breadboard Connection
>![ldr 2 circuit](https://user-images.githubusercontent.com/65575529/151670527-c460fa60-5adb-4395-a6ce-93019059dd40.jpg)


>![ldr3](https://user-images.githubusercontent.com/65575529/151670631-7baaf449-e905-463d-86de-c6b130c393aa.jpg)



## Code

```
int potpin = 0; // initialize analog pin 0, connected with photovaristor
int ledpin = 11; // initialize digital pin 11
int val = 0; // initialize variable val
void setup()
{
  pinMode (ledpin,OUTPUT); // set digital pin 11 as “output”
  Serial.begin(9600); //to begin serial communication
}

void loop()
{
  val = analogRead(potpin); // read the value of the sensor and assign it to val
  Serial.println(val); // display the value of val
  analogWrite(ledpin,val/4); // set up brightness（maximum value 255）
  delay(10); // wait for 0.01s
}

```

## Output
> The brightness of the LED reduced as the intensity of the light source increased. When the light source is removed, the LED lights up in full brightness.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151670993-696ff0b8-09d6-4fdb-b587-78ca38bed8ee.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 8 : Flame Sensor
>In this experiment, we are going to learn how to use an Infrared Receiver (IR) for detecting Flame.

## Infrared Receiver
>![IDVWv_3102_1628756405](https://user-images.githubusercontent.com/65575529/151671511-7b5e1b94-bf74-4db7-b43d-189320c9250e.png)

>  the receiver outputs a code to uniquely identify the infrared signal that it receives.


## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Infrared Receiver x 1 Nos  
4) 10KΩ Resistor x 1 Nos  
5) Buzzer x 1 Nos  
6) Breadboard  
7) Jumper Wires (Male to Male ) X 5 Nos  

## Circuit Diagram
### Circuit
>![gI9NP_3102_1628756600](https://user-images.githubusercontent.com/65575529/151671626-cfaba30b-6e2b-4b3d-a103-b1eebe438fc5.png)


### Breadboard Connection
>![FLAME 2](https://user-images.githubusercontent.com/65575529/151672392-92191614-7056-4475-9964-e605616fca5c.jpg)

>![flame 3](https://user-images.githubusercontent.com/65575529/151683409-1f2b76b2-c4d2-4a2c-87e6-49777f861bfd.jpg)





## Code

```
int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
void setup() 
{
   pinMode(Beep,OUTPUT);// set LED pin as “output”
   pinMode(flame,INPUT);// set buzzer pin as “input”
   Serial.begin(9600);// set baud rate at “9600”
} 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=20)// when the analog value is larger than 20, the buzzer will buzz
  {  
    digitalWrite(Beep,HIGH); 
  }
  else 
  {  
     digitalWrite(Beep,LOW); 
  }
   delay(500); 
}

```

## Output
> When the FLAME source came near the IR sensor the buzzer started to make a sound.

<iframe width="400" height="300"
src="https://user-images.githubusercontent.com/65575529/151684443-2c4f57e9-4e8f-44bc-b2cf-f835c27b82b9.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 9 : LM35 Temperature Sensor
>In this experiment, we are going to learn how to use an LM35 Temperature Sensor for measuring room temperature.

## LM35 Temperature Sensor
>![image](https://user-images.githubusercontent.com/65575529/151673742-f6a31e35-ebfe-48e6-a76b-0653e7b5dce8.png)

>  LM35 temperature sensor can produce different voltage by different temperature  
>When temperature is 0 ℃, it outputs 0V;  
>if increasing 1 ℃, the output voltage will increase 10 mv.  
>The output temperature is 0℃～100℃,  
>the conversion formula is as follows: 
>![image](https://user-images.githubusercontent.com/65575529/151673867-c3e1eadd-f27b-4bf4-8792-ccbb47e7037a.png)
#### Note
>LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) LM35 x 1 Nos  
4) Breadboard  
5) Jumper Wires (Male to Male ) X 3 Nos  

## Circuit Diagram
### Circuit
>![image](https://user-images.githubusercontent.com/65575529/151673942-75daf01d-0707-402d-b957-3325039c7ebb.png)


### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151674085-59da70d2-a98d-43bd-b7d0-2c9f7570f7aa.png)


>![temp3](https://user-images.githubusercontent.com/65575529/151683450-1de38a2c-3f19-452d-9f2b-53e37576930d.jpg)




## Code

```
int potPin = 0;  // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
  Serial.begin(9600);
}

void loop()
{
  int val; // define variable
  int dat; // define variable
  val = analogRead(potPin); // read the analog value of the sensor and assign it to val
  dat = (125*val)>>8; // temperature calculation formula
  Serial.print("Tep"); // output and display characters beginning with Tep
  Serial.print(dat); // output and display value of dat
  Serial.println("C"); // display “C” characters
  delay(500); // wait for 0.5 second
}


```

## Output
> When the Arduino starts working the temperature of the room is displayed on the serial monitor in celsius.    
> ![image](https://user-images.githubusercontent.com/65575529/151675250-76e90eb7-c362-4a2d-ac40-b90a4c9fd25d.png)



<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151684495-220477f0-c9b4-4df6-b758-d10d72f11e60.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 10:IR Remote Control Using TSOP
>In this experiment, we are going to learn how to use a remote to control the circuit.


## TSOP - IR Receiver Module
>![image](https://user-images.githubusercontent.com/65575529/151675570-eb826f93-7238-4025-9d13-d3c5a1eef8a4.png)    
>![image](https://user-images.githubusercontent.com/65575529/151678043-ba801690-967b-4415-93ec-00c844af8c58.png)


>  The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.
#### Working
>  The built-in receiver converts the light signal it received from the sender into feeble electrical signal. The signal will be amplified by the IC amplifier. After automatic gain control, band-pass filtering, demodulation, wave shaping, it returns to the original code. The code is then input to the code identification circuit by the receiver's signal output pin.

## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) Infrared Remote Controller(We can use TV Remote or any other remote) x 1 Nos
4) Infrared Receiver  
5) LED   
   - Red M5 LED x 1 Nos  
   - Yellow M5 LED x 1 Nos  
   - Green M5 LED x 1 Nos 
6) 220Ω Resistor x 3 Nos
8) Breadboard  
9) Jumper Wires (Male to Male ) X 8 Nos  

## Circuit Diagram

### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151678629-220f7910-b590-4440-9179-3abb60b4d8f4.png)

>![remote 4](https://user-images.githubusercontent.com/65575529/151684514-1646630e-31b5-4229-8ad2-528b3dbef0e9.jpg)





## Code

```
#include <IRremote.h>
int RECV_PIN = 9;

int red = 5;
int green = 6;
int yellow = 3;
int val=85;

bool r=false;
bool w=false;
bool y=false;
bool a=false;

IRrecv irrecv(RECV_PIN);
decode_results results;

void setup() 
{
  Serial.begin(9600);
  pinMode(red, OUTPUT);
  pinMode(green, OUTPUT);
  pinMode(yellow, OUTPUT);
  irrecv.enableIRIn();
  irrecv.blink13(true); 
}
void loop() 
{
  if (irrecv.decode(&results)) 
   {
     Serial.println(results.value,HEX);
     delay(100);
     
     if(results.value==0x8041A701)
     {
        r=!r;
        digitalWrite(red, r);
        
     }
     
     else if(results.value==0x8041A702)
     {
        w=!w;
        digitalWrite(green, w);
        
     }
     else if(results.value==0x8041A703)
     {
        y=!y;
        digitalWrite(yellow, y);
        
     }  
    
     else if(results.value==0x80412704)
     {
        if(r||w||y)
        {
          a=true;
          r=false;
          w=false;
          y=false;
                    
          Serial.println("a=true");
        }
        a=!a;
        digitalWrite(red, a);
        digitalWrite(green, a);
        digitalWrite(yellow, a);        
        if(a)
        {
         r=true;
         w=true;
         y=true; 
        }
     }
         
     irrecv.resume(); // Receive the next value
   }
  
}  
```

## Output
> When one key is pressed in the remote corresponding led turns ON. again the same key is pressed the LED turns OFF.


<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151683786-cdffd466-a9c8-4b43-a6db-3faf24b1b38e.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 11 :Potentiometer analog Value Reading
>In this experiment, we are going to learn how to read analog value from Potentiometer.

## Potentiometer 
>![image](https://user-images.githubusercontent.com/65575529/151678925-f5a5fe62-ea4f-4ea0-8c99-db7b2e31f67b.png)

>  a variable resistor with a third adjustable terminal. The potential at the third terminal can be adjusted to give any fraction of the potential across the ends of the resistor. 
>  Potentiometer made using plastic and having a small size  is called Preset  
>  ![image](https://user-images.githubusercontent.com/65575529/151679011-acf02dd0-4f5d-4b44-bf63-ffe08318fcc8.png)


## Components Required
1) Arduino Uno Board  
2) USB Cable  
3) 10KΩ Potentiometer x 1 Nos  
4) Breadboard  
5) Jumper Wires (Male to Male ) X 3 Nos  

## Circuit Diagram
### Circuit
>![image](https://user-images.githubusercontent.com/65575529/151679099-8a5335a1-0e2d-4b64-af2a-315001ca23bb.png)

### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151679178-af5ed399-7f74-4359-9f4c-d7d0c74945ee.png)

>![poten1](https://user-images.githubusercontent.com/65575529/151683498-c97cb31a-7daf-4d3d-b20a-7cf26c5a5d21.jpg)




## Code

```
int potpin = 0; // initialize analog pin 0
int ledpin = 13; // initialize digital pin 13
int val=0; // define val, assign initial value 0
void setup()
{
  pinMode (ledpin, OUTPUT); // set digital pin as “output”
  Serial.begin(9600); // set baud rate at 9600
}
void loop()
{
  digitalWrite(ledpin, HIGH); // turn on the LED on pin 13
  delay(50); // wait for 0.05 second
  digitalWrite(ledpin, LOW); // turn off the LED on pin 13
  delay(50);
  val = analogRead(potpin); // read the analog value of analog pin 0, and assign it to val 
  Serial.println(val); // display val’s value
}

```

## Output
> As the knob of the potentiometer turns the value displaying on the serial monitor is also changing.    
>![image](https://user-images.githubusercontent.com/65575529/151679523-3b0734c4-0b4d-4b4a-b58d-ff25fe054e52.png)



<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151683741-3aac358d-849f-4be4-aa80-061f24833a2d.mp4" frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Exp 12 : 7 Segment Display
>In this experiment, we are going to learn how to add an 7 Segment Display as OUTPUT in the Arduino circuit.
  
## 7 Segment Display 
>![image](https://user-images.githubusercontent.com/65575529/151679760-8347a20b-39b6-49aa-a202-ec39e7cacfad.png)

> 7 segment display is basically a combination of 7 different LED arranged in a manner so that we can use their combination to produce numerical values from 0 to 9.  
>  Some of them have the 8th segment which helps to display decimal points.

### pinout
>![image](https://user-images.githubusercontent.com/65575529/151679909-68085635-9a66-434a-b7bb-05409651febe.png)

## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) 1-digit LED Segment Display x 1 Nos  
4) 220Ω Resistor x 8 Nos  
5) Breadboard  
6) Jumper Wires (Male to Male ) X 9 Nos  

## Circuit Diagram
### Circuit
>![image](https://user-images.githubusercontent.com/65575529/151679961-1779ff0d-8c5d-4728-a084-9254c008e876.png)

### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151680287-fbc6b560-4364-46f0-ab50-5fe725bf2815.png)  
>![7,2](https://user-images.githubusercontent.com/65575529/151683526-e9723405-2fd4-4264-9166-c5a7263c75f4.jpg)





## Code

```
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}
```

## Output
> As the power supply is connected in the circuit, the 7 segment display started to count from 0 to 9.   



<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151683685-d111f43e-1073-457c-91a7-eaff375b8dcb.mp4" frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

                        
                        
# ASSIGNMENTS   

## Assignment 1
>Create an automatic night lamp model using LDR and LED  
### Automatic Night Lamp



## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) LDR module x 1 Nos  
4) LED x 1 Nos 
5) 220Ω resistor x 1 Nos  
6) 10kΩ resistor x 1 Nos 
7) Breadboard  
8) Jumper Wires (Male to Male ) X 12 Nos  

## Circuit Diagram

### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151683176-471a85ae-dc4a-4c48-bb6c-6c2507433fd9.png)
>![ass1](https://user-images.githubusercontent.com/65575529/151693416-08bde0c7-8dff-4061-9250-534b8562e0fd.jpg)





## Code

```
int potpin=0;// initialize analog pin 0, connected with photovaristor
int ledpin=11;// initialize digital pin 11, 
int val=0;// initialize variable val
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
Serial.begin(9600);// set baud rate at “9600”
}
void loop()
{
val=analogRead(potpin);// read the value of the sensor and assign it to val
Serial.println(val);// display the value of val
if(val<=(255))
  digitalWrite(ledpin,LOW);// set up brightness（maximum value 255）
else
  digitalWrite(ledpin,HIGH);
  delay(10);// wait for 0.01 
}
```

## Output
> When the room becomes dark LED turns ON automatically and turns OFF when dark is over.    



<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151692616-0d13c05c-1a18-4251-a976-fa7944d0c1e7.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Assignment 2
>Create a Digital Dice using 7 Segment Display and Push Button  
### Digital Dice
>![image](https://user-images.githubusercontent.com/65575529/151681505-52062599-1fe2-453e-b875-ab2141fe20cc.png)


## Components Required
1) Arduino Uno Board  
2) USB Cable 
3) 1-digit LED Segment Display x 1 Nos  
4) 220Ω resistor x 8 Nos  
5) 10kΩ resistor x 1 Nos 
6) Breadboard  
7) Jumper Wires (Male to Male ) X 12 Nos  

## Circuit Diagram

### Breadboard Connection
>![image](https://user-images.githubusercontent.com/65575529/151682268-bec18561-ab13-43a3-a045-6f10e4f995b3.png)
>![ass2 3](https://user-images.githubusercontent.com/65575529/151692735-6f662fae-a82c-47fe-ae2a-cdfdff0ec321.jpg)




## Code

```

int button = 2; //specifying button
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
long num;
int buttonstate;


void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}

void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
buttonstate = digitalRead(button);
if(buttonstate == HIGH)
{
  num = random(1,7); //Generate random number from 1 to 6.
  if (num == 1)
    digital_1();// display number 1
  if (num == 2)
    digital_2();// display number 2
  if (num == 3)
    digital_3();// display number 3
  if (num == 4)
    digital_4();// display number 4
  if (num == 5)
    digital_5();// display number 5
  if (num == 6)
    digital_6();// display number 6
 }
}
```

## Output
> When the button is pressed a random number is displayed in the 7 segment display.   



<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/65575529/151693045-b3247f5b-57ae-4514-b706-805f41e04b0d.mp4"
frameborder="1" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
