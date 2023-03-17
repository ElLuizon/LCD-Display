# LCD Display 📟

![image](https://electronicavaltierra.com.mx/wp-content/uploads/2018/01/D-C1602L.jpg)

# ¿Qué es una LCD?
Las siglas LCD significan “Liquid Cristal Display” ó pantalla de cristal líquido. Es una pantalla plana basada en el uso de una sustancia liquida atrapada entre dos placas de vidrio, haciendo pasar por este una corriente eléctrica a una zona especifica, para que así esta se vuelva opaca, y además cuenta (generalmente) con iluminación trasera.
Las pantallas LCD de color, cada pixel individual se divide en tres cédulas o sub pixeles con los colores RGB (Rojo, Verde y Azul) respectivamente. Y así cada pixel puede controlarse para  producir una gran variedad de colores distintos..

# Características de las LCD
Existen una gran variedad de proyectos en los que se incluye una LCD para interfaz con el usuario, lo que modifica las necesidades, las cuales es importante atender más que nada por los precios. Y la importancia de esta en el proyecto.
Algunos factores básicos a considerar en una LCD son:

Tamaño:
El tamaño de un panel LCD generalmente se mide a lo lardo de su diagonal, expresado generalmente en pulgadas. Sin embargo existen más características que pueden describir las dimensiones aproximadas, como por ejemplo la LCD 16×2 (negro sobre fondo azul) se refiere a que tiene la capacidad de tener al mismo tiempo 16 caracteres de manera horizontal en dos renglones (cada uno).

Resolución:
Esta se expresa con las dimensiones horizontal y vertical. las pantallas HD tienen una resolución de 1920×1080 por ejemplo. Y esta puede alcanzar con esta resolución una gran variedad de tamaño, pero si no se ocupa gran a gran detalle esta, estarías desperdiciando calidad (por no utilizar algo que tienes disponible). En 5hz se maneja, por ejemplo la LCD gráfica 128×64 (negro sobre fondo verde). Que a pesar de su tamaño la consideramos suficiente para las aplicaciones estudiantiles, y algunas industriales donde se requiera tener algo claro y legible en un tamaño práctico.

Brillo:
La luminosidad de la pantalla también es importante analizarla, ya que según la aplicación en la que se encuentre esta, requerirá más luz para poder apreciarse, o viceversa. Por lo que la mayoría cuentan con una luz trasera y la posibilidad de poder controlar su luminosidad.

Iluminación CCFL Esta iluminación básicamente consta poner detrás de la pantalla una matriz de CCFL, o bien en las orillas o bordes de la pantalla. Sin embargo es más consumo que el led y tiene un menor tiempo de vida, por lo que poco a poco se ah ido poniendo en segundo plano.

Iluminación LED Esta iluminación puede presentarse en dos maneras, en un solo color, (generalmente blanco) o bien en RGB, los blanco suelen ser los más utilizados. Estos al igual que la iluminación CCFL, pueden estar formando una matriz en la parte de atrás, o bien pueden colocarse a los extremos del display.

Contraste:
Es la relación entre la intensidad más brillante y la más oscura.

{
  "version": 1,
  "author": "Uri Shaked",
  "editor": "wokwi",
  "parts": [
    {
      "type": "wokwi-pi-pico",
      "id": "pico",
      "top": 123.67,
      "left": 135.97,
      "rotate": 90,
      "hide": false,
      "attrs": { "env": "arduino-community" }
    },
    {
      "type": "wokwi-lcd1602",
      "id": "lcd",
      "top": -17.85,
      "left": 22.03,
      "rotate": 0,
      "hide": false,
      "attrs": {}
    },
    {
      "type": "wokwi-resistor",
      "id": "r1",
      "top": 114.8,
      "left": 226.31,
      "rotate": 0,
      "hide": false,
      "attrs": { "value": "220" }
    }
  ],
  "connections": [
    [ "pico:GND.1", "lcd:VSS", "black", [ "v-51", "*", "h0", "v18" ] ],
    [ "pico:GND.1", "lcd:K", "black", [ "v-51", "*", "h0", "v18" ] ],
    [ "pico:GND.1", "lcd:RW", "black", [ "v-51", "*", "h0", "v18" ] ],
    [ "pico:VSYS", "lcd:VDD", "red", [ "v16", "h-16" ] ],
    [ "pico:VSYS", "r1:2", "red", [ "v16", "h0" ] ],
    [ "r1:1", "lcd:A", "pink", [] ],
    [ "pico:GP12", "lcd:RS", "blue", [ "v-16", "*", "h0", "v20" ] ],
    [ "pico:GP11", "lcd:E", "purple", [ "v-20", "*", "h0", "v20" ] ],
    [ "pico:GP10", "lcd:D4", "green", [ "v-24", "*", "h0", "v20" ] ],
    [ "pico:GP9", "lcd:D5", "brown", [ "v-28", "*", "h0", "v20" ] ],
    [ "pico:GP8", "lcd:D6", "gold", [ "v-32", "*", "h0", "v20" ] ],
    [ "pico:GP7", "lcd:D7", "gray", [ "v-36", "*", "h0", "v20" ] ]
  ]
}
