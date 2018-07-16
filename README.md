# Demonstra��o de Leak para o TDC

	@author:Evandro Franco
	@author:Helio Silva
	
Este projeto � uma demo para o TDC (2018) na trilha de Java enterprise. 

Ser�o gerados dois tipos de conten��o:

	1- Memory Leak 
	2- Conten��o em Threads
	
## Instru��es Gerais

Por se tratar de um projeto Web, bem simples, basta subir um container de sua prefer�ncia (Jboss, Tomcat, etc.) e fazer o deploy do projeto.

Ap�s escolher o container, adicionar o .jar que faz refer�ncia aos m�dulos Web (servlet).

Na nossa demo, adicionamos o Wildfly 11 no Eclipse, e adicionamos os seguintes argumentos de JVM:

	-server -Xms64m -Xmx512m -XX:+HeapDumpOnOutOfMemoryError -verbose:gc
	
## 1-Memory Leak

Para testar o servlet que gera o memory leak, basta acessar a URL abaixo:

	http://localhost:8080/Web_leak/LeakServlet


## 2-Conten��o em Threads

Para acessar o servlet que bloqueia as threads, basta acessar:

	http://localhost:8080/Web_leak/LeakServlet2
	
	 