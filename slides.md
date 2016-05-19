## Aplicaciones distribuidas descentralizadas con JavaScript


## Motivación

* Open Web
* Independencia de servicios y gatekeepers.
* Revivir el espíritu creativo de la web.
* escenarios offline / conexiones intermitentes / etc.

## Repaso Streams en 2 minutos


[Diagramas de conceptos básicos de streams](http://hugozap.com/development/2015/11/01/nodejs-streams-intro-diagrams)

## Multicast ( Red Local )

Capacidad para crear servicios que se anuncien y se
puedan descubrir sin conocer la dirección de la máquina
donde se alojan ( en la red local )

[https://www.npmjs.com/package/airpaste](airpaste)
[https://github.com/mafintosh/multicast-dns](multicast-dns)

    Terminal A:
    > echo "hola" | airpaste
    Terminal B:
    > airpaste
    > hola

## Descentralización en varios frentes

* WebRTC (Comunicación entre nodos de Internet)
    - Browser
    - NodeJS
    - Desktop (Electron)
    - Mobile (Android Chrome / IOS)
    - ...

* IPFS / WebTorrent (storage)
* Blockchain, Ethereum( contratos inteligentes descentralizados)

## P2P y WebRTC

VideoConferencias => Meh...

Data Channels => Yeiii!!

## Centralizado y Descentralizado

* ![Centralizado](central.png)

* ![Descentralizado](swarm1.png)

## 1. Estableciendo conexión con otros Peers

* No necesariamente me conecto con TODOS (límites de conexiones)
* Necesitamos uno o más nodos que coordinen la conexión (Signal hub)
* Un SignalHub solo presenta peers. 

![Descentralizado](swarm2.png)

## 2. Cómo replicar información entre peers? (swarm)

* Merkle DAG (Ej => GIT)
* Arquitectura "Append Only"
* Registramos Cambios a nuestro Log
* CambioA puede depender de CambioB y CambioC
* Usamos Hash (shasum256) como llave de cada nodo (verificar integridad)
* Hash(Contenido Del Nodo + Lista de llaves a otros nodos)

## Modularidad al rescate

* hyperlog
* leveldb
* webrtc-swarm
* signalhub





