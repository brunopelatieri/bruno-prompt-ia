## 👽 :21/06/2026

Sim — você precisa **cadastrar no Portainer**, na própria stack.

O `${POSTGRES_USER}`, `${POSTGRES_PASSWORD}` e `${POSTGRES_DB}` no YAML são **placeholders**. O Portainer substitui pelos valores que você define ao criar ou editar a stack.

## Onde cadastrar

**Portainer → Stacks → `bizu-hub` → Editor** (ou ao criar a stack)

Role até **Environment variables** (ou **Env**) e adicione:

| Nome | Valor (exemplo) |
|------|------------------|
| `POSTGRES_USER` | `bizu_hub` |
| `POSTGRES_PASSWORD` | `BrunoIME14198303MaiTe` |
| `POSTGRES_DB` | `bizu_hub` |
| `DOCKER_IMAGE` | `registry.gitlab.com/brunopelatieri/bizu-hub` |
| `DOCKER_TAG` | `latest` |

Depois: **Update the stack** / **Deploy**.

---

## O que acontece

1. Portainer injeta os valores no YAML
2. O container Postgres sobe com user/senha/db definidos
3. O serviço `app` monta o `DATABASE_URL` com as **mesmas** variáveis:

```yaml
DATABASE_URL: postgresql://${POSTGRES_USER}:${POSTGRES_PASSWORD}@postgres:5432/${POSTGRES_DB}
```

Não precisa cadastrar em outro lugar (GitLab, `.env` do app, etc.) — **só na stack do Portainer**.

---

## Dica

- Use a mesma senha que você anotar para rodar migrations depois
- Não commite a senha no Git — só no Portainer
- Se mudar `POSTGRES_PASSWORD` **depois** do primeiro deploy, o Postgres **não** troca a senha sozinho (volume já inicializado). Aí é alterar no banco ou recriar o volume

Quer um exemplo pronto para colar no editor de variáveis do Portainer?