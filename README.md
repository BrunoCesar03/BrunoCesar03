int e1=6;         // Sensor caixa baixa 
int e2=4;         // Sensor caixa media
int e3=3;         // Sensor caixa alta
int k1=11;         // Sopro
int k2=12;         // Esteira de desvio
int ts=500;       // Tempo do sopro
int td=1000;      // Tempo do desvio 

int sensor1=0;
int sensor2=0;
int sensor3=0;


void setup() {
  // put your setup code here, to run once: // Coloque seu codigo de configuracao aqui para rodar uma vez
pinMode(sensor1, INPUT);
pinMode(sensor2, INPUT);
pinMode(sensor3, INPUT);
pinMode(k1, OUTPUT);      //SOPRO
pinMode(k2, OUTPUT);      //DESVIO
}

void loop() {
  // put your main code here, to run repeatedly: // Coloque seu codigo principal aqui para ser executado repetidamente
  
sensor1 = digitalRead(e1);
sensor2 = digitalRead(e2);
sensor3 = digitalRead(e3);


 // Aciona soprador caixa fora de padão

if
// MEDIA  &      BAIXA        & ALTA 
((sensor2==1)&&(sensor1==1)&&(sensor3==0)) // Se somente o sensor de caixa baixa e media ser sensibilizado, o sopro atua por 0,5 segundos
{digitalWrite(k1, HIGH); //SOPRO

delay(ts); // Tempo do sopro

digitalWrite(k1, LOW); // Desliga sopro

}

else{
digitalWrite(k1, LOW);
}







// Aciona esteira de desvio

if 
((sensor1==1)&&(sensor2==1)&&(sensor3==1)) // se os sensores de caixa baixa, média, e alta forem sensibilizados a esteira de desvio liga por 1 segundo
{digitalWrite(k2, HIGH); //DESVIO

delay(td); // tempo do desvio

digitalWrite(k2, LOW); // desliga desvio
}
else
{digitalWrite(k2, LOW);
  
  }
// no simulador ligue o "S CX BX" e o "S CX ALT" mantendo pressionado, no "S CX MD" basta um pulso para funcionar






}
