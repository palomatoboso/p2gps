FROM openjdk:8-jre

MAINTAINER pablo.bermejo@uclm.es

RUN mkdir -p /usr/local/app

#WORKDIR /usr/local/app/

#copiar el .jar del servicio a la imagen
#no se indica el nombre porque las versiones cambian
COPY drop/*.jar usr/local/app/

#copiar script que se ejecuta al lanzar el contenedor
COPY drop/run.sh usr/local/app/run.sh


#si ejecutamos la imagen en local, este servicio tendria acceso
#a la ip del host de Mongo, pero como lanzamos pila
#de servicio Docker la ip MongoDB no puede descubir
# que se la pasemos en un archivo en propiedades
COPY drop/application.properties application.properties

EXPOSE 8080

ENTRYPOINT sh usr/local/app/run.sh
