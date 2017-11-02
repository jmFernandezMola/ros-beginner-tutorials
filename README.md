# ros-beginner-tutorials
## Tutorial 1: 
Creat el workspace als meus documents :

`txema@txema-Asus:~$ echo $ROS_PACKAGE_PATH`

`/home/txema/catkin_ws/src:/opt/ros/kinetic/share`

## Tutorial 2: 
Fet, igual que el terminal de linux, fa servir el TAB per acabar d’emplenar les possibilitats de la línia de comandes

## Tutorial 3:
S’aprèn a fer servir el `catkin_create_pkg` i es crea un package propi. A continuació es compila fent servir el `catkin_make`. Comentari: abans de veure les dependències fent servir el rospack, cal fer un `sudo rosdep init` i un `rosdep update`.
S’estudien també les dependències dels packages, les de primer ordre (declarades al fer el `catkin_create_pkg`) i les dependències de les dependències.
Finalment es modifica l’arxiu package.xml sobstituint els *TODO*

## Tutorial 4: 
S’explica amb més detall com es fa el `catkin_make`, inputs i outputs.

## Tutorial 5:
S’expliquen què són els nodes com a concepte i el roscore. S’executa per primer cop el roscore i s’aprenen algunes comandes com el:

`rosnode list`

`rosnode info /rosout`

`rosrun`

`rosnode cleanup`

## Tutorial 6:
S’introdueixen els Topics, que és una forma de comunicació publicador-subscriptor entre els diferents nodes, l’eina rqt_graph i rqt_plot. Els Topics són els canals o ports mitjançant els quals viatgen els missatges. També es veu el:

`rostopic echo` per espiar les dades publicades.

`rostopic list`

`rostopic type` per veure els tipus de missatges publicats.

`rostopic pub` per publicar dades manualment o de forma repetitiva.

`rosmsg show` per veure com estan formats els missatges.

## Tutorial 7:
S’introdueixen els Services, que és un altre tipus de missatge basat en pregunta-resposta. També s’introdueixen els paràmetres.

`rosservice type` serveix per veure com està construït el missatge (quin tipus de dades s’intercanvien).

`rosservice call` serveix per fer la crida del servei.

`rossrv show` Si es passa un tipus determinat, mostra com està composat. Un exemple de crida és el de:  `rosservice type /spawn | rossrv show`

`rosparam set` serveix per modificar un paràmetre. Que es modifiqui un paràmetre no vol dir que l’aplicació sigui immediata. Pot ser necessari demanar un servei després, per aplicar el paràmetre.

`rosparam get` serveix per obtenir els paràmetres. Una aplicació curiosa és la de rosparam get / fent servir aquesta aplicació es retorna la llista de tots els paràmetres llistats amb la funció list. Això és útil si es vol crear una foto de l’estat de configuració del sistema i guardar-la per més endavant. Això es fa:

`rosparam load` per carregar una sèrie de paràmetres.

`rosparam dump` per guardar una sèrie de paràmetres.

## Tutorial 10:
Es crea un missatge senzill amb un enter de 64 bits. Es dóna d’alta al package.xml i es prepara el CMake per a que a l’hora de construir el missatge el trobi.
Es fa servir la comanda `rosmsg show` per buscar missatges i mostrar el paquet que els conté.
L’equivalent pels serveis és el `rossrv`. Es fa el mateix procediment, però aquest cop es fa servir la comanda `roscp` per copiar un servei ja existent.
També s’aprèn com trobar ajuda amb la comanda i l’opció `-h`.

## Tutorial 11:
Es fa un "publicador" en C++ que el que fa és avisar al Master que s’enviaran missatges del tipus string a través del topic "chatter". Això es repetirà 10 cops per segon.
El listener es subscriu a "chatter"
Finalment es modifica el CMakeList  per poder compilar els arxius .c generats.
Addicionalment s’ha fet el tutorial 13 per verificar el funcionament de tot plegat.

## Tutorial 12:
És com el tutorial 11 tot i que hi ha alguna petita variació, es fa amb python. *Observació:* No cal modificar el CMakeList per compilar arxius de Python.

## Tutorials 8 i 9:
Llegits, són eines.
