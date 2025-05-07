#Configuração de Time-Range

## Objetivo
Utilizar recurso time-range em switches Cisco, permitindo aplicar políticas com base em horários/dias específicos.

## O que é Time-Range?

time-range é uma funcionalidade usada para aplicar configurações com base em *horários e dias da semana. Pode ser utilizado em conjunto com **ACLs (Access Control Lists)* para permitir ou negar tráfego apenas em determinados períodos.

---

## POP
_Entrar no modo de configuração global_
~~~bash
configure terminal
~~~
__Configurar nome do time-range__
~~~bash
time-range [WORD<1-32] 
~~~

~~~bash

~~~




#Após configurar o nome o switch retorna este valor: Cisco(config-time-range)#
~~~bash
time-range HORARIO_COMERCIAL
 periodic Monday Friday 08:00 to 18:00
~~~
