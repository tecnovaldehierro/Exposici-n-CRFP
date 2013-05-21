/*
  Programa que controla un par de semáforos en un cruce estandar
  se ampliará para controlar el cruce de peatones mediante un sensor
  capacitivo para su activación.
  */
 
void setup() {
  // Inicializamos como salida los pines de 3 al 8
  for (int pin = 3; pin <= 8; pin++) {
    pinMode(pin, OUTPUT);
  }
}
 
///////////////////////////////////////
// Función que controla el semáforo 1
//////////////////////////////////////
void semaforoUno() {
  digitalWrite(3, HIGH);// Luz verde
  int count = 0;
  delay(3000); // Luz verde encendida durante 3 segundos
  //El led verde parpadea
  digitalWrite(3, LOW);
  delay(500);
  digitalWrite(3, HIGH);
  delay(500);
  digitalWrite(3, LOW);
  delay(500);
  digitalWrite(3, HIGH);
  delay(500);
  digitalWrite(3, LOW);
  delay(500);
  digitalWrite(3, HIGH);
  delay(500);
  digitalWrite(3, LOW);
  delay(500);
  digitalWrite(3, HIGH);
  delay(500);
  digitalWrite(3, LOW);// Led verde se apaga
  digitalWrite(4, HIGH);// Led ambar se enciende
  delay(2500);
  digitalWrite(4, LOW);// Led ambar se apaga
  digitalWrite(5, HIGH);// Led rojo se enciende
  digitalWrite(8, LOW);// Se apaga el led rojo del semaforo 2
  //Llamamos a la función del semáforo 2.
  semaforoDos();
}

//////////////////////////////////////////////////////
//Función que controla el semáforo 2
///////////////////////////////////////////////////////
void semaforoDos() {
  digitalWrite(6, HIGH); // Luz verde semáforo 2
  delay(3000); // Tiempo de encendido del semáfor 2
  //El led verde parpadea
  digitalWrite(6, LOW);
  delay(500);
  digitalWrite(6, HIGH);
  delay(500);
  digitalWrite(6, LOW);
  delay(500);
  digitalWrite(6, HIGH);
  delay(500);
  digitalWrite(6, LOW);
  delay(500);
  digitalWrite(6, HIGH);
  delay(500);
  digitalWrite(6, LOW);
  delay(500);
  digitalWrite(6, HIGH);
  delay(500);
  digitalWrite(6, LOW);// El led verde se apaga
  // Se enciende el led ambar
  digitalWrite(7, HIGH);
  delay(2500);
  digitalWrite(7, LOW);// Se apaga el led ambar
  digitalWrite(8, HIGH);// Se enciende el led robo del semáforo 2
  digitalWrite(5, LOW);// Se apaga el led verde del semáforo 1
  //Llamamos a la función del semáforo 1
  semaforoUno();
}
 
void loop() {
  //Utilizamos un bucle para apagar todos los led de los dos semáforos
  for (int pin = 3; pin <= 8; pin++) {
    digitalWrite(pin, LOW);
  }
  digitalWrite(3, HIGH);// Encendemos el led verde del primer semáforo
  digitalWrite(8, HIGH);// Encendemos el led rojo del segundo semáforo
  // Llamamos a la función del semáforo uno
  // que iniciara una llamada recursiva a funciones.
  semaforoUno();
}
