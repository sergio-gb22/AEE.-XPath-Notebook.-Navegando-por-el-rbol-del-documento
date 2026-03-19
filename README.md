# AEE.-XPath-Notebook.-Navegando-por-el-rbol-del-documento

## Reto 1: Filtrado por contenido y estado. El departamento de desarrollo necesita actualizar su bibliografía sobre diseño. Obtén los títulos de todos los recursos cuya categoría sea 'CSS' y que, además, estén marcados como disponibles (true).
//recurso[categoria='CSS' and disponible='true']/titulo /string()
dentro de [] pongo and porque quiero que busque estas dos verificaciones que son categoria y disponibilidad

## Reto 2: Atributos y negaciones. No todos nuestros recursos son documentos estándar. Queremos identificar aquellos materiales que tienen un formato especial. Selecciona los ID (el atributo id) de todos los recursos cuyo formato no sea "PDF".
//recurso[@formato!='PDF' or not(@formato) ]/@id /string()

pongo or ya que quiero que busque que el formato no sea PDF o no tenga formato (not(@formato))

## Reto 3: Manejo de múltiples nodos (Autores). La colaboración es clave en la ciencia. Localiza y muestra únicamente el nombre del primer autor de aquellos recursos que han sido publicados después del año 2015.
//recurso[anio>2015]/autor[1] /string()
el [1] porque quiero que sean los primeros 

##Reto 4: Consultas de complejidad técnica (Nivel y Categoría). Buscamos material para un seminario avanzado de arquitectura de datos. Necesitamos los títulos de los recursos que pertenezcan a las categorías de "XPath" o "XSLT" y que tengan un nivel de dificultad de 5.
//recurso[categoria='XPath' or categoria='XSLT' and nivel=5]/titulo /string()
pongo or porque quiero que busque que sea de categoria XPath o XSLT y and porque quiero que tambien sea de nivel de dificultad 5
