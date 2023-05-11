## Integrantes
- Matias Díaz
- Mateo Ciotti
- Franco Beltrán
- 


## Proyecto


<img src="https://github.com/0Mateciotti/SPD-Jodo-2/blob/main/Jodo%202/Imagenes/adasd.PNG?raw=true" width="800"/>

## Descrpcion
Este programa enciende y apaga las luces de un semaforo con sus respectivos tiempo junto con un buzzer que serviria para gente con problemas de vista


## Funcion principal

~~~ C (lenguaje en el que esta escrito)
// C++ code
//

#define ESTACION_1 13
#define ESTACION_2 12
#define ESTACION_3 11
#define ESTACION_4 10
#define SEGMENTOA 7
#define SEGMENTOB 6
#define SEGMENTOC 3
#define SEGMENTOD 4
#define SEGMENTOE 5
#define SEGMENTOF 8
#define SEGMENTOG 9
#define BUZZER 2


void setup()
{
  pinMode(2,INPUT);
  Serial.begin(9600);
  
  for(int i =2;i<=13;i++){
  
  	pinMode(i,OUTPUT);	
  
  } 
}

void loop()
{	
  Serial.println(digitalRead(A1));
  if(detectarBoton(digitalRead(A1)) == 1){
  
    secuencia();
  }
 	
}	



int secuencia(){
	
  
  	//estacion 1
	digitalWrite(ESTACION_1,HIGH);
	digitalWrite(SEGMENTOB,HIGH);
  	digitalWrite(SEGMENTOC,HIGH);
  	Serial.println("Llego a la estacion: Constitucion.");
  	tone(2,1000,200);
	    	
  	delay(1000);
  	digitalWrite(ESTACION_1,LOW);
  	digitalWrite(SEGMENTOB,LOW);
  	digitalWrite(SEGMENTOC,LOW);
    delay(1000);
	
  
  	//estacion 2
  	digitalWrite(ESTACION_2,HIGH);
	digitalWrite(SEGMENTOD,HIGH);
  	digitalWrite(SEGMENTOE,HIGH);
  	digitalWrite(SEGMENTOG,HIGH);
  	digitalWrite(SEGMENTOB,HIGH);
 	digitalWrite(SEGMENTOA,HIGH);
  
  	Serial.println("Llego a la estacion: San Juan.");
  
  	tone(2,1000,200);
  
  	delay(1000);
  	digitalWrite(ESTACION_2,LOW);
	digitalWrite(SEGMENTOD,LOW);
  	digitalWrite(SEGMENTOE,LOW);
  	digitalWrite(SEGMENTOG,LOW);
  	digitalWrite(SEGMENTOB,LOW);
 	digitalWrite(SEGMENTOA,LOW);
    delay(1000);
  
  
  
  	//estacion 3 en proceso...
 	digitalWrite(ESTACION_3,HIGH);
	digitalWrite(SEGMENTOB,HIGH);
  	digitalWrite(SEGMENTOC,HIGH);
  	digitalWrite(SEGMENTOG,HIGH);
  	digitalWrite(SEGMENTOD,HIGH);
  	digitalWrite(SEGMENTOA,HIGH);
  	
  	
  	Serial.println("Llego a la estacion: Independencia.");
  	tone(2,1000,200);
  		
  
  
  	delay(1000);
  	digitalWrite(ESTACION_3,LOW);
	digitalWrite(SEGMENTOB,LOW);
  	digitalWrite(SEGMENTOC,LOW);
  	digitalWrite(SEGMENTOG,LOW);
  	digitalWrite(SEGMENTOD,LOW);
  	digitalWrite(SEGMENTOA,LOW);
    delay(1000);
  	
  	//estacion 4
 	digitalWrite(ESTACION_4,HIGH);
	digitalWrite(SEGMENTOB,HIGH);
  	digitalWrite(SEGMENTOC,HIGH);
  	digitalWrite(SEGMENTOG,HIGH);
  	digitalWrite(SEGMENTOF,HIGH); 	
  
  	Serial.println("Llego a la estacion: Moreno");
  	tone(2,1000,200);	
  
  	delay(1000);
  	digitalWrite(ESTACION_4,LOW);
	digitalWrite(SEGMENTOB,LOW);
  	digitalWrite(SEGMENTOC,LOW);
  	digitalWrite(SEGMENTOG,LOW);
  	digitalWrite(SEGMENTOF,LOW);
    delay(1000);
}

int detectarBoton(int boton){

  int retorno;
  
  if(boton == 1){
  
  	retorno = 1;
  
  }else{
  retorno = 0;
    
  }

  return retorno;
}





~~~

## Links
-[ThinkerCad](https://www.tinkercad.com/things/7pXPCxyjQpk-dojo-2/editel?sharecode=IQytHxrYL692Wkem_FyFjY2PSjNzhZThaxvCZEPInLU)
