---
layout: default
title: "Sprint 3. Administración de dominios y seguridad"
---

Empezamos buscando la ip y ver que dos estar en misma red
Ip cliente  
1

Ip server
2

Instalamos el ad 
En administrar server vamos a agregar roles y caracterisitcas
3

Instalacion basada en roles y caracterisiticas
4

Selecionar un servidor
5

Elegir opcion Active Directory Domain Services (AD DS)
6

Le damos a siguiente hasta llegar a resumen y allí marcamos que queremos reiniciar server cuando termine 
7

Mientras se intala ponemos la ip del server como server dns del cliente, en mi caso es 172.16.147.129
8

Una vez instalado el ad vamos a configuracion de active directory y Indicamos que queremos busque nuevo
9

Ahora le indicamos que contraseña queremos poner 
10
Despues de eso, le dames a siguiente hasta llegar a resumen, le dejamos que se instale y se reiniciara el host
Despues de eso crear usuario en el ad
Vamos users y equipos de ad
11

12
13
14
Crear unidad formativa 
15
16
17
Para conectar el win cliente con el server, lo que hay que hacer es editar el dominio local del cliente al del server y así te conectas, reinicias
18

Y ahora entras con los credenciales que creaste en el server 
19
20
p.d, estoy usando windows server datacenter 2025 y windows 11 pro

