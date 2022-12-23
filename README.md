## Instalação

- Clonar ou baixar o repositório e jogar em uma pasta do seu Computador.  
- Em seguida abrir o projeto no terminal e rodar o **composer install**  
- Aguarde a finalização da instalação  

## Configuração
Criar o banco de dados com as tabelas no plural e as models no singular as configurações de Banco de Dados e URL estão no arquivo *src/Config.php*  


## Formas de acessar o projeto   

#### Virtual host   

A melhor forma de acessar o projeto é criando um virtual host:  

**Ubuntu**

- https://www.fredericomarinho.com/como-configurar-apache-virtual-hosts-no-ubuntu-20-04/  


**Windows**

- Cole as linhas abaixo em seu arquivo httpd-vhost no xampp, caminho: C:/xampp/apache/conf/extra/httpd-vhosts.conf.  
- configure conforme caminho do seu projeto

```
    <VirtualHost *:80>  
        ServerName www.meuprojeto.com.br    
        ServerAlias meuprojeto.com.br  
        DocumentRoot "caminho_para_o_projeto"  
    </VirtualHost>  
```

- Abra seu bloco de notas como administrador e abra o arquivo hosts na pasta C:/Windows/System32/drivers/etc/hostsgit cole a seguinte linha   

```
    127.0.0.1	www.meuprojeto.com.br
```

- depois basta reiniciar o seu xampp ou o seu computador

Obs.: 

Altere o ServerName para a url que deseja acessar em seu navegador, por exemplo www.mvc.local    
Altere o ServerAlias para a url que deseja acessar em seu navegador, sem o www. por exemplo: mvc.local    
alter o documentoRoot para o caminho exato onde se encontra o projeto que vc baixou, exemplo: C:\xampp\htdocs\mvc\public    
Importante que seu documentoRoot aponta para a pasta public, que é onde a aplicação é iniciada.  

Caso queira usar o servidor XAMPP:  

É importante configurar corretamente a constante *BASE_DIR*:
> const BASE_DIR = '/**PastaDoProjeto**/public';


## Modelo de MODEL
```php
<?php
namespace src\models;
use \core\Model;

class Usuario extends Model {

}
```