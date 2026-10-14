# BOOTCAMP-II

# Explorador de Países

## Autor
Tiago Ribeiro Van Der Broocke - Matrícula 22606645

## Descrição
Aplicação web para consultar dados de países, visualizar bandeiras e salvar uma lista de favoritos em um banco de dados.

## Tecnologias e APIs
- **Frontend:** HTML5, CSS3 e JavaScript (ES6 Modules)
- **API de Busca:** Open-Meteo Geocoding API e FlagCDN
- **Banco de Dados:** Supabase (PostgreSQL)
- **Container:** Docker (imagem Nginx Alpine)

## Funcionalidades
- **Consulta:** Busca dados do país (região, código, população) e exibe a bandeira oficial.
- **Adicionar favorito (Create):** Salva o país e sua região na tabela do Supabase.
- **Listar favoritos (Read):** Carrega os itens salvos do banco ao abrir a página.
- **Remover favorito (Delete):** Exclui o registro do banco de dados ao clicar em "Excluir".

## Como rodar via Docker
Para executar o container público da aplicação:

```bash
docker run -d -p 8080:80 TiagoRibas1/bootcamp2-app:1.0
