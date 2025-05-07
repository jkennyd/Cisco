# Configuração de Time-Range

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
<br>
_Dica:_
<br>
<sup>
  Em dispositivos Cisco, existe o __periodic__ e __absolut__, que são usados ​​para definir intervalos de tempo. __periodic__ define períodos de tempo recorrentes dentro de um dia, semana ou mês. __absolut__ define uma data e hora específicas ou um intervalo entre duas   datas e horas
</sup>
<br>
_Após configurar o nome o switch retorna este valor: Cisco(config-time-range)#_
~~~bash
periodic [sun,mon,tue,wed,thu,fri,sat,daily,weekdays,weekend] HH:MM to HH:MM
~~~





~~~bash
time-range HORARIO_COMERCIAL
 periodic Monday Friday 08:00 to 18:00
~~~
