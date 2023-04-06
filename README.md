
<!--- [![PÁGINA WEB](https://img.shields.io/badge/P%C3%81GINA%20WEB-21759B?style=for-the-badge&logo=WordPress&logoColor=white)](http://mecatrogrupo.com) --->
[![INSTAGRAM](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](http://instagram.com/mecatrogrupo)
[![CONTACTO](https://img.shields.io/badge/Contacto-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contacto@mecatrogrupo.com)
[![TIENDA](https://img.shields.io/badge/Tienda-53B755?style=for-the-badge&logo=&logoColor=white)](http://mecatrogrupo.com)

<img src="https://raw.githubusercontent.com/Mecatrogrupo/custom-nfc-tags/main/Fotos/render1Cuadrado.png" alt="Foto explotada llavero" width="350"/>

## Objetivo
Lograr convertir diferentes tarjetas NFC dispositivos más pequeños que cumplan las mismas funciónes, como llaveros o pulseras. Esto incluye: extraer los chips y armarles otra carcasa, clonar tarjetas a otros formatos, combinar diferentes tecnologías en una, diseñar métodos para hacerlo en masa, y documentar los hallazgos en general.

## Hallazgos sobre diferentes sistemas
### Transporte argentino
Las tarjetas que usa son del tipo Mifare 1k. Guardan su saldo adentro y, al estar encriptadas, no pueden ser clonadas (o al menos no fácilmente). Su comunicación se define en [ISO 14443](https://www.iso.org/obp/ui/#iso:std:iso-iec:14443:-4:ed-4:v1:en) y trabaja a 13.56MHz. Sin embargo, en la práctica los lectores de transporte oscilan entre 14 y 15 MHz, y hay diferencias pronunciadas entre los diferentes métodos de transporte [[1]](#1).

Las tarjetas pueden ser leídas por teléfonos, pero testear antenas armadas con los mismos no es una buena indicación de la distancia en que las leerá un lector de transporte (por la diferencia de frecuencias y de diámetros del bobinado).

Los chips internos hasta el 2022 venían en dos tamaños: 7,5mm x 5mm y 6mm x 3mm. En 2023 se agregaron unos un poco más grandes.

#### Referencias

<a id="1">[1]</a> 
[ST AN2866 Application note](https://www.st.com/content/ccc/resource/technical/document/application_note/d9/29/ad/cc/04/7c/4c/1e/CD00221490.pdf/files/CD00221490.pdf/jcr:content/translations/en.CD00221490.pdf)


## Diseño circular de llavero
Este diseño de llavero se basa en un cuerpo con un disco interno con el chip de la tarjeta, una bobina de cobre esmaltado, y un capacitor. Este último es necesario para lograr que la antena resuene bien a la frecuencia de los lectores, ya que seleccionar el alambre justo con la cantidad de vueltas justa es mucho más difícil y resulta en una distancia de lectura menor. \
Probamos hacer variantes *print in place* (se imprime el cuerpo hasta la mitad y después se coloca el llavero) y no *print in place* (se imprimen por separado y conectan a presión). Encontramos que la segunda es mucho más fácil de armar y no presenta desventajas considerables (solo queda un poquito más grande). \
Hay instrucciones de armado usando el ejemplo de transporte Argentino en [/Manuales/Instrucciones-maker.pdf](/Manuales/Instrucciones-maker.pdf).

### Medias testeadas que funcionan
*foto con las diferentes medidas*

n: cantidad de vueltas \
l: largo del alambre \
d: diámetro del alambre \
D: diámetro de la bobina \
H: altura espacio para bobinado \
h1: grosor de la tapa inferior \
h2: grosor de la tapa superior \
L: distancia de lectura relativa a la original \
F: medida del capacitor

#### Transporte argentino
| n | l      | d       | D    | H     | h1    | h2     | L     | F    |
|---|--------|---------|------|-------|-------|--------|-------|------|
| 7 | ~ 69cm | 0,25 mm | 25mm | ~35mm | 0.6mm | 1.15mm | buena | 39pF |


<hr />
<table border="0px">
<th align="left">
Mecatrogrupo 2022.
</th>
<tr>
<td>
Esta fuente describe Hardware Libre y está licenciada bajo la licencia 
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






