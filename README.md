# DataMania
Código realizado en Python para el concurso Data Manía aplicado el 22 de octubre durante el Foro de Estadística celebrado en la UV

## Descripcion del problema
Se encontraron problemas de tipo espacial dentro de la base ya que las coordenadas proporcionadas no correspondían al lugar propuesto, es decir, existe un desplzamiento de 65km del lugar de donde orginalmente de explica el lugar.
Aún con estos problemas se decidió continuar con el análisis en la ubicación dada (Mérida, Yucatán) actualizando las covariables

## Covariables
Las covariables que se utilizaron son:
"vph_pisoti","vph_c_elec","vph_s_elec","vph_aeasp","vph_aguafv","vph_tinaco","vph_letr","vph_drenaj","vph_nodren","vph_c_serv","vph_dsadma","vph_lavad","graproes","precip_promedio","evap" y "tem_p_semana". Estas están disponibles en el catálogo de Inegi dentro de la siguiente liga ()

## Ubicación geográfica
Como se explicaba anteriormente, se utilizó el .shp de Mérida, Yucatán como archivo geográfico debido a que las coordenadas proporcionadas en eggs_data.csv no corresponden al lugar de interés.

## Código Colab
El script de python "CodigoColab" funciona como su nombre lo indica en Colab debido a las posibles limitaciones técnicas de los equipos de computo personales. Para la ejecucion de este script se debe de concetar al entorno de ejecucion gratuito y cargar los datos eggs_data.csv y covariables_con_decimales.xlsx adjuntos en este mismo repositorio.
Así mismo el script "Datamania" corre en una computadora localmente, simplemente hay que descargar el script junto con los archivos necesarios en la misma carpeta y correrlo en cualquier IDE. Los resultados se crearán en la misma carpeta. Este método puede resultar demandante para algunas computadoras que no cuenten con los recursos suficientes.
Con respecto al archivo .rar, se debe descomprimir y cargar los todos los archivos que contiene para realizar el maapa final.

## Resultados
El modelo propuesto es un Random Forest con XGBoost para capturar la parte espacial en los datos en donde las medidas obtenidas son:
Para el conjunto de entrenamiento:
R2: 44%, RMSE: 27.3, MAE: 12.9
Para el conjunto de prueba son:
R2: 41%, RMSE: 28.5, MAE 13.4 
El R2 nos indica que explica de un 41$ a un 44% de la variablilidad de los datos con un error cuadratico medio de 27 a 28 huevos por trampilla y un error absoluto medio de 12 a 13 huevos por trampilla

## Mapas
En los mapas se expresan los datos predichos para la variable objetivo eggs en el lugar.