# Clase
El profesor creó un respositorio ya que tenía un directorio en su
computadora con lo que quería subir. Yo logré dicho procedimiento con
```
$ git init
$ git commit -m "blah blah blah"
$ git remote add origin url_del_proyecto
$ git push origin master
```

secretopineda creo un fork del repositorio de davidamaro. Cuando clonó
el repositorio (no recuerdo de quien) `$ git remote -v` traia por
defecto `origin` que apuntaba a __secretopineda__.

__secretopineda__ editó el archivo tarea1.md que venía de davidamaro
Hice
```
$ git push fork master
```

Vamos a hacer un cambio con __davidamaro__ y vamos a ver qué hace al
hacer git pull __secretopineda__.

Para actualizar el respositorio con el contenido de la clase, i.e.,
sólo ver:
```
$ git pull benet master
```
Para actualizar el repositorio con tareas, i.e., editar contenido:
```
$ git push/pull david master
```

## Manejo de pull request
Vamos a averiguar cómo funcionan los pull request. Para ello,
necesitamos editar un nuevo archivo con __secretopineda__ que no tenga
__davidamaro__.
