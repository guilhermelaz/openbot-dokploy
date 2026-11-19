# Gerador de template OpenBot para Dokploy

Página estática que gera o template do [OpenBot](https://openbot.run) pra instalar no [Dokploy](https://dokploy.com):

- **Base64 pra importar** no Dokploy (Advanced → Import → Configuration (Base64))
- `docker-compose.yml` adaptado pro Dokploy
- `seccomp.json` oficial do OpenBot (montado como File Mount)
- Comandos de login, status e atualização

Tudo roda no navegador. Nada é salvo nem enviado pra servidor nenhum.

**Acesse:** https://guilhermelaz.github.io/openbot-dokploy/

## Como usar

1. Abra a página e preencha o nome do servidor.
2. No Dokploy: projeto → Create Service → Compose → aba Advanced → Import → cole o Base64 → Load → Import.
3. Aba General → Deploy.
4. Open Terminal → container `openbot` → rode o comando de login da aba **Comandos**.
5. No app do OpenBot (mesma conta), selecione o servidor e conecte os providers de novo.

Não precisa de domínio: o OpenBot não publica porta web.

## Créditos e licença

Ferramenta não oficial. O `seccomp.json` e a imagem `ghcr.io/nightly-labs/openbot` são do OpenBot ([nightly-labs/openbot](https://github.com/nightly-labs/openbot)), sob a licença [PolyForm Noncommercial 1.0.0](https://github.com/nightly-labs/openbot/blob/main/LICENSE). Uso comercial do OpenBot exige licença própria deles.

Feito por [Guilherme Lazarotto](https://guilhermelaz.com.br).
