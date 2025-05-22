## Atividade

# Atividade 3: Detalhando a Arquitetura Cliente-Servidor na Web

## Introdução

A arquitetura cliente-servidor é um modelo fundamental da comunicação na web. Quando acessamos uma página na internet, o navegador (cliente) faz uma solicitação a um servidor, que processa essa solicitação e envia de volta os dados necessários, como páginas HTML, arquivos CSS, JavaScript e imagens.

---

## Papel do Cliente

O **cliente** é, geralmente, o navegador web utilizado pelo usuário (ex: Chrome, Firefox, Safari). Seu papel é:

- Solicitar recursos da web (como páginas, imagens ou dados)
- Interpretar e renderizar o conteúdo recebido (HTML, CSS, JS)
- Interagir com o usuário

Exemplos de clientes: navegadores, aplicativos móveis, ou qualquer software que se comunique com um servidor via rede.

---

## Papel do Servidor

O **servidor** é um sistema remoto que armazena e fornece os recursos da web. Ele é responsável por:

- Receber e processar requisições dos clientes
- Buscar e preparar os dados solicitados (às vezes consultando bancos de dados)
- Enviar uma resposta apropriada de volta ao cliente

Exemplos de servidores: Apache, Nginx, Node.js com Express, etc.

---

## Fluxo de Comunicação: Do Cliente ao Servidor

Abaixo está o fluxo básico da comunicação web:

### 1. O usuário digita uma URL no navegador

Exemplo: `https://www.exemplo.com/index.html`

### 2. Resolução de Nome com DNS

O navegador precisa saber o **endereço IP** do servidor que hospeda o site. Ele consulta o **DNS (Domain Name System)** para converter o nome de domínio (`www.exemplo.com`) em um endereço IP, como `192.168.0.1`.


### 3. Processamento da Requisição pelo Servidor

O servidor interpreta a requisição, localiza o arquivo solicitado (ex: `index.html`) ou gera dinamicamente o conteúdo, e então prepara uma **resposta HTTP**.

### 4. Resposta HTTP do Servidor

O servidor envia uma resposta contendo:

- Um **código de status HTTP** (ex: 200 OK, 404 Not Found)
- Cabeçalhos HTTP
- O corpo da resposta (ex: HTML da página)

Exemplo de resposta:

HTTP/1.1 200 OK
Content-Type: text/html

```html

<!DOCTYPE html> <html> <head><title>Exemplo</title></head> <body>Olá, mundo!</body> </html> ```

````

*6. Renderização da Página pelo Navegador*

O navegador interpreta o conteúdo recebido, carrega os arquivos adicionais (CSS, JS, imagens), e exibe a página ao usuário.

*Conceitos Importantes*

**Requisição HTTP**

Uma requisição HTTP é enviada do cliente ao servidor e contém:

Método (GET, POST, PUT, DELETE, etc.)

Caminho do recurso

Cabeçalhos (headers)

Corpo (opcional, geralmente em métodos como POST)

**Resposta HTTP**

A resposta HTTP enviada pelo servidor contém:

Código de status (ex: 200, 404, 500)

Cabeçalhos de resposta

Corpo da resposta (HTML, JSON, etc.)

**DNS (Domain Name System)**

O DNS é como uma "agenda telefônica" da internet. Ele traduz nomes de domínio legíveis por humanos (como google.com) para endereços IP que os computadores entendem.

FONTES:

https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview

https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/First_steps/Client-Server_overview

https://www.cloudflare.com/learning/dns/what-is-dns/
