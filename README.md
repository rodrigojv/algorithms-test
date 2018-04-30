# Ejercicios de algoritmia para evaluación de candidatos para Developers

## Requisitos

* Conocimientos básicos programación o algoritmia 🤓
* Cuenta en Github 😎
* Muchas ganas y curiosidad 💪

# Descripción de la Evaluación

Se proveen unos ejercicios de distinta dificultad. Leer antentamente lo que se pide en cada ejercicio y empezar por el que sea más sencillo.

Se pueden resolver los ejercicios en cualquier lenguaje o pseudo-código que se conozca.

## 1. Listas

* **1.1 Dado una lista de números, escribir un algoritmo que encuentre el producto más grande arrojado por tres de los números**

```
num = [-10, 7, 29, 30, 5, -10, -70];

int m1,m2,m3,p1,p2,r;
m1=num[0];
m2=num[0];
m3=num[0];
for(int i=1;i<7;i++){
  if(m1<num[i]){
    m1=num[i];
    p1=i;
  }
}  
for(i=1;i<7;i++){
  if(m2<num[i] && p1!=i){
    m2=num[i];
    p2=i;
  }
}  
for(int i=1;i<7;i++){
  if(m3<num[i] && p1!=i && p2!=i){
    m3=num[i];
  }
}  
r=m1*m2*m3;
print("el producto mas grande es "+r);

//computarProducto(listaDeNumeros);

// Salida: 21000


```

**Evaluación:** 

No se consideraron correctamente los números negativos, la multiplicación entre dos negativos y un positivo podía haber arrojado un número más grande que la múltiplicación de los 3 positivos más grandes.

3/5 puntos

## 2. Cadena de caractéres

* **2.1 Dado dos palabras o cadenas, escribir un algoritmo que retorne VERDADERO si la segunda palabra es un anagrama de la primera**

> > Un anagrama es una palabra o frase que resulta de la transposición de letras de otra palabra o frase.
> >
> > Dicho de otra forma, una palabra es anagrama de otra si las dos tienen las mismas letras, con el mismo número de apariciones, pero en un orden diferente.

Ejemplo de anagrama: "Mary" es un anagrama de "Army"


***********

```javascript

String c1="roma";
String c2="amor";
int cant1,cant2;
cant1=length(c1);
cant2=length(c2);
String L1,L2;
if(cant1==cant2){
  int b=0;
  for(int i=0;i<cant1;i++){
    b=0;
    L1=c1[i];
    for(int i2=0;i2<cant2;i2++){
      if(L1==extraer(1,i2,c2)){
        b=1;
      }
    }
    if(b==0)break;
  }
else
  print("falso");
}
if(b==1)print("true");


/*cadena1 = "Mary";
cadena2 = "Army";

esAnagrama(cadena1, cadena2);
*/
// Salida: VERDADERO
```
**Evaluación:**

Se buscan las letras de la primera palabra en la segunda, el proceso debería ser inverso también, ya que puede darse el caso
de que una letra aparezca en la segunda palabra pero no en la primera.

Ejemplo: "fueeral" y "realfun"

2/3 puntos

## 3. Números

* **3.1 Dado un número entero, escriba un algoritmo que determine si el número es potencia de dos**

```javascript
int n=55;
int c=0;int m=1;
if(n==1){
  print("es potencia de 2");
}else{
  while{
    m=m*2;
    if(m==n)print("es potencia de 2");
  }(m>n);
}
/*
esPotenciaDeDos(4); // VERDADERO
esPotenciaDeDos(64); // VERDADERO
esPotenciaDeDos(1); // VERDADERO
esPotenciaDeDos(0); // FALSO
esPotenciaDeDos(-1); // FALSO
*/
```

**Evaluación:**

Faltó ajustar un poco la estructura de control while con la expresión para continuar el while, tenía que ser `do{...}while(m < n)`

1/2 puntos

# Forma de entrega

Se debe hacer un fork de este repositorio, solucionar en ese fork los ejercicios y luego hacer un push a dicho repositorio.

Se puede crear un archivo `.txt` o `.md` por cada ejercicio. Ejemplo: `ejercicio_01.md`.

Finalmente, enviar un email con la URL del repositorio forkeado a la persona que te envió este test.

Muchas gracias y buena suerte! ❤️️
