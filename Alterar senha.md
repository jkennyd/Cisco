# Alteração de Senha

## Objetivo
Alterar senha de acesso dos usuários.

---

_Entre no modo de configuração global_
~~~bash
configure terminal
~~~
<br>

_Selecione o usuário, criptografia e coloque a nova senha_
~~~bash
username 'NomeDoUsuario' algorithm-type (SHA256) secret 'NovaSenha'
~~~
<br>

_Coloque a senha antiga para confirmar a troca_
~~~bash
Exemplo:
Cisco(conf t): Old password
~~~
<br>

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








