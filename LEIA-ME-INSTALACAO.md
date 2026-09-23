# Instalação — Welisson Barber

Este pacote já está pronto. Falta só ligar ao banco de dados (Firebase) e publicar.

## 1. Firebase (banco de dados)

1. https://console.firebase.google.com → **Adicionar projeto** (nome livre).
2. **Firestore Database** → *Criar banco de dados* → modo **produção** → região `southamerica-east1` (São Paulo).
3. **Authentication** → *Sign-in method* → ative **E-mail/senha**. Em **Users** → *Adicionar usuário*:
   - E-mail: `admin@welissonbarber.com`
   - Senha: a que o dono vai usar para entrar no painel.
4. **Configurações do projeto** → *Seus apps* → ícone **</>** (Web) → registre o app (os dados já estão no `config.js`).
5. **Firestore Database → Regras** → apague o que estiver lá, cole o conteúdo do arquivo `firestore.rules` deste pacote e clique em **Publicar**.
   (Essas regras só deixam o e-mail `admin@welissonbarber.com` administrar o sistema.)
6. **Authentication → Settings → User actions**: desmarque **Enable create (sign-up)**.

## 2. Publicar o site
Suba **todos os arquivos desta pasta** em uma hospedagem estática:
- **Netlify** (mais simples): app.netlify.com/drop → arraste a pasta.
- **GitHub Pages** ou **Firebase Hosting**, se preferir.

Depois, no Firebase: **Authentication → Settings → Domínios autorizados** → adicione o endereço do site.

- Site dos clientes: `https://SEU-ENDERECO/`
- Painel do dono: `https://SEU-ENDERECO/admin.html` (senha do passo 1.3)

## 3. Primeiro uso (painel → aba **Ajustes** e **Horários**)
1. **Ajustes**: confira nome, WhatsApp, logo, letra do nome no topo, cores (dá para pedir uma sugestão de cores a partir da logo), planos, valores e tempo de cada serviço.
2. **Horários**: dias e horários de atendimento (e almoço).
3. **Datas Especiais**: feriados.
4. Faça um agendamento de teste no site e use **Zerar receitas** no painel para limpar os testes.

## Dados desta instalação
- Barbearia: Welisson Barber
- WhatsApp: 5585982358729
- Serviços: Corte Degradê (R$30), Corte tesoura (R$30), Corte Social (R$20), Barba (R$45), Sobrancelha (R$10), Corte + Barba (R$45), Corte + Barba + Sobrancelha (R$50), Luzes (R$60), Luzes + Corte (R$80), Platinado (R$80), Platinado + Corte (R$110)
- Planos: Barba (R$50), Simples (R$50), Intermediário (R$90), Sênior (R$130), Plano Neto (R$0)
