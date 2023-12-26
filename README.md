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

**FUNCION 2**

### def lista_direcciones(lista,direccion)

> [!TIP]
> Utilizar la lista obtenida en la función **leer_carpeta**

***ej:** lista_de_direcciones = lista_direcciones (lista_de_archivos_de_leer_carpeta, path)*

## Win Laborat.ipynb

> [!WARNING]
> *(Cada archivo tiene que tener el nombre y apellido del deportista + cuad der/cuad izq/isq der/isq izq + .dat)*
> **Ej:** Garcia Piccinini cuad der.dat

**FUNCION 1**
### def celda_dat_csv(lista,direccion_dat,direccion_csv,direccion_equipo)
***ej:** celda_dat_csv(lista,direccion_dat,direccion_csv,direccion_equipo)*

+ Arma un .csv con los máximos de las 4 pruebas de fuerza isométrica de Celda de Cargas para muslos, independientemente del tiempo de duración de la prueba y la cantidad de repeticiones de la toma.
+ Lo exporta en la "direccion_csv"
+ Arma un .csv grupal con todas las jugadoras para el análisis de equipo.

## Fpdf.ipynb
  
**FUNCION 1** 
Obtener el nombre del archivo de "direccion_celda_final"
### def armar_pdf(nombre,protocolo,direccion_celda_final,direccion_pdf)

> [!TIP]
> Utilizar direcciones de archivos en los discos compartidos de drive para evitar problemas de path

***ej:** armar_pdf ("Garcia Piccinini Osvaldo","Fuerza isométrica con Celda de cargas en MMII", "path_csv_jugador_terminado","path_final del pdf)*


## Análisis_Celda_de_Carga.ipynb
  
**CLASE CELDA** 
Celda(4 valores máximos en el orden: CD,CI,ID,II)
Celda.ejecutar():

def ejecutar_historico_celda(self,jugadora,fecha,datos):
self= No se usa
jugadora= nombre de la jugadora
fecha = lista de fechas de cada evaluacion en formato AA-MM
datos = CD,CI,ID,II,SD,SI,HQC,HQI

> [!TIP]
> Utilizar direcciones de archivos en los discos compartidos de drive para evitar problemas de path

## Gráfico_Polar.ipynb
Arma un gráfico polar con las variables asignadas, se recomienda usar:

def grafico_polar(nombre_jugadora,tipo,etiquetas,variables,largo,fecha_test,color_list):

color_list= una lista con el formato de cada item      color = float((fecha.year-2020) + fecha.month/12 )

## Ejecutar_celda.ipynb
## Ejecutar_fotocelula.ipynb
Arman el informe del último corte de evaluación poniendole la direccion correcta

## ejecutar_historico_celda_pdf.ipynb
Arma un infome histórico de cada jugadora de celda de cargas con la función Celda.ejecutar_historico_celda con gráficos polares absolutos y relativos
