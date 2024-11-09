# Advanced Project 
## Introducción
### El objetivo de este proyecto es aplicar conceptos avanzados de Unity aprendidos en clase. Aquí se exploran habilidades como la gestión de escenas y objetos, creación de terrenos, y el uso del patrón de diseño Singleton para controladores y eventos en C#. Los paquetes utilizados incluyen:
### -  Sci-Fi Styled Modular Pack
### -  SciFiWarriorPBRHPPolyart
### -  SkySeries Freebie
### -  Input System (nuevo método de player inputs)

# Creación de la Base 
## Paso 1: Crear el Piso
### Inserta un cubo, ajusta sus dimensiones y añade una textura para simular losas de piso. Conviértelo en prefab. Asegúrate de que tenga componentes de Rigidbody y Box Collider. Crea un objeto vacío y coloca 16 copias del prefab formando un 4x4. Ajusta el tamaño según lo necesites.
![image](https://github.com/user-attachments/assets/594ea6e9-3d3b-4773-bc25-1523bbf89dc9)

## Paso 2: Crear el Template
### Debajo del piso, inserta otro cubo, llamado "template"; este cubo no llevará componentes. Ajústalo para que sea un poco más grande que el piso. 
![image](https://github.com/user-attachments/assets/3e5971ae-fb00-4b5b-b11c-41c162c863a8)

## Paso 3: Añadir Esquinas y Jugador Principal
### Selecciona una esquina y conviértela en prefab. Agrega Rigidbody y Colliders, y coloca las cuatro esquinas en un objeto vacío. Finalmente, añade el jugador principal.
![Screenshot (449)](https://github.com/user-attachments/assets/0ec73b09-0ad9-4197-9af5-90e511b07330)

## Paso 4: Colocar Paredes
### Crea un prefab de pared y añade Rigidbody y Collider. Coloca las paredes en un objeto vacío, con ocho entre cada esquina, totalizando 32 paredes.
![image](https://github.com/user-attachments/assets/29233abf-5573-43d9-9a01-97cc0251624f)

## Paso 5: Configurar Spawners de Enemigos y Añadir Skybox (adicional)
### Crea un objeto vacío llamado EnemySpawners y coloca cuatro objetos vacíos adicionales dentro. A cada uno, asígnales el siguiente script:
![image](https://github.com/user-attachments/assets/f68e9e2c-0783-43d3-922a-5fdc1638b779)
### Asegúrate de que cada spawner tenga un objeto asignado. Aquí usamos un prefab del mismo modelo del jugador, llamado Enemy. Para hacer la escena más dinámica, incluimos un skybox. 
![image](https://github.com/user-attachments/assets/cc62815e-0ff3-4bab-aa08-da707ed170d1)

## Paso 6: Componentes y Scripts para el Player, Enemy y Bala
### Para el Player, se agregó un Capsule Collider ajustado para evitar caídas y un Rigidbody. Se añadieron los scripts: Life, PlayerShooting y PlayerMovement, usando el nuevo sistema de inputs de Unity. Aquí están los scripts del Player junto con su Collider:
![image](https://github.com/user-attachments/assets/a75f8252-93fe-41e6-9d19-0952a5fd77c0)
![image](https://github.com/user-attachments/assets/7f3542a8-c125-4f67-a73f-a039febfec2d)
![image](https://github.com/user-attachments/assets/e1bbcfa3-3ec4-4d4a-b93c-69a589331520)
![image](https://github.com/user-attachments/assets/13568200-d622-45be-a72f-d3b5820c8b16)
![image](https://github.com/user-attachments/assets/616642d4-6d82-434e-be8e-08c4fc031181)

### Para el Enemy, se agregó un Capsule Collider ajustado y los scripts: Enemy, EnemyLife y ForwardMovement. A continuación, se muestran los scripts y su Collider:
![image](https://github.com/user-attachments/assets/14b85bca-6eb7-429b-88b1-395778ee8f65)
![image](https://github.com/user-attachments/assets/908ad873-b726-44cf-8c7a-cfd66b25f342)
![image](https://github.com/user-attachments/assets/18aa79ee-21f7-4e05-9c90-fedb8afdae46)
![image](https://github.com/user-attachments/assets/a39fb465-cab4-43e0-9b5b-8e3023433952)

### Finalmente, para crear la Bala, hicimos un prefab de una esfera, le asignamos un material, añadimos un Rigidbody y un Sphere Collider, ajustamos sus dimensiones y agregamos los scripts: ContactDestroy, AutoDestroy, ContactDamage y ForwardMovement. A continuación, se muestran los scripts con su Collider:
![image](https://github.com/user-attachments/assets/a37800b0-0a01-49ba-9106-da3daf151d74)
![image](https://github.com/user-attachments/assets/6e92811a-bb1e-49fd-bb67-be781f23959c)
![image](https://github.com/user-attachments/assets/3f9852e6-3839-404f-8eef-fe27d7639288)
![image](https://github.com/user-attachments/assets/cbb0d570-6f5d-4fca-a405-7d9f103097f0)
![image](https://github.com/user-attachments/assets/ab073330-0efa-48f0-af50-7b645b4e1887)

### Una vez completados todos estos pasos, tendríamos lista una maqueta básica del proyecto. El resultado debería ser el siguiente:


# Creación de la Lluvia

![Screenshot 2024-11-08 194055](https://github.com/user-attachments/assets/18ad853d-9d19-4a68-a68b-913c85ba643f)

### Se creó el prefab de una gota de lluvia utilizando una esfera y se le pusieron los scripts de Contact Destroy y Autodestroy, para que las gotas se destruyan una vez toquen el suelo y Drop Damage, para que las gotas le hagan daño al jugador.

### Además se le colocó un rigidbody con gravedad para que cayeran y  un capsule collider para que no se amontonaran las gotas al caer.

### Se crearon dos empty objects uno llamado Rain con el script para spawnear las gotas de lluvia (Rain Spawner) y un Rain Manager, con un script con el mismo nombre que se encarga de manejar las gotas que caen al escenario.

### Código de Rain Spawner:

![Screenshot 2024-11-08 201021](https://github.com/user-attachments/assets/5c630fe3-0b8f-451a-8949-bad09b5fb457)

### Código del Rain Manager:

![Screenshot 2024-11-08 195153](https://github.com/user-attachments/assets/820a0168-ec31-4fe1-8054-711b80de0d10)

# Pisos, paredes y esquinas

Se hicieron los scripts Floor y Floor Manager, para manejar los pisos y saber cuantos pisos son destruidos durante la partida.

Código de Floor:

Código de Floor Manager: 

Se hicieron los scripts Wall y Wall Manager, para saber la cantidad de paredes que  hay durante la partida.

Código de Wall:

Código de Wall Manager:

Para las esquinas se realizaron 3 scripts, Corner, Corner Manager y Contact Corner. Los primeros dos cuentan las esquinas y el último se encarga de destruir todos los pisos una vez que el jugador le dispara a las esquinas. Este código destruye todos los pisos a la vez, destruyendo el Floor Grid donde están colocados los pisos. Además de imprimir el mensaje Hit Corner en la consola.

Código de Corner:

Código de Corner Manager:

Código de Contact Corner: 


Luego se creó el script Destroy Floor, que recoge cada uno de los pisos para destruir uno aleatorio cada vez que una bala impacta contra una pared. Para generar el número random se utiliza Random Range, con un rango del 0 al 16. Se utilizó este rango porque 16 es el máximo de pisos. El número random obtenido se evalúa en un switch case, donde cada caso destruye un piso en específico. 

Código de Destroy Floor:


Layers de colisión: 

Se crearon los layers: EnemyVariant, Bullet, Drop, FloorPanel, cornerVariant y sidewallsVariant, para determinar la forma en que interactúan los objetos. Pues las balas y los enemigos no son afectados por la lluvia, en cambio el jugador sí. 

Se le aplicaron los layers a los objetos.


# Creacion de las Condiciones de Victoria y Derrota
## Creacion de Escenas de Victoria y Derrota
### Creamos dos escenas distintas a la principal. La primera la nombramos WinScreen y la segunda LoseScreen. En cada una colocamos un plano e insertamos una imagen que indicara si ganaste o perdiste. Le anadimos un skybox para darle un poco de atmosfera a las escenas. A continuacion mostramos imagenes de los resultados: 
![image](https://github.com/user-attachments/assets/2f6b179c-bad3-47a1-a6b1-82c4dff87a95)
![image](https://github.com/user-attachments/assets/d05ba787-52f4-493f-82b2-baa359221f15)
### Para manejar las transiciones a las distintas escenas, insertamos un objeto vacio llamado GameMode y le colocamos el siguiente script

### Aqui esta el r

# Opiniones Personales Sobre la Actividad

## Sebastián Negrón:

## Mayra Lago:
## Jancarlos González:
