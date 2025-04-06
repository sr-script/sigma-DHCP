# DHCP Sigma Daemon con interfaz grafica alaverga para que quede asi bien maniacote 

** Es un servidor DHCP personalizado que estoy haciendo con python para practicar y ajá, desarrollado con python supongo
quiero que permita gestionar IPs <para q aprenda de redes pq soy un maldito infgorante y eso

## Objetivo
	Asignar dinamicamente direcciones IP a los dispositivos de la red
	visualizar los dispsoitosvos conectados
	detectar comportamientos sospechosos de usuarios y que los vote alaverga xdxdxdddxd (aun no se como, pero creo q el profe lo dijo en una clase o algo asi, estaba disociando)
	hacer q daniel (yo) piense en otra cosa q no sea comer compusiltavamente(opcinal)	

## Q cosas voy a usar
	primero q nada supongo Python pq es el unico lenguake al q mas o menos le se, lo cual es preocupante ya q no le se mucho
	Scapy pq dice google q sirve para manejar paquetes (whatever that means)
	Tkinter | como soy una puta verga le voy a meter interfaz grafica asi q investigué y al parecer esta madre es para hacer eso
	Bash para los scripts de automatizacion como nos enseñó el porfe 
	Coca cola con Monter para q piense mejor pq sino solo me quedo viendo a la pared jaja que pedo

###### estructura
	Como no soy un puto retrasado de mierda, aun recuerdo q en parasigmas de la programacion (materia que probablemente reoproeb) vimos de q se tiene q esgtructurasr y carpetas y eso, entonces ps va asi creo

	dhcp_sigma_daemon/
	|- server/				# Lógica del server DHCP
	|- gui/					# Interfaz grafica
	|- utils/				# los scripts q va a usar (Bash)
	|- sniffer/				# sniffer opcional (pq no somos script kdieds y asi)
	|- README.md			# este documento xdxdxdxd
	|- requirements.txt		# Dependencias de python ncesarias para cuando alguien baje esta madre de github pueda usarlo pq va a tenre cos python 


#### Links a cosas que investigue para entenderle a esto
	RFC 2131 
		https://www.ietf.org/rfc/rfc2131.txt

	Documentación de Scapy
		https://scapy.readthedocs.io/en/latest/


#### PARA ENTENDER EL FUNCIONAMIENTO DE DHCP
	Hasta el momento sabemos que DHCP posee 3 mecanismos para la conexión de direcciones IP:
		- Asignación Automatica
			Asigna automaticamente (bruh) direcciones IP permanentes a los clientes, esa dirección queda reservada para ese cliente asi que no se reutiliza si el cliente se desconecta, asiq ue eno es tan eficiente en lugares donde los clientes entren y salgan varias veces como la fockin RIUV 

		- Asignación Dinamica
			DHCP asigna de manera temporal por un perioso limitado de tiempo (o hasta que el cliente renuncie a ella) una dirección IP
			# | Este tipo de asignación es el unico de los 3 mecanismos que permite reutilizar automaticamente una dirección que el cliente ya no necesite, osea que si un cliente se desconecta y libera una direccion, DHCP puede reasignarla a otro cliente

		- Asignación Manual 
			El Sysadmin asigna las direcciones IP a los clientes mediante la MAC
			Esta configuración se pasa por el arco del triunfo la configuración manual del dispositivo pero a cambio nos da el maldito poder total de asignar las direcciones a los sysadmins jajajajajajajajajajajajajajajajjajajajajajajjajajajajajajajajajajajajajajajajajajajajajajajajajajajjajajajajajaja
				
JAJA QUE PEDO, DESPUES DE LEER TODO EL RFC 2131 ME DI CUENTA DE QUE NECESITO UN SWITCH PARA PODER PROBAR Y HACER ESDTO JAJAJA SE QUEDA EN PAUSA HASTA NUEVO AVISOP
