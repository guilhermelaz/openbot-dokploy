# Gerador de template OpenBot para Dokploy e EasyPanel

Página estática que gera o template do [OpenBot](https://openbot.run) pra instalar no [Dokploy](https://dokploy.com) ou no [EasyPanel](https://easypanel.io). No topo da página tem um seletor (Dokploy vem marcado por padrão).

**Dokploy:**

- **Base64 pra importar** no Dokploy (Advanced → Import → Configuration (Base64))
- `docker-compose.yml` adaptado pro Dokploy
- `seccomp.json` oficial do OpenBot (montado como File Mount)
- Comandos de login, status e atualização

Tudo roda no navegador. Nada é salvo nem enviado pra servidor nenhum.

**Acesse:** https://guilhermelaz.github.io/openbot-dokploy/

**EasyPanel:** serviço Compose com fonte Git apontando pra pasta [`/easypanel`](easypanel) deste repositório, mais as variáveis do Environment. Link direto: https://guilhermelaz.github.io/openbot-dokploy/?painel=easypanel

## Como usar (Dokploy)

1. Abra a página e preencha o nome do servidor.
2. No Dokploy: projeto → Create Service → Compose → aba Advanced → Import → cole o Base64 → Load → Import.
3. Aba General → Deploy.
4. Open Terminal → container `openbot` → rode o comando de login da aba **Comandos**.
5. No app do OpenBot (mesma conta), selecione o servidor e conecte os providers de novo.

Não precisa de domínio: o OpenBot não publica porta web.

## Como usar (EasyPanel)

Veja [easypanel/README.md](easypanel/README.md).

## Créditos e licença

Ferramenta não oficial. O `seccomp.json` (também copiado em `easypanel/`) e a imagem `ghcr.io/nightly-labs/openbot` são do OpenBot ([nightly-labs/openbot](https://github.com/nightly-labs/openbot)), sob a licença [PolyForm Noncommercial 1.0.0](https://github.com/nightly-labs/openbot/blob/main/LICENSE). Uso comercial do OpenBot exige licença própria deles.

Feito por [Guilherme Lazarotto](https://guilhermelaz.com.br).
