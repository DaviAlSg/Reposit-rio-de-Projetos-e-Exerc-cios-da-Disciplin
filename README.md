# Reposit-rio-de-Projetos-e-Exerc-cios-da-Disciplin


# Exercicio_em_Sala_1 : Programa BLINK

# Arduino feito no Tinkercard

![Editing Components](https://github.com/user-attachments/assets/88dcb5d4-65ef-4320-a103-3dbb5c528b6d)

# Código
void setup() {
pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
digitalWrite(LED_BUILTIN, HIGH);
delay(1000);
digitalWrite(LED_BUILTIN, LOW);
delay(1000);
}

# Exercicio_em_Sala_2 : Luzes de sinalização de Garagem

# Arduino feito no Tinkercard

![Editing Components (1)](https://github.com/user-attachments/assets/84e73e50-2e80-4ef0-bfe6-23a2306c3dea)

# Código

const int ledPin1 = 13;
const int ledPin2 = 9;

const int interval = 500;

void setup() {
Serial.begin(9600);

pinMode(ledPin1, OUTPUT);
pinMode(ledPin2, OUTPUT);

Serial.print("LED 1 está conectado ao pino ");
Serial.println(ledPin1);
Serial.print("LED 2 está conectado ao pino ");
Serial.println(ledPin2);
}

void loop() {
       digitalWrite(ledPin1, HIGH); 
       digitalWrite(ledPin2, LOW);
        Serial.println("LED 1 aceso, LED 2 apagado");
       delay(interval);
       digitalWrite(ledPin1, LOW);
       digitalWrite(ledPin2, HIGH);
       Serial.println("LED 1 apagado, LED 2 aceso");
       delay(interval);
  }

# Exercicio_em_Sala_3 : Luzes de sinalização de Garagem

# Arduino feito no Tinkercard
![Editing Components (2)](https://github.com/user-attachments/assets/b25494d1-c90b-43ad-99ef-c5226afdf348)


# Código

const int ledPin1 = 4;
const int ledPin2 = 5;
const int ledPin3 = 6;

void setup() {
pinMode(ledPin1, OUTPUT);
pinMode(ledPin2, OUTPUT);
pinMode(ledPin3, OUTPUT);
}

void loop() {
digitalWrite(ledPin1, HIGH);
delay(1000);
digitalWrite(ledPin1, LOW);

digitalWrite(ledPin2, HIGH);
delay(1000);
digitalWrite(ledPin2, LOW);

digitalWrite(ledPin3, HIGH);
delay(1000);
digitalWrite(ledPin3, LOW);
}

# Exercicio_em_Casa_1 : Ligar e desligar o LED com o botão (ao contrário)


# Arduino feito no Tinkercard 

![Editing Components (3)](https://github.com/user-attachments/assets/b570be43-491a-4eb8-8e1a-3634712707d8)




# Código
const int buttonPin = 2;
const int ledPin = 13;


// variables will change:
int buttonState = 0;


void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}


void loop() {
  buttonState = digitalRead(buttonPin);
  if (buttonState == HIGH) {
    digitalWrite(ledPin,HIGH);
  } else {
    digitalWrite(ledPin,LOW);
  }
}

# Exercicio_em_Casa_2 :Contagem de pressionamentos de botão

# Arduino feito no Tinkercard




# Código
const int buttonPin = 2;
const int ledPin = LED_BUILTIN;
int buttonPushCounter = 0;
int buttonState = 0;
int lastButtonState = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState != lastButtonState) {
    if (buttonState == HIGH) {
      buttonPushCounter++;
      Serial.println("on");
      Serial.print("Number of button pushes: ");
      Serial.println(buttonPushCounter);
    } else {
      Serial.println("off");
    }
    delay(50);
  }

  lastButtonState = buttonState;
}

