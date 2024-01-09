# Aplicação de Envio de E-mails

Esta aplicação é responsável por enviar e-mails utilizando o RabbitMQ como intermediário para comunicação com outros serviços.

## Funcionalidades

- **Envio de E-mails:** Recebe mensagens do RabbitMQ para enviar e-mails aos destinatários.

## Requisitos

- PHP 8.x ou superior
- Composer
- RabbitMQ (com configurações adequadas)

Para esse projeto usamos o serviço da (CloudAMQP)[https://www.cloudamqp.com/] e da pacote (laravel-queue-rabbitmq)[https://github.com/vyuldashev/laravel-queue-rabbitmq]. Siga o processo de instalação e configuração de ambos.

## Instalação e Uso

1. Clone este repositório: `git clone https://github.com/seu-usuario/microservice-clientes.git`
2. Instale as dependências: `composer install`
3. Configure as variáveis de ambiente no arquivo `.env`, incluindo as credenciais do RabbitMQ.
4. Execute as migrações: `php artisan migrate`
5. Inicie o serviço: `php artisan serve`

Certifique-se de que o RabbitMQ está em execução e configurado corretamente para receber e processar as mensagens de envio de e-mails.

## Consumindo Mensagens

Use o comando 'php artisan queue:work' para consumir as mensagens.

## Funcionamento

Esta aplicação se conecta ao RabbitMQ para aguardar mensagens contendo informações sobre os e-mails a serem enviados. Quando uma mensagem é recebida, o e-mail correspondente é enviado aos destinatários especificados na mensagem.

## Autor

Gabriel Pereira - [GitHub](https://github.com/gabrielfpereira)
