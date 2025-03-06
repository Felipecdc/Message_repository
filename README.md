# 📩 Nodemailer Notification Service

Este repositório contém uma biblioteca para envio de **e-mails de notificação** usando **Nodemailer**. O objetivo é enviar notificações automáticas, como atualizações de pedidos, diretamente para os clientes de uma aplicação.

## 🚀 Funcionalidades

Atualmente, o projeto oferece a seguinte funcionalidade:

### ✉️ **Envio de E-mails de Notificação**

- 📦 **Notificação de Pedido** → `sendNotificationEmail.ts`

### 🛠 **Testes**

- ✅ **Teste de Envio de E-mail** → `sendNotificationEmail.test.ts`

## 🛠 Tecnologias Utilizadas

- **Node.js** → Para o desenvolvimento do backend.
- **TypeScript** → Para segurança e robustez na codificação.
- **Nodemailer** → Para envio de e-mails.
- **dotenv** → Para armazenar variáveis de ambiente de forma segura.
- **Jest** → Para testes automatizados.

## 📑 Como Usar

### 1️⃣ **Configuração Inicial**

1. Clone este repositório:

   ```sh
   git clone https://github.com/seuusuario/nodemailer-notification-service.git
   ```

2. Instale as dependências:

   ```sh
   npm install
   ```

3. Configure as variáveis de ambiente no arquivo `.env`:

   ```env
   SMTP_HOST=smtp.gmail.com
   SMTP_PORT=587
   EMAIL_USER=seu_email@gmail.com
   EMAIL_PASS=sua_senha_de_app
   ```

   **Observação:** É necessário gerar uma senha de app no Gmail para que o serviço funcione corretamente.

### 2️⃣ **Enviando um E-mail de Notificação**

Exemplo de envio de notificação de pedido:

```ts
import { sendNotificationEmail } from "./nodemailer/sendNotificationEmail";

sendNotificationEmail({
  email: "cliente@example.com",
  orderId: "12345",
  trackingUrl: "https://example.com/track/12345",
  trackingCode: "AF123456789",
});
```

### 3️⃣ **Rodando os Testes**

```sh
npm test
```

## 📸 Exemplo de Resposta

### ✅ **Envio de E-mail Bem-Sucedido**

```json
{
  "success": true,
  "message": "E-mail enviado com sucesso.",
  "to": "cliente@example.com"
}
```

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
