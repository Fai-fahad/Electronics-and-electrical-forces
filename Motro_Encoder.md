![The suspension system is responsible for stability and balance and is used in the chassis and wheelhouse to maintain the stability of the car on roads and turns  (13)](https://user-images.githubusercontent.com/101976302/186574776-ecaf4bfa-2dd6-4fb6-aa18-1d243a15836b.png)
![The suspension system is responsible for stability and balance and is used in the chassis and wheelhouse to maintain the stability of the car on roads and turns  (14)](https://user-images.githubusercontent.com/101976302/186577817-9aa25992-d9b9-4adf-aa84-f980bb46ce75.png)
# We need
###  1.Motor with encoder

### 2.Arduino board ( I used arduino Uno)

### 3.Computer

### 4.Battery or DC voltage supply

### 5.Encoder library , download from https://www.pjrc.com/teensy/td_libs_Encoder.html or from the zip file attached

### 6.Background : https://en.wikipedia.org/wiki/Rotary_encoder

### 7.( A little experiment I did with multimeter :

### power the encoder with 2 AA battery, attach multimeter GND cable to GND of the battery , and multimeter RED cable to the C1 or C2 output of the encoder.

### As you turn the motor slowly, you can see that the output voltage of C1 and C2 change from 0V to 3V.
### If you have 2 multimeter, attach C1 and C2 each to a multimeter, then turn the multimeter slowly you can see the value of multimeter change from 3V-3V, 0V-3V,0V-0V,3V-3V, which is the pulse according the background theory)
### [FB237MUIXLAD6OS.zip](https://github.com/Fai-fahad/Electronics-and-electrical-forces/files/9421402/FB237MUIXLAD6OS.zip)
![13](https://user-images.githubusercontent.com/101976302/186577917-9df617ea-d6a5-445e-9324-190926b7ff7c.png)
# The DC motor with encoder has 6 wires :

### 2 wires to power the motor (Often labeled as : M1, M2 , motor power ...)

###  2 wires to power the encoder (often labeled GND and 3.3V)

###  2 wires to send signal of position to the microcontroller (Arduino) (labeled as encoder output or C1 & C2)

###  First you will connect 2 wires to power the encoder to Arduino Gnd And Vcc 3.3V (in my version of encoder motor, the encoder led turn on when I connected the wire power)

### Then connect 2 wires signal of the encoder to 2 pins with interrupt of Arduino , (which is pin 2 and 3 of the Arduino Uno)

###  You can turn the motor by hand or connect 2 motor wires to the battery to rotate the motor.

###  Note : normal pin will still work at low speed when you turning the motor by hand, however, when you run the motor with the battery and the motor rotates at high speed, the encoder will misread the position of the motor, result in duplication while reading. Using interrupt pin with the library prevent the encoder from making this mistake (in my experiment it was quite accurate when read the motor with interrupt pin, the only time it make a mistake is in the end when I stop the motor and the motor slowing down, that time the reading was duplicate for a few position).
![14](https://user-images.githubusercontent.com/101976302/186577934-50248819-6c19-4728-b825-4bece4c1b8cb.png)
## After the installed the library, you can open File/Example/Encoder/Basic to run the code , or copy paste this code in :
## https://www.instructables.com/Motor-With-Encoder-How-to-Read-Input-Value-From-En/#:~:text=power%20the%20encoder%20with%202%20AA%20battery%2C%20attach,C1%20and%20C2%20change%20from%200V%20to%203V.


![15](https://user-images.githubusercontent.com/101976302/186577894-24e93be3-b0d5-440f-8925-f10effe9c79e.png)

## After successful with all above step, turn on the serial monitor :

## And first turn the motor with your hand to see that the position is slightly change

## Then run the motor with battery to see that position reading change rapidly as the motor run fast.

## All the steps from this link:
## https://www.instructables.com/Motor-With-Encoder-How-to-Read-Input-Value-From-En/#:~:text=power%20the%20encoder%20with%202%20AA%20battery%2C%20attach,C1%20and%20C2%20change%20from%200V%20to%203V.








