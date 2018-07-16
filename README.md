# Demonstração de Leak para o TDC

	@author:Evandro Franco
	@author:Helio Silva
	
Este projeto é uma demo para o TDC (2018) na trilha de Java enterprise. 

Serão gerados dois tipos de contenção:

	1- Memory Leak 
	2- Contenção em Threads
	
## Instruções Gerais

Por se tratar de um projeto Web, bem simples, basta subir um container de sua preferência (Jboss, Tomcat, etc.) e fazer o deploy do projeto.

Após escolher o container, adicionar o .jar que faz referência aos módulos Web (servlet).

Na nossa demo, adicionamos o Wildfly 11 no Eclipse, e adicionamos os seguintes argumentos de JVM:

	-server -Xms64m -Xmx512m -XX:+HeapDumpOnOutOfMemoryError -verbose:gc
	
## 1-Memory Leak

Para testar o servlet que gera o memory leak, basta acessar a URL abaixo:

	http://localhost:8080/Web_leak/LeakServlet


## 2-Contenção em Threads

Para acessar o servlet que bloqueia as threads, basta acessar:

	http://localhost:8080/Web_leak/LeakServlet2
	
	 