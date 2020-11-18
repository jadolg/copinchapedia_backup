---
title: Plástico Leal - La Maquinaria
description: Para aprender a construir colaborativamente herramientas y máquinas de código abierto para reciclar plástico, usando preferiblemente recursos localmente accesibles.
published: true
date: 2020-11-01T22:19:05.140Z
tags: 
editor: undefined
dateCreated: 2020-09-22T23:48:17.672Z
---

En este taller aprendemos a construir colaborativamente herramientas y máquinas de código abierto para reciclar plástico, usando preferiblemente recursos localmente accesibles.

*Por favor entienda este espacio como un laboratorio vivo donde vamos actualizando el contenido para reflejar las iniciativas e interacciones que participan.*

<br>

# Objetivos: 

- Aprender sobre los procesos técnicos y usos prácticos más comunes para reciclar de plásticos. 

- Construir colaborativamente máquinas de código abierto para reciclar de plástico usando la mayor cantidad reursos accesibles en Cuba. 

	- Construir una trituradora de plástico.

	- Construir una extrusora. Para hacer filamentos de impresión 3D con el plástico triturado.

	- Construir una hangprinter. Para fabricar por impresión 3D objetos de grandes dimensiones con los filamentos plásticos.
  
	- Documentar las experiencias de construcción de máquinas en el repositorio público.

- Exponer Mapear y documentar otras experiencias ya existentes de construcción de máquinas de código abierto para reciclar plástico.

<br> 

# Máquinas en construcción

<br> 

## Trituradora de plástico

![trituradora.jpeg](/8c2e157f298e40ca9e1de6639ed86665.jpeg)

### Tab {.tabset}

#### Descrpción

Corta artículos de plástico en pequeñas partículas listas para ser convertidas en cosas nuevas por otras máquinas. El plástico triturado puede ser de múltiples tamaños y colores para aumentar su valor.

#### Listado de materiales

Los detalles del costo de una trituradora según lo que el proyecto ya ha conseguido están [aquí](https://docs.google.com/spreadsheets/d/1ArtWWj6Qs_AYpu6C6BTy-PNZvMUTdnTiIenrF_23XxQ/). 
<br> 

| Partes					 								 | Cantidad  | Detalles | Conseguido |
|------------------------------------|-----------|----------------------------------|-|
| Cuerpo de Cuchillas				 								 | 1  |  | ✓ |
| Barra hexagonal				 			    					 | 1  |  | ✓ |
| Soporte 								 | 4  | Perfil L 30x30x3 |  |
| Malla             				 								 | 1  |  |  |
| Rodamientos			 								 | 2  | | ✓ |
| Tolva				 								 | 1  | | ✓ |
| Base			 								 | 1  | Perfil cuadrado x30 |  |
| Motor | 1 | Motor monofásico 2Hp, 1600 -1700 RPM | ✓ |
| Reductor			 								 | 1  | entre 1->80 y 1->130 | ✓ |
| Encendedor de alimentación			 								 | 1 |  | ✓|
| Indicador LED			 								 | 1 |  | ✓ |
| Cable de alimentación				 								 | 5m | | ✓ |

<br> 

#### Enlaces

uu

{.is-info}

<br>

## Extrusor de Filamentos RepRapable Recyclebot

![extrusor de filamentos.jpg](/9449d00fd1ea4ee4b9a050adfea7efec.jpg)

### Tab {.tabset}

#### Descrpción
La extrusión es un proceso continuo donde las partículas de plástico se insertan en la tolva y se extruyen en una hilo de plástico. Estas hilos se pueden usar para hacer nueva materia prima, plástico granulado, girar alrededor de un molde o usarse de manera creativa.

#### Listado de materiales
Pueden encontrar un listado materiales [aquí](https://www.sciencedirect.com/science/article/pii/S2468067218300208?via%3Dihub#s0020). 

#### Enlaces

hhhh

{.is-info}

<br>

## Hangprinter

![impresoras 3D Hangprinter.jpg](/79b326f19c634a51ae9a5cc151afe305.jpg)
  
### Tab {.tabset}

#### Descrpción
**[Hangprinter](https://www.hangprinter.org/)** es un modelo de impresora 3D delta por deposición fundida de código abierto que se destaca por su diseño único sin marco y su bajo costo. Fue creado por Torbjørn Ludvigsen. Muchas de las partes de esta impresora 3D se pueden producir en una impresora 3D (parcialmente autorreplicable), formando parte del proyecto RepRap.  

Se instala en un espacio determinado utilizando la propia habitación como marco. El diseño también se puede adaptar para utilizar una mesa en lugar de una habitación completa. La impresora tiene un Efector que se suspende del techo y se mueve mediante motores paso a paso estacionarios con poleas e hilos de sedal.

Uno de los beneficios de perder el marco es, por supuesto, un volumen de construcción mucho mayor, ya que no está restringido a "la caja". Con tres puntos de anclaje que mantienen la máquina en su lugar, la Hangprinter puede colgarse de cables conectados al techo. A continuación, el sistema puede determinar qué movimientos realizar a partir de las ubicaciones configuradas del firmware.

#### Listado de materiales
**[Listado de materiales original ](https://docs.google.com/spreadsheets/d/1lOPZoF1P2OSdJcijZRVrwAEVFh3LLAnf6-s6k-hlbZU).**

<br>

| Partes impresas 					 | Cantidad | Detalles                  | Conseguido |
|----------------------------|----------|-----------------------------------|----|
| Beam Slider ABC 					 | 3  		  |				                            |  ✓ |
| Beam Slider D   					 | 3        | 					  						      		|  ✓ |
| Corner Clamp    					 | 3 			  |  												 	        |  ✓ |
| Extruder Holder  					 | 1      	| Usar plástico resistente al calor |  ✓ |
| Lineroller ABC	Winch			 | 3			  |  								      				 	  |  ✓ |
| Lineroller D 							 | 3 			  |  		 		  		      						  |  ✓ |
| Lineroller Anchor Template | 2 			  | 					      									|  ✓ |
| Lineroller Anchor 				 | 6 			  | 					      								 	|  ✓ |
| Motor Braket 							 | 4 	      | Usar plástico resistente al calor |  ✓ |
| Motor Gear	             	 | 4        |  												      	  |  ✓ |
| Spool  										 | 4 			  |  											      		  |  ✓ |
| Spool Gear								 | 4 			  |  											      		  |  ✓ |
| Spacer 										 | 4				|												      	    |  ✓ |
| Spool Core								 | 4				|												      	    |  ✓ |
| Cable Clamp 							 | 12 			|  										      			  |  ✓ |
| Layout										 | 1        | 									              	|  ✓ |
| Mechaduino standoff		     | 32	      | Usar plástico resistente al calor |  ✓ |

<br>

| Vitaminas					 								 | Cantidad  | Detalles | Conseguido |
|------------------------------------|-----------|----------------------------------|-|
| Motor Nema 17		  				 |  5	 	 	   | > 40 N/cm holding torque, flat shaft. Se reduce a 4 por impresora si otro motor es usado para el extrusor. |  |
| FireLine 0.5 mm 				  				 |  60 m  	 | 0.39 mm también sirve. Es significante cuán largo cortes los hilos. | |
| Hoja de MDF o Plywood						 |  50x50 cm | Grosor 10-14 mm						 | |
| Arduino Mega 				  						 |  1	   	   |					  									 |  ✓ |
| RAMPS 				  									 |  1	     	 |					  											 |  ✓ |
| Controladores de motor paso a paso (pololu)			  				 |  1	   	   | 			  	     |  ✓ |
| Cable USB  (tipo B) 				  	 |  1	 |			 |  ✓ |
| Listón de 40 cm de largo   | 3 | Perfil cuadrado de 15 mm de grosor |   |
| Listón de 27.5 cm de largo | 1 |				^^	  											|   |
| Fuente		  						   | 1 | 12 V, 12.5 A o mayor 							| ✓ |
| Brida plástica				 										 |  18	     | ancho entre 4 y 5 mm | ✓ |
| Tornillo M3, largo 5 mm		 | 16 |					  											 | ✓ |
| Tornillo M3, largo 12 mm			 			 |  12	     |					  											 | ✓ |
| Tornillo M3 largo, 45 mm			 		 |  16	     | Ca 1 cm longer than your motor body height. For mounting Mechaduino PCB on motor rear. | |
| Tornillo M3/M4, largo 14 - 20 mm		 |  4	   	   | For attaching PSU to sheet				 | ✓ |
| Rodamiento 608		 								 |  8	   	   |  																 | ✓ |
| Rodamiento 623 con ranura V			 				 |  12	     | 			                             | |
| Tubo de PTFE 		  										 |  10 cm	   | Standard bowden, 4 mm outer dia, any inner dia	| ✓ |
| Tornillo de madera autorroscante ca M3x10	 |  ca 90    | M[2.5-4.5]x10, head diámetro 8-14 mm, non-countersunk. For fastening to ceiling plate | |
| Tornillo de madera autorroscante M4x45		 |  4	   	 	 | For fastening spool core	| |
| Tornillo de madera autorroscante M2x[6-14] |  4	   	   | Head diameter ca 4 mm. For mounting Mega onto sheet material. | |
| Tornillo de madera autorroscante M3x10		 |  18	     | Head diameter 7 mm, length 10 mm Countersunk head. For attaching linerollers on ABC anchors| |
| Arandela M6 o M8 									 | 	4		     | For capping 608 bearings in place on top of spool core | ✓ |
| Cinta de 15 hilos de cable			  				 |  5	m      | O cinta de 30 hilos de cable 28AWF with quadrupled wires to/from the heater element ||
| Tuerca M3 Nuts			  										 | 12 | 					 		| ✓ |
| Extrusor + hot end				  			 |  1	   	 	 | Cualquier configuración que se ajuste a Nema17 debe funcionar | |
| Cables de alimentación Rojo y Negro   		 |  ca 2.5	 | Para conectar 12 V a la RAMPS y los Mechaduinos | ✓ |
| Smart Stepper PCB				  				 |  4	     	 | Sirve tanto la versión de Mechaduino 0.2 como la 0.1 | |
| Cable Jumper 		  							 |  ca 50	 	 | Para codificar el sistema con 7 colores | ✓ |
| Regulator 5V 			  							 |  1      	 | Para energizar Mechaduino directamente desde el PSU. Recommended for reliable long term operation | |
| 5V -> 3V3 level converter				  	 |  1	     	 | para RAMPS i2c <-> Mechaduino. Small breadboard handy for connecting this | |

#### Manual

##### Montaje de hardware

![small_000.jpg](/small_000.jpg)

Bienvenido al ensamblaje de hardware Hangprinter versión 3. Haga clic en las imágenes para ver versiones más grandes. Las siguientes instrucciones asumen que ha completado el paso de abastecimiento.

![small_001.jpg](/small_001.jpg)

Hardware para una construcción que no sea SmartStepper, excluyendo el cable USB y los tornillos. Tenga en cuenta que el material de la hoja rectangular es para construir anclajes ABC. Deben ser una pila de tres. Las partes impresas en blanco estarán en contacto con los motores. Imprímalos en un plástico resistente al calor en caso de que sus motores se calienten alguna vez.

![small_002.jpg](/small_002.jpg)

Empuje los carretes y los engranajes del carrete sobre los cojinetes 608.

![small_003.jpg](/small_003.jpg)

Repita para todos los carretes y engranajes de carretes.

![small_004.jpg](/small_004.jpg)

Empuje los carretes con rodamientos 608 en los núcleos de los carretes.

![small_005.jpg](/small_005.jpg)

Ahora coge tus espaciadores.

![small_006.jpg](/small_006.jpg)

... y compruebe que encajan perfectamente en los núcleos de los carretes.

<br>

Ahora podría ser un buen momento para medir los radios de sus carretes con un par de calibradores. Tenga en cuenta los radios en los propios carretes. Esto será necesario para la calibración del firmware más adelante.

También podría ser un buen momento para colocar líneas en sus carretes. Se requieren nueve líneas para impulsar la impresora. Por defecto, tres de ellos tienen 4 m de largo, los seis restantes tienen 7,5 m de largo. Coloque los de 4 m en un carrete. Coloque pares de 7.5 m en los tres carretes restantes.

[Aquí](http://forums.reprap.org/read.php?1,792937,809736#msg-809736) encontrará una guía más detallada sobre cómo elegir la longitud de las líneas . Si usa longitudes de línea personalizadas o grosor de línea, debe especificar esto en la configuración del firmware más adelante.

Así es como atas tu línea a tu carrete:

![small_hangprinter_hitch_0.jpg](/small_hangprinter_hitch_0.jpg)

Pase un bucle a través del orificio de la pared del carrete derecho y sáquelo del orificio izquierdo.

![small_hangprinter_hitch_1.jpg](/small_hangprinter_hitch_1.jpg)

Pase su línea a través del agujero derecho nuevamente.

![small_hangprinter_hitch_2.jpg](/small_hangprinter_hitch_2.jpg)

Apriete desde el interior. Deja mucho hilo suelto por dentro.

![small_hangprinter_hitch_3.jpg](/small_hangprinter_hitch_3.jpg)

Haz un simple tirón alrededor de la pierna izquierda de tu lazo.

![small_hangprinter_hitch_4.jpg](/small_hangprinter_hitch_4.jpg)

Primer plano del mismo enganche.

![small_hangprinter_hitch_5.jpg](/small_hangprinter_hitch_5.jpg)

Haz otro tirón por encima del anterior. Haz tres tirones en total, así que uno más después de este.

![small_hangprinter_hitch_6.jpg](/small_hangprinter_hitch_6.jpg)

Apriete sus enganches tirando de la pierna izquierda del lazo y del extremo suelto de la línea. Luego, tire de los carretes hacia afuera para ver si el nudo se sostiene.

![small_hangprinter_hitch_7.jpg](/small_hangprinter_hitch_7.jpg)

El exterior de su carrete ahora debería verse así.

![small_008.jpg](/small_008.jpg)

Compruebe que los engranajes de los carretes encajen bien en los carretes. Tenga en cuenta que los dos engranajes de carrete + carrete están montados al revés en esta imagen. Las escotillas en los radios del engranaje de carrete están ahí para dejar espacio para las cuatro cabezas de los tornillos más adelante.

![small_010.jpg](/small_010.jpg)

Inserte el tubo de PTFE en los rodillos de revestimiento de anclaje y corte al ras con el frente.

![small_011.jpg](/small_011.jpg)

Haga lo mismo con los D-linerollers.

![small_012.jpg](/small_012.jpg)

Los tubos de PTFE deben encajar bien en los rodillos de revestimiento en D. Empújelos así.

![small_013.jpg](/small_013.jpg)	

Tubos de PTFE insertados.

![small_014.jpg](/small_014.jpg)	

Monte los rodamientos 623 con ranura en V en todos los rodillos de revestimiento.

![small_015.jpg](/small_015.jpg)	

Ahora agarre sus motores y engranajes del motor.

![small_016.jpg](/small_016.jpg)

Los engranajes del motor tienen orificios en forma de D y una muesca para ayudarlo a alinearlos con los ejes del motor.

![small_017.jpg](/small_017.jpg)

Golpee suavemente el engranaje del motor en su lugar con muchos golpes pequeños de un objeto ligero, suave y redondeado. No golpees fuerte. Si los orificios del engranaje del motor están demasiado apretados, taladre / lime más ancho o simplemente imprima otros nuevos. Si los orificios del engranaje del motor son demasiado anchos, inserte las tuercas desde abajo y apriételas con tornillos de fijación.

![small_018.jpg](/small_018.jpg)

El espacio entre el engranaje del motor y el motor debe ser de aproximadamente 1 mm.

![small_019.jpg](/small_019.jpg)

Ahora agarra los soportes del motor.

![small_020.jpg](/small_020.jpg)

Primero inserte los tres tornillos en sus agujeros. Será más complicado hacerlo más tarde.

![small_021.jpg](/small_021.jpg)

Monte los soportes del motor en los motores.

![small_022.jpg](/small_022.jpg)

Ahora junta tus aparatos electrónicos. Se recomienda utilizar SmartSteppers en los motores A, B, C y D, aunque en la imagen se muestran los stepsticks. Consulte las <a href="#SmartStepper">instrucciones de montaje de SmartStepper</a>

![small_023.jpg](/small_023.jpg)

Inserte el paso / directorio de sus controladores en las salidas paso / directorio de la placa RAMPS.

![small_024.jpg](/small_024.jpg)

Monte su escudo RAMPS firmemente en su Arduino Mega.

![small_025.jpg](/small_025.jpg)

Coge las piezas de tu mudanza.

![small_026.jpg](/small_026.jpg)

Su viga de 40 cm debe empujarse hasta la raíz de la pared separadora. Esto es importante para obtener el ancho correcto de su triángulo de movimiento.

![small_027.jpg](/small_027.jpg)

Adjuntar con cremalleras sin apretar.

![small_028.jpg](/small_028.jpg)

Asegúrese de que las vigas estén alineadas con la raíz de la pared del separador. Luego apriete lo más fuerte que pueda sin romper las cremalleras.

![small_029.jpg](/small_029.jpg)

El triángulo terminado debe sentirse razonablemente rígido. No experimentará grandes fuerzas durante la impresión, pero no debería cambiar las dimensiones fácilmente.

![small_030.jpg](/small_030.jpg)

Deje unos mm de brida, para que pueda ajustarlos más tarde si es necesario.

![small_031.jpg](/small_031.jpg)

Si usa vigas de madera, puede perforar un orificio de montaje a través del lado del triángulo y la viga transversal. Si usa vigas de fibra de carbono, coloque la viga transversal con bridas en su lugar, como se muestra en esta [imagen vinculada.](https://copinchapedia.copincha.org/ziptied_crossbeam.jpg)

![small_032.jpg](/small_032.jpg)

Utilice arandelas en ambos lados del tornillo M3.

![small_033.jpg](/small_033.jpg)

Apriete bastante el tornillo. Si su madera es blanda, la lavadora debe hundirse ligeramente en la madera.

![small_034.jpg](/small_034.jpg)

Ahora agarra tus controles deslizantes de haz.

![small_035.jpg](/small_035.jpg)

Los controles deslizantes de la viga ABC deben estar bien sujetos.

![small_036.jpg](/small_036.jpg)

Los controles deslizantes de la viga D deben estar sueltos al principio.

![small_037.jpg](/small_037.jpg)

Apriete los controles deslizantes de la viga D colocándolos más adentro de la brida, apuntando hacia la esquina más cercana.

![small_038.jpg](/small_038.jpg)

Coloque los controles deslizantes ABC y D en los extremos opuestos de cada lado del triángulo.

![small_039.jpg](/small_039.jpg)

Pase una brida sobre la viga transversal y a través del soporte de la extrusora como se muestra.
![small_040.jpg](/small_040.jpg)

Use dos zipties como se muestra en la imagen, o use un ziptie más largo. Apriete lo más fuerte que pueda.

![small_041.jpg](/small_041.jpg)

Agrega dos cremalleras más, en bucles rectos alrededor de la viga.

![small_042.jpg](/small_042.jpg)

Use la cuña impresa para apretar las correas largas. El soporte de la extrusora ahora debería estar muy ajustado a la viga transversal.

![small_043.jpg](/small_043.jpg)

El cable plano está sujeto con cremallera al soporte de la extrusora para aliviar la tensión.

![small_044.jpg](/small_044.jpg)

Monte su extrusora + extremo caliente de elección y guarde el motor terminado.

![small_045.jpg](/small_045.jpg)

Coge tu plantilla 2d-prints. Verifique que estén impresos al 100% de escala comparando los tamaños de los contornos impresos en 2d con las bases de las piezas impresas en 3D. [Imagen de una doble verificación exitosa.](https://copinchapedia.copincha.org/print_template_to_scale.jpg)


![small_046.jpg](/small_046.jpg)

Colóquelos de modo que las líneas brillen. Idealmente en una ventana o en una mesa de cristal.

![small_047.jpg](/small_047.jpg)

Alinee las superposiciones perfectamente una encima de la otra.

![small_048.jpg](/small_048.jpg)

Pegue juntos.

![small_049.jpg](/small_049.jpg)

Coloque su plantilla 2d terminada en su placa de techo.

![small_050.jpg](/small_050.jpg)

Atornille la plantilla plana sobre la placa de techo.

![small_051.jpg](/small_051.jpg)

Marque las marcas a través de los centros de todos los círculos pequeños.

![small_052.jpg](/small_052.jpg)

La plantilla con todas las marcas martilladas se ve así.

![small_053.jpg](/small_053.jpg)

La placa del techo debajo debe tener marcas visibles como esta.

![small_054.jpg](/small_054.jpg)

Ahora monte sus carretes y rodillos de revestimiento preparados. Tenga en cuenta la orientación de los linerollers para que la línea pueda entrar como se especifica en la plantilla. Es útil marcar los carretes con los nombres A, B, C y D, como se especifica en la plantilla. No olvide los tornillos largos que atraviesan el centro de los núcleos del carrete.

![small_055.jpg](/small_055.jpg)

Un poco de juego en los engranajes es inofensivo porque las líneas pretensarán los engranajes de todos modos. Los engranajes que engranan mal o ruedan de manera desigual debido a un ajuste demasiado apretado pueden causar problemas más adelante.

![small_056.jpg](/small_056.jpg)

Apuntar los cables del motor lejos del centro del carrete es bueno, pero no crítico.

![small_056.jpg](/small_057.jpg)

Sujete los cables del motor lo más cerca posible del soporte del motor.

[Video de montaje de piezas a placa de techo.](https://www.hangprinter.org/doc/v3/media/mounting_parts_onto_ceiling_plate.webm)

<br>

##### SmartStepper y cableado <a name="SmartStepper"></a>

Utilice el firmware que se encuentra en el [repositorio de Hangprinter](https://gitlab.com/tobben/hangprinter/tree/Openscad_version_3/firmware/SmartStepper_subtree) . Para saber cómo cargarlo, consulte la propia [documentación de Misfittech.](http://misfittech.net/nema-17-smart-stepper/)

No tenemos un diagrama de cableado completo con SmartSteppers, por lo tanto, consulte el siguiente diagrama de cableado, pero tenga en cuenta que no se necesita el cambiador de nivel externo de 12V -> 5V, ya que este componente está integrado en los SmartSteppers.

![small_hangprinter_electronics_diagram_mechaduino_ramps1.4_v2.3.jpg](/small_hangprinter_electronics_diagram_mechaduino_ramps1.4_v2.3.jpg)

... y conecte los SmartSteppers de esta manera:

![small_smartstepperwires.jpeg](/small_smartstepperwires.jpeg)

Cableado SmartStepper. 

<br>

##### Montaje

Las únicas fuentes de instrucciones de montaje son videos:

- [HP3 Build With tobben & Thomas Sanladerer (enlace directamente al montaje)](https://www.youtube.com/watch?v=iOwjbu2UMlQ&feature=youtu.be&t=3h54m43s)
- [Vínculos anotados en el video de compilación de HP3 de Tobben y Thomas Sanladerer](https://reprap.org/wiki/Links_Into_Hangprinter_v3_Build_Video#)
- [Compilación de HP3 con Chris Riley](https://www.youtube.com/watch?v=VBc7Zab64do&list=PLB_0YGFjbOnbQ_zPnpLAjwgnE2ryhKScB)

<br>

##### Calibración de anclajes y acumulación de carretes

Si lo está haciendo manualmente (sin SmartStepper), mire [esto](https://reprap.org/wiki/Links_Into_Hangprinter_v3_Build_Video#Now_going_into_an_hour_of_measuring_this). También mire las fuentes de video de [Chris Riley](https://www.youtube.com/watch?v=VBc7Zab64do&list=PLB_0YGFjbOnbQ_zPnpLAjwgnE2ryhKScB) y [Thomas Sanladerer](https://www.youtube.com/watch?v=Jk4fhQvNoaM&list=PLDJMid0lOOYmSWYimgOW-Q9OKyIp0OFyK).

Si está utilizando SmartStepper, entonces tobben ha preparado un script que, con suerte, le permitirá evitar tener que medir las posiciones de los anclajes manualmente: [aquí](https://gitlab.com/tobben/auto-calibration-simulation-for-hangprinter). Es un poco difícil de usar, asegúrese de leer el archivo README y de presentar un problema si encuentra un error o una mejora.

<br>

<br>

<br>

Construir, montar, calibrar y ejecutar una HP3 es difícil. No estas solo. Asegúrese de revisar los [recursos](https://www.hangprinter.org/resources) , hay algunos bastante buenos.

- tobben 👷

<br>

---

La fuente de texto sin formato de este manual se publica bajo la licencia GPL-2.0 y se mantiene en el repositorio hangprinter-org . Todas las imágenes y videos también se publican bajo la GPL-2.0, excepto el diagrama de cableado, que se publica bajo la licencia GPLv3.

---

Texto tomado de https://www.hangprinter.org/doc/v3/

#### Recursos

##### Social

**[Blog de desarrollo de Tobben](https://torbjornludvigsen.com/blog)**

**[Hilos de Hangprinter en el Foro RepRap](https://reprap.org/forum/list.php?423)**

**[Grupo de Facebook](https://www.facebook.com/groups/hangprinter)**

<br>

##### Repositorios

**[Modelos 3D en STL](https://gitlab.com/tobben/hangprinter/tree/Openscad_version_3/openscad_stl)**

**[Plantilla PDF](https://gitlab.com/tobben/hangprinter/blob/Openscad_version_3/layout_a4.pdf)**

**[Hangprinter](https://gitlab.com/tobben/hangprinter)**

**[Detector de colisión de línea](https://gitlab.com/hangprinter/line-collision-detector)**

**[Hangprinter.org](https://gitlab.com/tobben/hangprinter-org)**

**[Ayudante de calibración experimental para HP3](https://gitlab.com/tobben/auto-calibration-simulation-for-hangprinter)**

**[Ayudante de calibración experimental para el HP4 experimental](https://gitlab.com/tobben/auto-calibration-simulation-for-hangprinter/-/tree/buildup_compensation)**

**[El HP4 experimental](https://gitlab.com/tobben/hangprinter/-/tree/version_4_dev)**

**[Marca HP](https://gitlab.com/tobben/hp-mark)**

<br>

##### Construcciones bien documentadas

**[Fablab Chemnitz hizo una construcción HP3 bien documentada](https://wiki.fablabchemnitz.de/display/TH)**

**[El usuario de los foros de Reprap pvsfa ha documentado un poco (compilación HP3)](https://reprap.org/forum/read.php?423,868741)**

**[Compilación HP3 con Chris Riley](https://www.youtube.com/watch?v=VBc7Zab64do&list=PLB_0YGFjbOnbQ_zPnpLAjwgnE2ryhKScB)**

**[Vídeos de Hangprinter de Thomas Sanladerer]()**

<br>

{.is-info}

<!Organizados en colaboración con Precious Plastic La Habana (el nodo existente en La Habana, que forma parte de la red global Precious Plastics). Desarrollando una cultura de reciclado de plástico a partir de innovaciones de código abierto y prácticas ecológicas>

