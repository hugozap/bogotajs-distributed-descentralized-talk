# INTRO 
Aplicaciones distribuidas descentralizadas con JavaScript

# Motivación

* Independencia de servicios y gatekeepers.
* Revivir el espíritu creativo de la web.

# Repaso Streams en 2 minutos


[http://hugozap.com/development/2015/11/01/nodejs-streams-intro-diagrams](NodeJS Streams diagrams)

# Multicast

Capacidad para crear servicios que se anuncien y se
puedan descubrir sin conocer la dirección de la máquina
donde se alojan ( en la red local )

[https://www.npmjs.com/package/airpaste](airpaste)

# P2P y WebRTC

La característica más interesante de WebRTC son los canales de datos.
Se establece una conexión entre los nodos.
Solo se requiere de un nodo central ( por ahora ) para coordinar
el handshake inicial.

# Cómo replicar la información de manera distribuida? 

Logs > snapshots.

El log de operaciones es más importante que el snapshot de datos.
Porque con el log puedo recrear los datos.

hyperlog => Merkle DAG (Directed acyclic graph)

Replicar un hyperlog => Usando protocolo "gossip"

# Modularidad al rescate

* hyperlog
* leveldb
* webrtc-swarm
* signalhub

