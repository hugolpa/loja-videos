# Sistema de Compra de Vídeos com Envio Automático de Link

## Descrição

Este sistema permite que os usuários comprem vídeos e recebam automaticamente um link para o vídeo adquirido por email. Utiliza a API do PayPal para processar pagamentos e a API do Google Drive para armazenar e compartilhar vídeos. Emails são enviados aos compradores utilizando o nodemailer.

## Funcionalidades

1. **Processamento de Pagamento**:
   - Integração com a API do PayPal para executar pagamentos.
   - Validação de pagamento e captura de informações do comprador.

2. **Autorização e Acesso ao Google Drive**:
   - Uso de OAuth2 para autorizar e acessar o Google Drive.
   - Concessão de permissões de leitura ao comprador para o vídeo adquirido.

3. **Envio de Email**:
   - Geração de link de visualização do vídeo no Google Drive.
   - Envio de email ao comprador com o link do vídeo utilizando nodemailer.

## Configuração

### Requisitos

- Node.js
- Conta no Google Cloud para configurar OAuth2
- Conta no PayPal para processar pagamentos

### Passos para Configurar

1. **Clone o Repositório**:
    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    cd seu-repositorio
    ```

2. **Instale as Dependências**:
    ```bash
    npm install
    ```

3. **Configuração do Google Cloud e OAuth2**:
   - Crie um projeto no [Google Cloud Console](https://console.cloud.google.com/).
   - Habilite a API do Google Drive.
   - Crie credenciais OAuth2 e baixe o arquivo JSON.

4. **Configuração do nodemailer**:
   - Ative o acesso para aplicativos menos seguros em sua conta do Gmail, ou configure OAuth2 conforme as instruções acima.

5. **Variáveis de Ambiente**:
   - Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis:

    ```plaintext
    EMAIL_USER=seu_email@gmail.com
    EMAIL_PASS=sua_senha  # Se estiver usando OAuth2, ignore esta variável
    CLIENT_ID=seu_client_id
    CLIENT_SECRET=seu_client_secret
    REDIRECT_URI=seu_redirect_uri
    REFRESH_TOKEN=seu_refresh_token
    ```

6. **Executar o Sistema**:
    ```bash
    node app.js
    ```

## Exemplo de Uso

Quando um usuário realiza uma compra, o sistema:
1. Processa o pagamento via PayPal.
2. Autoriza o acesso ao Google Drive e concede permissão de leitura para o comprador.
3. Envia um email ao comprador com o link para o vídeo adquirido.

## Contato

Para dúvidas ou sugestões, entre em contato pelo email: [hugo.leonardo.jobs@gmail.com](mailto:hugo.leonardo.jobs@gmail.com).

