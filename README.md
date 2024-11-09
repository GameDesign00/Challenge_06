# Advanced Project 
## Introducción
### El objetivo de este proyecto es aplicar conceptos avanzados de Unity aprendidos en clase. Aquí se exploran habilidades como la gestión de escenas y objetos, creación de terrenos, y el uso del patrón de diseño Singleton para controladores y eventos en C#. Los paquetes utilizados incluyen:
### -  Sci-Fi Styled Modular Pack
### -  SciFiWarriorPBRHPPolyart
### -  SkySeries Freebie
### -  Input System (nuevo método de player inputs)

# Parte I: Diseño del Escenario Principal
## Paso #1: Crear el Piso
### Inserta un cubo, ajusta sus dimensiones y añade una textura para simular losas de piso. Conviértelo en prefab. Asegúrate de que tenga componentes de Rigidbody y Box Collider. Crea un objeto vacío y coloca 16 copias del prefab formando un 4x4. Ajusta el tamaño según lo necesites.
![image](https://github.com/user-attachments/assets/594ea6e9-3d3b-4773-bc25-1523bbf89dc9)

## Paso #2: Crear el Template
### Debajo del piso, inserta otro cubo, llamado "template"; este cubo no llevará componentes. Ajústalo para que sea un poco más grande que el piso. 
![image](https://github.com/user-attachments/assets/3e5971ae-fb00-4b5b-b11c-41c162c863a8)

## Paso #3: Añadir Esquinas y Jugador Principal
### Selecciona una esquina y conviértela en prefab. Agrega Rigidbody y Colliders, y coloca las cuatro esquinas en un objeto vacío. Finalmente, añade el jugador principal.
![Screenshot (449)](https://github.com/user-attachments/assets/0ec73b09-0ad9-4197-9af5-90e511b07330)


## Paso #4: Colocar Paredes
### Crea un prefab de pared y añade Rigidbody y Collider. Coloca las paredes en un objeto vacío, con ocho entre cada esquina, totalizando 32 paredes.
![image](https://github.com/user-attachments/assets/29233abf-5573-43d9-9a01-97cc0251624f)

## Paso #5: Configurar Spawners de Enemigos y Añadir Skybox (adicional)
### Crea un objeto vacío llamado EnemySpawners y coloca cuatro objetos vacíos adicionales dentro. A cada uno, asígnales el siguiente script:
![image](https://github.com/user-attachments/assets/f68e9e2c-0783-43d3-922a-5fdc1638b779)
### Asegúrate de que cada spawner tenga un objeto asignado. Aquí usamos un prefab del mismo modelo del jugador, llamado Enemy. Para hacer la escena más dinámica, incluimos un skybox. 
![image](https://github.com/user-attachments/assets/cc62815e-0ff3-4bab-aa08-da707ed170d1)

## Paso 6: 
### Los siguientes scripts son importantes para el funcionamiento del proyecto. A continuacion, pon estos scripts al enemigo: Enemy, EnemyLife y EnemyMovement
![image](https://github.com/user-attachments/assets/14b85bca-6eb7-429b-88b1-395778ee8f65)
![image](https://github.com/user-attachments/assets/908ad873-b726-44cf-8c7a-cfd66b25f342)
![image](https://github.com/user-attachments/assets/18aa79ee-21f7-4e05-9c90-fedb8afdae46)


# Parte II: La Lluvia

![Screenshot 2024-11-08 194055](https://github.com/user-attachments/assets/18ad853d-9d19-4a68-a68b-913c85ba643f)

### Se creó el prefab de una gota de lluvia utilizando una esfera y se le pusieron los scripts de Contact Destroy y Autodestroy, para que las gotas se destruyan una vez toquen el suelo y Drop Damage, para que las gotas le hagan daño al jugador.

### Además se le colocó un rigidbody con gravedad para que cayeran y  un capsule collider para que no se amontonaran las gotas al caer.

### Se crearon dos empty objects uno llamado Rain con el script para spawnear las gotas de lluvia (Rain Spawner) y un Rain Manager, con un script con el mismo nombre que se encarga de manejar las gotas que caen al escenario.

### Código de Rain Spawner:

![Screenshot 2024-11-08 201021](https://github.com/user-attachments/assets/5c630fe3-0b8f-451a-8949-bad09b5fb457)

### Código del Rain Manager:

![Screenshot 2024-11-08 195153](https://github.com/user-attachments/assets/820a0168-ec31-4fe1-8054-711b80de0d10)


# Parte III: Suelos y Paredes

### Se hicieron los scripts Floor y Floor Manager, para manejar los pisos y saber cuantos pisos son destruidos durante la partida.

# Parte IV: 

# Parte V: 

# Opiniones Personales Sobre la Actividad

## Sebastián Negrón:

## Mayra Lago:
## Jancarlos González:
