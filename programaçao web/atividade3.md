

---

## 🧩 Visão Geral: Cliente e Servidor

### 🔹 Cliente (navegador)

O **cliente** é o navegador web (como Chrome, Firefox, Edge), que envia solicitações para um servidor para obter páginas web e outros recursos (imagens, scripts, etc.). Ele é responsável por:

* Interpretar e renderizar o HTML recebido.
* Apresentar a interface para o usuário.
* Iniciar a comunicação com o servidor.

### 🔹 Servidor

O **servidor web** é um computador (ou um conjunto deles) configurado para responder a solicitações HTTP. Ele:

* Recebe requisições do cliente.
* Processa os pedidos (estáticos ou dinâmicos).
* Envia respostas com o conteúdo solicitado (como arquivos HTML, JSON, imagens, etc.).

---

## 🔄 Fluxo de Eventos: Da Solicitação ao Recebimento

### 1. 🧭 Digitação do endereço (URL)

O usuário digita uma URL no navegador, como `https://www.exemplo.com`.

### 2. 🌐 Resolução de DNS

Antes de conectar ao servidor, o navegador precisa saber o endereço IP de `www.exemplo.com`. Para isso, usa o **DNS**:

* O navegador consulta o **resolver DNS** configurado (geralmente do provedor ou sistema operacional).
* O DNS retorna o **endereço IP** associado ao domínio (`93.184.216.34`, por exemplo).
* Agora o navegador sabe para onde enviar a solicitação.

### 3. 🔗 Estabelecimento de conexão (TCP/TLS)

* O navegador abre uma conexão **TCP** com o IP do servidor na **porta 80 (HTTP)** ou **443 (HTTPS)**.
* Se for HTTPS, ocorre uma **negociação TLS (SSL)** para criptografar a comunicação.

### 4. 📤 Envio da Requisição HTTP (HTTP Request)

O navegador envia uma **requisição HTTP**. Exemplo:

```http
GET /index.html HTTP/1.1
Host: www.exemplo.com
User-Agent: Mozilla/5.0
Accept: text/html
```

Explicação:

* `GET`: método HTTP (solicita um recurso).
* `/index.html`: caminho do recurso solicitado.
* `Host`: informa o domínio.
* `User-Agent`: identifica o navegador.

### 5. 📥 Processamento no Servidor

* O servidor recebe a requisição.
* Pode ler arquivos do disco ou gerar conteúdo dinâmico (ex: via PHP, Python, Node.js).
* Monta uma **resposta HTTP** com os dados solicitados.

### 6. 📦 Envio da Resposta HTTP (HTTP Response)

Exemplo de resposta:

```http
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1256

<html>
  <head><title>Exemplo</title></head>
  <body>Bem-vindo!</body>
</html>
```

Explicação:

* `200 OK`: código de status HTTP (requisição bem-sucedida).
* `Content-Type`: tipo do conteúdo (`text/html`, `image/png`, etc.).
* Corpo da resposta: o conteúdo da página web.

### 7. 🖼️ Renderização da Página pelo Navegador

* O navegador interpreta o HTML.
* Faz novas requisições (paralelas) para imagens, CSS, JS, etc.
* Executa scripts e renderiza a página final para o usuário.

---

## 🛠️ Conceitos Técnicos Envolvidos

### 🔸 HTTP (HyperText Transfer Protocol)

* Protocolo de comunicação entre cliente e servidor.
* Baseado em requisições e respostas.
* Usa métodos como `GET`, `POST`, `PUT`, `DELETE`.

### 🔸 DNS (Domain Name System)

* Sistema de nomes que traduz **nomes de domínio** (ex: `google.com`) para **endereços IP**.
* Atua como uma "agenda telefônica" da internet.

### 🔸 HTTPS (HTTP Secure)

* Versão segura do HTTP.
* Usa **TLS/SSL** para criptografar os dados entre cliente e servidor.

---

## 📘 Fontes

1. Mozilla Developer Network (MDN Web Docs)
   [https://developer.mozilla.org/pt-BR/docs/Web/HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP)
2. W3Schools - HTTP Tutorial
   [https://www.w3schools.com/tags/ref\_httpmethods.asp](https://www.w3schools.com/tags/ref_httpmethods.asp)
3. Cloudflare - O que é DNS
   [https://www.cloudflare.com/pt-br/learning/dns/what-is-dns/](https://www.cloudflare.com/pt-br/learning/dns/what-is-dns/)
4. How Browsers Work - Tali Garsiel
   [https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)

---
