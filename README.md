# 💘 Disfarce.app — Plataforma de Relacionamentos com Moedas Virtuais

![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Mercado Pago](https://img.shields.io/badge/Mercado%20Pago-009EE3?style=for-the-badge&logo=mercadopago&logoColor=white)
![PIX](https://img.shields.io/badge/PIX-32BCAD?style=for-the-badge&logo=pix&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

> Aplicação web de relacionamentos no estilo Tinder, com economia interna baseada em moedas virtuais,
> pagamento instantâneo via PIX integrado à API do Mercado Pago e sistema completo de match e chat entre usuários.

🔗 **[Acessar aplicação](http://pachecotec.com.br/site/public_html/login.php)**

---

## 📌 Sobre o projeto

O Disfarce.app é uma plataforma de relacionamentos construída do zero em PHP puro,
com interface inspirada no Tinder e economia virtual própria baseada em moedas.
Os usuários compram moedas via PIX (integração real com API do Mercado Pago),
e utilizam essas moedas para interagir na plataforma — curtir perfis, desbloquear
conversas e enviar presentes virtuais.

Todo o sistema foi desenvolvido de forma autônoma, sem frameworks ou CMS externos,
cobrindo autenticação, match em tempo real, chat, upload de mídia e
processamento de pagamentos com confirmação assíncrona via webhook.

---

## 🚀 Funcionalidades

### Perfis e descoberta

- **Sistema de match estilo Tinder** — cards de perfil com ações de curtir (like) e
  rejeitar (dislike), animações de swipe e lógica de match mútuo
- **Upload de fotos de perfil** — envio e armazenamento de imagens com validação
  de tipo e tamanho no backend
- **Cadastro e autenticação** — registro de usuários, login seguro com hash bcrypt
  e controle de sessão com timeout automático

### Sistema de moedas

- **Economia virtual interna** — cada usuário possui um saldo de moedas vinculado
  à sua conta no banco de dados
- **Moedas para curtir perfis** — cada like consome moedas do saldo do usuário
- **Moedas para desbloquear conversas** — chat liberado mediante consumo de moedas
- **Moedas para enviar presentes** — gifting virtual entre usuários com débito automático

### Chat entre usuários

- **Mensagens em tempo real** — troca de mensagens entre matches com atualização
  via AJAX polling
- **Desbloqueio pago** — conversa liberada somente após consumo de moedas,
  incentivando recargas

### Pagamento via PIX

- **Compra de pacotes de moedas** — usuário escolhe um pacote (ex: 100, 500, 1000 moedas)
  e inicia o pagamento
- **Geração de QR Code PIX** — integração com API do Mercado Pago para criação
  de cobrança instantânea com QR Code e copia-e-cola
- **Confirmação assíncrona via webhook** — o Mercado Pago notifica o servidor
  ao confirmar o pagamento; o backend credita as moedas automaticamente na conta
  do usuário sem necessidade de ação manual
- **Histórico de transações** — registro de todas as recargas com status,
  valor e timestamp

---

## 💳 Fluxo de pagamento PIX
