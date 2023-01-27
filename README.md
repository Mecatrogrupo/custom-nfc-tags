<!--- [![PÁGINA WEB](https://img.shields.io/badge/P%C3%81GINA%20WEB-21759B?style=for-the-badge&logo=WordPress&logoColor=white)](http://mecatrogrupo.com) --->
[![INSTAGRAM](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](http://instagram.com/mecatrogrupo)
[![CONTACTO](https://img.shields.io/badge/Contacto-D14836?style=for-the-badge&logo=gmail&logoColor=white)](http://mecatrogrupo.com)
[![TIENDA](https://img.shields.io/badge/Tienda-53B755?style=for-the-badge&logo=&logoColor=white)](http://mecatrogrupo.com)
  
## Objetivo
Lograr convertir diferentes tarjetas NFC dispositivos más pequeños que cumplan las mismas funciónes, como llaveros o pulseras. Esto incluye: extraer los chips y armarles otra carcasa, clonar tarjetas a otros formatos, combinar diferentes tecnologías en una, diseñar métodos para hacerlo en masa, y documentar los hallazgos en general.

## Hallazgos sobre diferentes sistemas
### Transporte argentino
Las tarjetas que usa son del tipo Mifare 1k. Guardan su saldo adentro y, al estar encriptadas, no pueden ser clonadas (o al menos no fácilmente). Su comunicación se define por el protocolo sadfopiasdfp, que trabaja a 13.56MHz. Sin embargo, en la práctica los lectores se acercan más a 12341234MHz, y hay diferencias entre los diferentes métodos de transporte. 

Las tarjetas pueden ser leídas por teléfonos, pero testear antenas armadas con los mismos no es una buena indicación de la distancia en que las leerá un lector de transporte (por la diferencia de frecuencias y de diámetros del bobinado).

Los chips internos vienen en dos tamaños: 7,5mm x 5mm y 6mm x 3mm.

## Diseño circular de llavero
Este diseño de llavero se basa en un cuerpo con un disco interno con el chip de la tarjeta, una bobina de cobre esmaltado, y un capacitor. Este último es necesario para lograr que la antena resuene bien a la frecuencia de los lectores, ya que seleccionar el alambre justo con la cantidad de vueltas justa es mucho más difícil y resulta en una distancia de lectura menor. \
Probamos hacer variantes *print in place* (se imprime el cuerpo hasta la mitad y después se coloca el llavero) y no *print in place* (se imprimen por separado y conectan a presión), y encontramos que la segunda es mucho más fácil de armar y no presenta desventajas considerables (solo queda un poquito más grande). \
Hay instrucciones de armado usando el ejemplo de transporte Argentino en /Manuales/Armado.md.

### Medias testeadas que funcionan
*foto con las diferentes medidas*

n: cantidad de vueltas \
l: largo del alambre \
d: diámetro del alambre \
D: diámetro de la bobina \
H: altura espacio para bobinado \
h1: grosor de la tapa \
L: distancia de lectura relativa a la original \
F: medida del capacitor

| n | l       | d       | D  | H  | h  | L     | F    |
|---|---------|---------|----|----|----|-------|------|
| 7 | ~ 69 cm | 0,25 mm | ?? | ?? | ?? | buena | 39pF |


<hr />
<table border="0px">
<th align="left">
Mecatrogrupo 2022.
</th>
<tr>
<td>
Esta fuente describe Hardware Abierto y está licenciada bajo la licencia 
CERN-OHL-W v2
</td>
</tr>
<tr>
<td>
Puede redistribuir y modificar esta documentación y crear productos
que la utilicen bajo los términos del CERN-OHL-W v2 (https:/cern.ch/cern-ohl).
Esta documentación se distribuye SIN NINGUNA GARANTÍA EXPRESA O IMPLÍCITA
GARANTÍA, INCLUIDA LA DE COMERCIABILIDAD, CALIDAD SATISFACTORIA
E IDONEIDAD PARA UN FIN DETERMINADO. Por favor refiérase a la CERN-OHL-W v2
para condiciones aplicables.<br/>
Ubicación de la fuente: https://github.com/Mecatrogrupo/custom-nfc-tags/
</td>
</tr>
</table>






