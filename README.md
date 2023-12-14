# laboratorio-automatico
## **Análisis de datos de diferentes evaluaciones biomecánicas hechas funciones para poder llamarlas desde otros lugares**

> [!NOTE]
> + Se recomienda clonar desde Google colab este repositorio para aprovechar las funciones definidas en cada script
> !git clone "[https://github.com/ovapichi/biomecanica-automatico.git](https://github.com/ovapichi/laboratorio-automatico.git)"
> + Correr el archivo que se desea usar según la evaluación realizada.
> %run "/content/biomecanica-automatico/(nombre_de_archivo).ipynb"
> + Llamar directamente a las funciones por su nombre.

## Navegador.ipynb
**FUNCION 1**
### def leer_carpeta (direccion)

***ej:** lista = leer_carpeta (direccion)*

**VARIABLES**
1. direccion = path de la carpeta que quiero obtener la lista

**ACCIONES**
+ Recibe una dirección (Path)
+ Revisa cada archivo de la dirección
+ Devuelve una lista de todos los archivos/carpetas que estan dentro de esa dirección, sin entrar en ninguna carpeta interna

## Win Laborat.ipynb

> [!WARNING]
> *(Cada archivo tiene que tener el nombre y apellido del deportista + cuad der/cuad izq/isq der/isq izq + .dat)*
> **Ej:** Garcia Piccinini cuad der.dat

**FUNCION 1**
### def celda_dat_csv(lista,direccion_dat,direccion_csv,direccion_equipo)
***ej:** celda_dat_csv(lista,direccion_dat,direccion_csv,direccion_equipo)*

**VARIABLES**
1. lista = la lista de archivos .dat
1. direccion_dat = path de los archivos .dat
1. direccion_csv = path de guardado de los .csv individuales
1. direccion_equipo = path de guardado del .csv de equipo

**ACCIONES**
+ Recibe una lista de archivos .dat exportados de Win Laborat 
+ Recibe la dirección de la carpeta de los archivos .dat Win Laborat Celda de Cargas
+ Recibe la dirección de la carpeta donde grabará los .csv individuales de cada deportista con sus 4 pruebas
+ Arma un .csv con los máximos de las 4 pruebas de fuerza isométrica de Celda de Cargas para muslos, independientemente del tiempo de duración de la prueba y la cantidad de repeticiones de la toma.
+ Lo exporta en la "direccion_csv"
+ Arma un .csv grupal con todas las jugadoras para el análisis de equipo.
+ Lo exporta en la direccion_equipo


## Fpdf.ipynb
  
> [!WARNING]
> **FUNCION 1** INCOMPLETO
> Obtener el nombre del archivo de "direccion_celda_final"
> ### def armar_pdf(nombre,protocolo,direccion_celda_final,direccion_pdf)

> [!TIP]
> Utilizar direcciones de archivos en los discos compartidos de drive para evitar problemas de path

***ej:** armar_pdf ("Garcia Piccinini Osvaldo","Fuerza isométrica con Celda de cargas en MMII", "path_csv_jugador_terminado","path_final del pdf)*

**VARIABLES**
1. nombre = nombre del deportista
2. protocolo = nombre del protocolo
3. direccion_celda_final = "path del archivo donde se guardaron todos los datos procesados del jugador"
4. direccion_pdf = "path de la carpeta para guardar el pdf armardo"

**ACCIONES**
+ Recibe el nombre del club y el protocolo para el pdf
+ Recibe la dirección del archivo final procesado del jugador para obtener todos los datos necesarios para poner en el informe
+ Arma el informe del jugador en formato pdf
+ Exporta el archivo .pdf en la direccion_pdf


