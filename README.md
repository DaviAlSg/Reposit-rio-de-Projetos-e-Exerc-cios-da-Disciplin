# Reposit-rio-de-Projetos-e-Exerc-cios-da-Disciplin
-
-
# Exercicio_em_Sala_1 : Programa BLINK
-
https://github.com/DaviAlSg/Exercicio_em_Sala_1/tree/main

# Exercicio_em_Sala_2 : Luzes de sinalização de Garagem
-
https://github.com/DaviAlSg/Exercicio_em_Sala_2-Luzes-de-sinaliza-o-de-Garagem/blob/main/README.md
-
# Exercicio_em_Sala_3 : Luzes de sinalização de Garagem
-
-
https://github.com/DaviAlSg/Exercicio_em_Sala_3-Luzes-de-sinaliza-o-de-Garagem/blob/main/README.md
-
-
# Exercicio_em_Casa_1 : Ligar e desligar o LED com o botão
-
-
https://github.com/DaviAlSg/Exercicio_em_Casa_1-Ligar-e-desligar-o-LED-com-o-bot-o/blob/main/README.md
-
-
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

# Projeto_Final_de_Disciplina
-
-
![Editing Components (5)](https://github.com/user-attachments/assets/d251a4d8-96d5-4a81-b2b7-9fc3378847a8)
-
-
# Códigos
-
-

int LED = 8;
void setup() {
  Serial.begin(9600);
  pinMode(LED, OUTPUT);
}
void loop() {
  int LDR = analogRead (A0);
  Serial.println(LDR);

  if(LDR<500)
   digitalWrite(LED, HIGH);
   else
     digitalWrite(LED,LOW);

   delay(500);
}

