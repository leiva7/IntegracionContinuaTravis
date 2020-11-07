# Integración continua

La integración continua es un modelo que propone hacer integraciones automáticas de un proyecto lo más a
menudo posible para así poder detectar fallos cuanto antes.
Esto tiene varios beneficios, entre ellos:
- Los desarrolladores pueden detectar y solucionar problemas continuamente, sin dejarlos todos para el cierre del proyecto.
- Siempre hay una versión disponible para pruebas o prelanzamientos.
- Las pruebas unitarias se van ejecutando automáticamente.
- Todo el tiempo se monitoriza la calidad del proyecto.
 
## Travis CI

Es un servicio de integración continua que está articulado al Github, con lo cual cada vez que se hace un push al repo en el que se haya activado Travis, ejecutará los comandos definidos en el archivo .travis.yml 

## Práctico de la clase

Se generó un repo con el archivo sut.py y varios archivos de test unitarios; se creo una cuenta en [Travis CI](https://travis-ci.org) y se seleccionó el repositorio para ser vinculado. Se subió el archivo .travis.yml que contenía la instrucción de ejecución de cada uno de los test y de creación del reporte. Se agregaron los archivos y se realizó un push. 
Hubo diferentes resultados de acuerdo a lo que había sido subido, por ejemplo, [en este caso](https://travis-ci.org/github/leiva7/IntegracionContinuaTravis/builds/741797383) puede verse que falló el build porque había incluído dos tests que tenían errores en su llamado. 
En cambio [en este caso](https://travis-ci.org/github/leiva7/IntegracionContinuaTravis/builds/741802387), luego de hacer un push en el que esos test ya no se encontraban, el build fue un merge exitoso.