# mysql_sup
Comandos mysql
<hr>

### SELECT user, host FROM mysql.user;
Isso mostrará todos os usuários e os hosts permitidos para cada um.
Caso você receba um erro de permissão, pode ser necessário ter privilégios de administrador (root). Para garantir que você consiga rodar o comando, faça login como root:
### mysql -u root -p
Depois, rode o comando SELECT normalmente.
<hr>

Para verificar qual usuário está logado no momento no MySQL, use o seguinte comando:
### SELECT USER();
Ou, se quiser mais detalhes sobre a conexão, use:
### SELECT CURRENT_USER();
A diferença entre os dois:
USER() retorna o nome do usuário que fez login no MySQL.
CURRENT_USER() retorna o usuário que o MySQL está utilizando para permissões (pode ser diferente se o usuário tiver sido autenticado por um plugin).
<hr>
Criando um usuário:

Estando logado no console do MySQL, digite:
### CREATE USER ' '@'localhost' IDENTIFIED BY ' ';
E então dê privilégios de ação ao novo usuário:
### GRANT ALL PRIVILEGES ON *.* TO ' '@'localhost' WITH GRANT OPTION;
Por fim, recarregue as configurações de privilégios:
### FLUSH PRIVILEGES;
<hr>
