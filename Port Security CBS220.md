# Port Security - CBS220 - 24P 4T

## Objetivo
Habilitar o Port Security no Cisco CBS220.

É um recurso que controla quais dispositivos
podem se conectar a uma interface do switch, com base nos endereços MAC. Ele
ajuda a evitar acessos não autorizados à rede, limitando o número de dispositivos
por porta e bloqueando ou desabilitando a porta se um dispositivo desconhecido
tentar se conectar..

_Diferença do Modo Clássico e Dinâmico_

>Classic Lock—All learned MAC addresses on the port are locked, and the port does not learn any new MAC addresses. The learned addresses are not subject to aging or re-learning.

>Dynamic Lock—The device learns MAC addresses up to the configured limit of allowed addresses. After the limit is reached, the device does not learn additional addresses. In this mode, the addresses are subject to aging and re-learning.

>Ações tomadas após violação: discard, snmp, log e shutdown

---

_Verifique quais são as configurações definidas nas interfaces_
~~~bash
show port-security interface gi1-24
~~~
<br>

_Entre no modo de configuração global_
~~~bash
configure terminal
~~~
<br>

_Selecione a(s) interface(s) que deseja configurar_
~~~bash

interface GigabitEthernet[nº interface]

~~~
<br>

_Configuração do Port Security no Modo Clássico ou Dinâmico_
~~~bash

switchport port-security mode [classic/dynamic] maximum [quantidade] action [ações a tomar] trap-freq [valor em segundos]

~~~
<br>

_Habilitar o Port-Security_
~~~bash

switchport port-security

~~~

>ATENÇÃO: tenha certeza de que o mac do equipamento não esteja cadastrado em outra interface do switch. Caso esteja, não vai funcionar enquanto não limpar da interface antiga.

---

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








