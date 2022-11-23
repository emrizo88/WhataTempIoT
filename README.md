# WhataTempIoT
Proyecto que embarcamos durante el bloque de IoT 3er Semestre.
Este proyecto consiste de tres sensores: sensor de flujo(ARD-370), sensor ultrasónico(HC-SR04), sensor temperatura/humedad(DHT11).
Estos sensores mediran volumen, distancia, temperatura y humedad para simular una regadera que al momento que el usuario ingrese una temperatura, el sensor de flujo detectara el movimiento del agua y en el momento que llegue a la temperatura objetivo, el agua que estaba siendo direccionada al tanque sera redirigida a la regadera. Mientras que el agua no este en la temperatura objetivo, esta agua sera direccionada a un tanque que busque ahorrar agua.

Nuestro Codigo consiste de:
BASE DATOS
	Temperatura actual
	Temperatura objetivo alcanzada (Booleano)
	Capacidad Actual Tinaco %
	Cantidad Ahorrada
	Regadera en uso (Booleano)
	Temperatura Maxima


Se ingresa la temperatura objetivo
	Se verifica que no sea mayor a temperatura maxima
Cerrar valvula check electronica de salida de regadera
Abrir llave de regadera // Usuario


Abrir valvula check electronica de tanque

loop(temperaturaActual esta fuera del rango para la temperaturaObjetivo)
	Medir capacidad tanque
	Mandar Capacidad Tanque
	if(Capacidad tanque > 80%)
		Enviar notificacion de vaciado
		Cerrar valvula check tinaco
		Sumar capacidad actual a cantidad ahorrada
		loop(SwitchVaciadoDetinaco)
			esperar a que este el tanque vacio
		
			
	Medir temperatura actual
	Mandar temperatura actual	

Notificar temperatura actual alcanzada

Loop(Esperar switch abrir regadera) //Usuario
	Medir capacidad tanque
	Mandar Capacidad Tanque
	if(Capacidad tanque > 80%)
		Enviar notificacion de vaciado
		Cerrar valvula check tinaco
		Sumar capacidad actual a cantidad ahorrada
		loop(SwitchVaciadoDetinaco)
			esperar a que este el tanque vacio
	Mandar temperatura actual

Modificar regadera en uso
Abrir valvula check regadera
Cerar valvula check tinaco

Loop(Switch regadera abrir regadera)
	checkar switch

Modificar regadera en uso //Usuario
Cerrar lalve regadera // Usuario
