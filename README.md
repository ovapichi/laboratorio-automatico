# laboratorio-automatico
Análisis de datos de diferentes evaluaciones biomecánicas hechas funciones para poder llamarlas desde otros lugares

Se recomienda clonar desde Google colab este repositorio para aprovechar las funciones definidas en cada script

 !git clone "[https://github.com/ovapichi/biomecanica-automatico.git](https://github.com/ovapichi/laboratorio-automatico.git)"

 y luego correr el archivo que se desea usar según la evaluación realizada.

%run "/content/biomecanica-automatico/(nombre_de_archivo).ipynb"

y luego se puede llamar directamente a las funciones por su nombre.

#Navegador

Contiene las funciones

lista = leer_carpeta (direccion) 
Recibe una dirección (Path)

Revisa cada archivo de la dirección

Devuelve una lista de todos los archivos/carpetas que estan dentro de esa dirección, sin entrar en ninguna carpeta interna

#Win Laborat

Contiene las funciones

celda_dat_csv(lista,direccion_dat,direccion_csv,direccion_equipo)

Recibe una lista de archivos .dat exportados de Win Laborat 
Recibe la dirección de la carpeta de los archivos .dat Win Laborat Celda de Cargas 
(Se recomineda que cada archivo tenga el nombre y apellido del deportista + cuad der/cuad izq/isq der/isq izq + .dat)
Recibe la dirección de la carpeta donde grabará los .csv individuales de cada deportista con sus 4 pruebas

Arma un .csv con los máximos de las 4 pruebas de fuerza isométrica de Celda de Cargas para muslos, independientemente del tiempo de duración de la prueba y la cantidad de repeticiones de la toma.

Lo exporta en la "direccion_csv"

Arma un .csv grupal con todas las jugadoras para el análisis de equipo.

Lo exporta en la direccion_equipo
