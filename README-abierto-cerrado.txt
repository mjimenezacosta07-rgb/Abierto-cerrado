principio abierto / cerrado 
en el principio nos dice que una clase debe estar abierta para extenderse pero cerrada para poder modificarse ósea, si necesita agregar algo nuevo, se crea código nuevo en vez de cambiar el código que ya funciona 

un ejemplo es un enchufe, para conectarlo una lampara o un cargador no hay que abrir la pared y cambiar los cables solos e conecta un aparato nuevo

Como se implementa 
La clase producto lo tiene todos los productos: nombre y precio, esta clase queda cerrada y no se modifica 

cuando se necesitan productos de datos distintos se crean clases nuevas que heredan de un producto (eso es extenderla)

físico hereda de producto y le agrega peso
digital hereda de producto y le agrega el filepath (que es la ruta del archivo)

si mañana se necesita otro tipo de producto se crea otra clase hija y producto no se toca si no se cumpliera el principio , lo que habría es que tendríamos que meter peso y filepath dentro del producto y cambiar esa clase cada vez que aparece un tipo de producto nuevo 



Expolicacion de los archivos 

producto.h 
declara clase producto y deja 2 atributos el nombre y el precio tiene constructor destructor virtual y metodos get y set para precio y nombre

producto.cpp
escribe lo que hacen los metodos de producto: getnombre y getprecio devuelven los datos a los sets correspondientes

fisisco.h 
declara la clase fisico y hereda el producto  y agrega ñ atributo peso y sus metodos get y set 


fisico.cpp
escribe lo que hacen los getpeso y set peso

dijital.h
declara la clase dijital que tanbien heredan de producto y agrega el atributo filepath y sus mretodos getfilepath y setfilepath

dijital.cpp 
escribe lo que hacen getfilepath y setfilepath

Main
crea el producto físico 
crea el producto dijityal 
muestra el peso del producto físico y la rura del digital 