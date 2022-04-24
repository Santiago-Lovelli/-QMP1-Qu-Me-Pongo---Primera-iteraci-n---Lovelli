# -QMP1-Qu-Me-Pongo---Primera-iteraci-n---Lovelli
## RESOLUCION PRIMERA INTERACION:
•	Para modelar el Atuendo lo que se es que va a ser un conjunto de prendas. Por lo que hago es crear una clase Atuendo que tiene una lista de prendas
 ![image](https://user-images.githubusercontent.com/40477288/164995426-dd1352c6-4c3c-4bcb-a671-319368c0394d.png)

•	Para las prendas lo primero que se me ocurrió es que tengan un tipoDePrenda y una categoría en donde esta sería un Enum (ya que sé que son: parte superior, calzado, parte inferior, accesorios).
 ![image](https://user-images.githubusercontent.com/40477288/164995435-0fcc6e99-dc5c-401b-a4e4-140ffee33973.png)

•	Pero esto creo que me terminaría generando un problema al tener que validar si la categoría corresponde con el tipo de la prenda. Por lo que decidí es cambiar a tener un TipoDePrenda asociado a una categoría para así poder relacionarla directamente, lo que limita a que el tipo de prenda sea una previamente cargado, pero genera una mayor robustes en el sistema. 
Esto no lo considero tan malo ya que a pesar de ser muchos los tipos de prendas existentes no creo que sean muchos para poder tenerlos previamente configurados.
 ![image](https://user-images.githubusercontent.com/40477288/164995438-2b4389cd-73db-4019-8c99-7407361c3388.png)

•	Para el manejo de la tela lo manejaría directamente con un Enum ya que así puedo evitar la repetición de datos erróneamente (podría tener un Jean con JEAN o un Shean).
 ![image](https://user-images.githubusercontent.com/40477288/164995441-93be92c4-91cd-4843-873a-41bf898242b0.png)

•	Con respecto al color al principio se me ocurrió manejarlo por string pero esto lo descarto ya que puede generar inconsistencias al tener un color Rojo y otro Rojito, por lo que prefiero manejarlos con un enum.
El problema al hacer esto es que podría generar nuevamente una inconsistencia de datos pero esta vez no al tener que tipiar el nombre sino que al elegirlo (mismamente hay colores que yo veo iguales y mi otra gente me dice que son distintos colores) y al momento de cargar los datos (hay prácticamente colores infinitos e incluso quizás el usuario quiere generar un color con un nombre especifico (rojo coca-cola o un verde cocodrilo de lacoste) por lo que me decante en generar una clase Color la cual posee los valores de red green blue que pose el color que desea cargar y nombre de dicho color para que al momento poder brindar una lista de los ya cargados y así elegirlo si lo desea (esto lo manejaría con un repositorio y así poder saber si ya existe otro color con los mismos valores darle la opción de cambiar el nombre de este color (si así lo quiere) o dejarle seleccionar este ya existente).
 ![image](https://user-images.githubusercontent.com/40477288/164995447-bdf0c5cc-a22a-4023-a1ae-24b317b4094a.png)

•	Para evitar que la prenda se cree sin tipo, tela, categoría o color primario lo manejaría en el constructor sin mayor complejidad

## Modelo Final:
![image](https://user-images.githubusercontent.com/40477288/164995486-d197ed40-5dfd-4399-8a13-17f51e5371ff.png)
