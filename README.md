# Data Dashboard

* **Track:** _Common Core_
* **Curso:** _Creando tu primer sitio web interactivo_
* **Unidad:** _Producto final_

***

## Flujo de trabajo

1. Debes realizar un [**fork**](https://gist.github.com/ivandevp/1de47ae69a5e139a6622d78c882e1f74)
   de este repositorio.

2. Luego deberás **clonar** tu fork en tu máquina. Recuerda que el comando a usar
   es `git clone` y su estructura normalmente se ve así:

   ```bash
   git clone https://github.com/<nombre-de-usuario>/freelancer.git
   ```

3. Cuando hayas terminado tu producto, envía un Pull Request a este repositorio
   (puedes solicitar apoyo de tus profes para este paso).

> Nota: No olvides que es una buena práctica describir tu proyecto en este
> archivo `README.md` y también desplegar tu web a Github Pages :smiley:.

# Requerimientos
### Datos revisados por los TMs:

##### 1.	El total de estudiantes presentes por sede y generación.
>El total de elementos del arreglo “estudiantes” (.length) = El total de estudiantes  por sede.          
>3 Generaciones: 2016-2, 2017-1 y 2017-2     
>Total  de estudiantes generación 2016-2 = 15

#### 2.	El total de estudiantes presentes por sede y generación.
> Active: false
> Llamar todos los false y ponerlos en un arreglo para sacar su longitud por .length         
> Fórmula:  (false.length x 100)/Total de estudiantes(1)

#### 3.	La cantidad de estudiantes que superan la meta de puntos en promedio de todos los sprints cursados. La meta de puntos es 70% del total de puntos en HSE y en tech.

>Tomar en cuenta 3 raitings 1 por cada generación.  raitings[1].supera

#### 4.	El porcentaje que representa el dato anterior en relación al total de estudiantes.

>Porcentaje de supera = (Total de estudiantes supera(3) x 100)/ Total de estudiantes(1)

#### 5.	El Net Promoter Score (NPS) promedio de los sprints cursados. El NPS se calcula en base a la encuesta que las estudiantes responden al respecto de la recomendación que darían de Laboratoria, bajo la siguiente fórmula:

>	Sumar con un for  += raitings[i].nps.promotors*       
>	Sumar con un for  += raitings[i].nps.detractors*        	                 
Calcular [NPS] = [Promoters] - [Detractors]

#### 6.	La cantidad y el porcentaje que representa el total de estudiantes que superan la meta de puntos técnicos en promedio y por sprint.
>En promedio:  Acceder a tech sumarlos y dividir entre numero de sprints(number)
              for students[i] i<total de estudiantes
              for total += sprint[i].score.tech  
              Obtener promedio: total/número de sprints
              Verificar cuantas superan la meta: if total >= meta ponerlas en un contador
              Obtener porcentaje en referencia al total de alumnas: (contador x 100)/total de alumnas
>Por sprint*:  Acceder a tech por sprint(number)
              Acceder a tech sumarlos y dividir entre numero de sprints(number)
              for total += sprint[i].score.tech
              for students[i] i<total de estudiantes
              Obtener promedio por sprint: total/número de alumnas
              Verificar cuantas superan la meta: if total >= meta ponerlas en un contador
              Obtener porcentaje en referencia al total de alumnas: (contador x 100)/total de alumnas

#### 7.	La cantidad y el porcentaje que representa el total de estudiantes que superan la meta de puntos de HSE en promedio y por sprint.
>En promedio:  Acceder a HSE sumarlos y dividir entre numero de sprints(number)
              for students[i] i<total de estudiantes
              for total += sprint[i].score.hse  
              Obtener promedio: total/número de sprints
              Verificar cuantas superan la meta: if total >= meta ponerlas en un contador
              Obtener porcentaje en referencia al total de alumnas: (contador x 100)/total de alumnas
>Por sprint*:  Acceder a HSE por sprint(number)
              Acceder a tech sumarlos y dividir entre numero de sprints(number)
              for total += sprint[i].score.hse
              for students[i] i<total de estudiantes
              Obtener promedio por sprint: total/número de alumnas
              Verificar cuantas superan la meta: if total >= meta ponerlas en un contador
              Obtener porcentaje en referencia al total de alumnas: (contador x 100)/total de alumnan

#### 8.	El porcentaje de estudiantes satisfechas con la experiencia de Laboratoria.
>Acceder a promotors, por medio de un for sumar los puntos por sprint(total): raitings[i].nps.promotors* Dónde i es < el número de sprints                     
>Obtener porcentaje: (total x 100)/(total de alumnas x número de sprints).

>Dónde el total de alumnas = promotors + passive + detractors

#### 9.	La puntuación promedio de l@s profesores.
>Acceder por medio de un for a 'teacher' y sumar los puntos por sprint:  raitings[i].teacher Dónde i es < el número de sprints.                           
>El total de puntos dividirlo entre el número de sprints

#### 10.	La puntuación promedio de l@s jedi masters.
>Acceder por medio de un for a 'jedi' y sumar los puntos por sprint: raitings[i].jedi Dónde i es < el número de sprints     
>El total de puntos dividirlo entre el número de sprints

### Extras:
#### 1.	Mostrar los datos procesados en un gráfico como el diseño propone u otra alternativa.
>Google chart

#### 2.	Tener un botón que permita indicar que una estudiante ha salido del Bootcamp y alterar los totales afectados por este cambio.**
>Active: false
