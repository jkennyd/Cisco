# Configuração de Time-Range

## Objetivo
Utilizar recurso time-range em switches Cisco, permitindo aplicar políticas em horários/dias específicos para controlar o status operacional de uma porta Cisco com base no tempo.

## O que é Time-Range?

Basicamento o __time-range__ é uma funcionalidade usada para aplicar configurações com base em *horários e dias da semana. Pode ser utilizado em conjunto com **ACLs (Access Control Lists)* para permitir ou negar tráfego apenas em determinados períodos.

---

## Etapa 1: criar e configurar o time-range
_Entrar no modo de configuração global_
~~~bash
configure terminal
~~~
<br>

_Adicionar nome ao time-range_
~~~bash
time-range [WORD<1-32>] 
~~~
<br>

_Configuração do time-range_
<br>
_Após configurar o nome o switch retorna este valor: Cisco(config-time-range)#_
~~~bash
periodic [sun,mon,tue,wed,thu,fri,sat,daily,weekdays,weekend] HH:MM to HH:MM
~~~
<sup>Dica: em dispositivos Cisco, existe o __periodic__ e __absolute__, que são usados ​​para definir intervalos de tempo. __periodic__ define períodos de tempo recorrentes dentro de um dia, semana ou mês. __absolute__ define uma data e hora específicas ou um intervalo entre duas datas e horas.
</sup><br><br>

_Depois de configurado saia do modo de configuração global_
~~~bash
end
~~~
<br>

_Consultar a configuração feita (opcional)_
~~~bash
show time-range HORARIO_COMERCIAL
~~~
<br>

---

## Etapa 2: adicionar time-range na interface desejada
_Entrar no modo de configuração global_
~~~bash
configure terminal
~~~
<br>

_Selecione a(s) interface(s) que deseja configurar_
~~~bash
interface GigabitEthernet [1-24]
~~~
ou
~~~bash
interface range GigabitEthernet <1-24>
~~~
<br>

_Aplicar time-range configurado anteriormente na(s) interface(s)_
~~~bash
operation time-range [WORD <1-32>]
~~~
<sup>Dica: o comando operation time-range no modo de configuração da interface permite especificar um intervalo de tempo durante o qual a porta estará habilitada ou desabilitada. Você pode então usar esse intervalo de tempo para controlar o status operacional da porta.</sup><br><br>


_Depois de configurado saia do modo de configuração global_
~~~bash
end
~~~
<br>

_Salve as configurações na memoria do switch_
~~~bash
write
~~~
ou
~~~bash
copy running-config startup-config
~~~








