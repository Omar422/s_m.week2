# s_m.week2
// C++ code
//
#include <Servo.h>

int degree = 0;

int value = 0;

Servo servo_5;

Servo servo_6;

Servo servo_9;

Servo servo_10;

Servo servo_11;

void setup()
{
  pinMode(A0, INPUT);
  servo_5.attach(5, 500, 2500);

  servo_6.attach(6, 500, 2500);

  servo_9.attach(9, 500, 2500);

  servo_10.attach(10, 500, 2500);

  servo_11.attach(11, 500, 2500);

}

void loop()
{
  value = analogRead(A0);
  degree = map(value, 0, 1023, 0, 180);
  servo_5.write(degree);
  servo_6.write(degree);
  servo_9.write(degree);
  servo_10.write(degree);
  servo_11.write(degree);
  delay(10); // Delay a little bit to improve simulation performance
}
