# BOOTCAMP-II

# Explorador de Países

## Autor
Tiago Ribeiro Van Der Broocke - Matrícula 22606645

Aplicação web interativa para busca de informações de países e localidades consumindo a API Open-Meteo, com funcionalidade de adição/remoção de favoritos e ordenação de dados.



##  Links do projeto

1. **Repositório GitHub:** https://github.com/TiagoRibas1/bootcamp2-app
2. **Aplicação no GitHub Pages:** https://tiagoribas1.github.io/bootcamp2-app/
3. **Repositório no Docker Hub:** https://hub.docker.com/r/tiagoribas/bootcamp2-app



##  Executar container

Para rodar a aplicação localmente via Docker, execute o comando abaixo no terminal:

```bash
docker run -d -p 8080:80 tiagoribas/bootcamp2-app:latest

```

## Persistência de Dados

- **Banco de Dados:** Supabase (PostgreSQL)
- **Tabela:** `favoritos`
- **Campos:** `id` (PK), `nome`, `latitude`, `longitude`, `codigo_pais` (para carregar a bandeira via FlagCDN) e `criado_em` (timestamp).

---

## Sidequests

### SQ1 · `.dockerignore`
Criado para ignorar `.git`, `README.md` e arquivos locais no build, reduzindo o tamanho da imagem e acelerando o processo.

### SQ2 · Tags no Docker Hub
- `1.0`: Primeira versão funcional.
- `1.1`: Versão com melhorias.
- `latest`: Última versão estável.

### SQ3 · Descrição no Docker Hub
Overview do repositório atualizado com a explicação do projeto, comando `docker run` e link do GitHub.

### SQ4 · Orquestração e Kubernetes

**Evidência dos 2 containers rodando (`docker ps`):**
![Print SQ4](print_sq4.png)

**Como gerenciar 100 containers?**
Usaria **Kubernetes**. As máquinas formam um **Cluster**, os containers rodam em **Pods** e as **Réplicas** mantêm o número de instâncias rodando automaticamente, garantindo escala e alta disponibilidade sem gestão manual.
