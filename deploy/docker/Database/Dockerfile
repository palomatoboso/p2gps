FROM mongo:3.4

MAINTAINER paloma.toboso@alu.uclm.es
#/data/db/ sera el volumen usado para persistencia de sesion
COPY drop/* usr/local/data/db/

#CMD es lo mismo que ENTRYPOINT pero con otro formato
CMD ["mongod", "--smallfiles", "--rest"]