# OpenBot no EasyPanel

Pasta usada como **Build Path** (`/easypanel`) num serviço **Compose** do EasyPanel com fonte **Git**.

Gere as variáveis e o passo a passo em: https://guilhermelaz.github.io/openbot-dokploy/?painel=easypanel

| Campo no EasyPanel | Valor |
|---|---|
| Repository URL | `https://github.com/guilhermelaz/openbot-dokploy` |
| Branch | `main` |
| Build Path | `/easypanel` |
| Docker Compose File | `docker-compose.yml` |

Variáveis (aba Environment, com **Create .env file** ligado):

```
OPENBOT_TAG=latest
OPENBOT_SHM=1g
OPENBOT_MEM_LIMIT=0
OPENBOT_TZ=America/Sao_Paulo
```

`OPENBOT_MEM_LIMIT=0` = sem limite de RAM.

## Licença do seccomp.json

O `seccomp.json` é uma cópia do arquivo oficial do OpenBot ([nightly-labs/openbot](https://github.com/nightly-labs/openbot/blob/main/docker/seccomp.json)), distribuído sob a licença [PolyForm Noncommercial 1.0.0](https://github.com/nightly-labs/openbot/blob/main/LICENSE).
