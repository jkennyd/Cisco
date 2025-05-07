#Configuração de Time-Range

## Objetivo
Utilizar recurso time-range em switches Cisco, permitindo aplicar políticas com base em horários/dias específicos.

## O que é Time-Range?

Basicamento o __time-range__ é uma funcionalidade usada para aplicar configurações com base em *horários e dias da semana. Pode ser utilizado em conjunto com **ACLs (Access Control Lists)* para permitir ou negar tráfego apenas em determinados períodos.

---

## POP
_Entrar no modo de configuração global_
~~~bash
configure terminal
~~~

_Adicionar nome ao time-range_
~~~bash
time-range [WORD<1-32] 
~~~

_Configuração do time-range_
<!--Em dispositivos Cisco, periodice absolutesão usados ​​para definir intervalos de tempo. periodicdefine períodos de tempo recorrentes dentro de um dia, semana ou mês. absolutedefine uma data e hora específicas ou um intervalo entre duas datas e horas-->
~~~bash

~~~




#Após configurar o nome o switch retorna este valor: Cisco(config-time-range)#
~~~bash
time-range HORARIO_COMERCIAL
 periodic Monday Friday 08:00 to 18:00
~~~
