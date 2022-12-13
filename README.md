![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png) 

# <h1 align="center">**`Proyecto Individual 2`**
# <h1 align="center">**`Machine Learning`**

## Descripción de la problematica
La hospitalización, o estancia hospitalaria, cuando es prolongada constituye una preocupación a nivel mundial debido a sus efectos negativos en el sistema de salud, aumentando los costos, generando deficiencia en la accesibilidad de prestación de servicios de salud, saturación de unidades de hospitalización y urgencias, por consiguiente, mayores efectos adversos como lo son las enfermedades intrahospitalarias.

El estudio de los procesos de atención en salud, así como el conocimiento de las características y perfiles de los usuarios con el objetivo de predecir la ocupación hospitalaria, es uno de los aspectos al que las autoridades de salud han prestado gran interés, pues permite no sólo garantizar los recursos necesarios para la atención del paciente, sino realizar ajustes respecto a la oferta y demanda de los servicios de salud y los implementos asociados.

## Descripción del proyecto: </br>   
En este proyecto usaremos python para crear un modelo predictivo de Machine Learning con el cual vamos a predecir si un paciente tendrá una estancia hospitalaria prolongada o no, utilizando la información contenida en el dataset asociado, la cual recaba una muestra histórica de sus pacientes, para poder administrar la demanda de camas en el hospital según la condición de los pacientes recientemente ingresados. 

Para esto, se define que un paciente posee estancia hospitalaria prolongada si ha estado hospitalizado más de 8 días. Por lo que generamos dicha variable categórica y luego categorizamos los pacientes según las variables que consideramos necesarias, justificando dicha elección.   </br>

Nuestros datos estan dividos en dos grupos, unos que usaremos para entrenar el modelo (train) y unos que usaremos para testear ese modelos (test) nuestro fin con este modelo de ML es permitir clasificar el tiempo de estancia de los pacientes, utilizando los datos que se han puesto a nuestra disposición. </br>

Para esto, específicamente, debemos predecir la **categorización** de la estancia hospitalaria del paciente considerando que se considera una estancia prolongada cuando es mayor a 8 dias.  </br>

Como método de evaluación del desempeño del modelo, se utilizará la métrica de Exhaustividad (Recall) para las estadías hospitalarias largas, a partir de la matriz de confusión (Confusion Matrix). 


$$ Recall=\frac{TP}{TP+FN}$$


Donde $TP$ son los verdaderos positivos y $FN$ los falsos negativos.

Como métrica adicional para verificar el desempeño de su modelo, también se utilizará la métrica de precisión (Accuracy) para las estadías hospitalarias largas.

$$ Accuracy=\frac{TP+TN}{P+N}$$

siendo $TP$ los verdaderos positivos, $TN$ verdaderos negativos y $P+N$ población total.


## Descripción de los archivos
 - 'hospitalizaciones_train.csv': Contiene 410000 registros y 15 dimensiones, el cual incluye la información **numérica** de la cantidad de días de estancia hospitalaria.
 - 'hospitalizaciones_test.csv': Contiene 90000 registros y 14 dimensiones, el cual no incluye la información de la cantidad de días de estancia hospitalaria.

## Descripción de las dimensiones de los archivos 
- Available Extra Rooms in Hospital: Habitaciones adicionales disponibles en el hospital. Una habitación no es igual a un paciente, pueden ser individuales o compartidas.
- Department: Área de atención a la que ingresa el paciente. 
- Ward_Facility_Code: Código de la habitación del paciente.
- doctor_name: Nombre de el/la doctor/a a cargo del paciente.
- staff_available: Cantidad de personal disponible al momento del ingreso del paciente.
- patientid: Identificador del paciente.
- Age: Edad del paciente.
- gender: Género del paciente.
- Type of Admission: Tipo de ingreso registrado según la situación de ingreso del paciente.
- Severity of Illness: Gravedad de la enfermedad/condición/estado del paciente al momento del ingreso.
- health_conditions: Condiciones de salud del paciente. 
- Visitors with Patient: Cantidad de visitantes registrados para el paciente.
- Insurance: Indica si la persona posee o no seguro de salud. 
- Admission_Deposit: Pago realizado a nombre del paciente, con el fin de cubrir los costos iniciales de internación. 
- Stay (in days): Días registrados de estancia hospitalaria. 

## Fases del proyecto
1. Carga y visualización de los archivos de train y test en un dataframe de pandas
2. Preprocesamiento de datos
3. Creación y grafica de la correlación
4. Creacion del modelo
5. Entrenamiento del modelo
6. Test del modelo
7. Creación de la matriz de confusión
8. Evaluación del modelo
9. Predicción con el dataset de test
10. Exportamos 