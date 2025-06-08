# FurioN

Este repositório contém o backend em FastAPI e as páginas estáticas do CED Brasília.

## Repositórios relacionados

- [SITE-DA-ESCOLA](https://github.com/CEDBRASIL/SITE-DA-ESCOLA) — front-end do site
- [SISTEMA-GERAL](https://github.com/CEDBRASIL/SISTEMA-GERAL) — back-end principal

O site está disponível em [https://www.cedbrasilia.com.br](https://www.cedbrasilia.com.br) e a API em [https://api.cedbrasilia.com.br](https://api.cedbrasilia.com.br).

## Deploy no Render

O Render pode construir e publicar tanto a API quanto o site utilizando o arquivo `render.yaml` incluído neste projeto.

### Passos

1. Faça um fork deste repositório em sua conta do GitHub.
2. Acesse [Render](https://render.com) e escolha **New Blueprint**.
3. Informe a URL do seu repositório. O Render lerá o `render.yaml` e criará dois serviços:
   - **ced-api**: serviço web Python executando `uvicorn main:app`.
   - **ced-site**: site estático que serve os arquivos HTML deste repositório.
4. No painel do Render, configure as variáveis de ambiente necessárias para a API (`BASIC_B64`, `UNIDADE_ID`, `OM_BASE`, `CHATPRO_TOKEN`, etc.).
5. Realize o deploy. Após a publicação, associe seus domínios personalizados (`https://api.cedbrasilia.com.br` e `https://www.cedbrasilia.com.br`).

Para mais detalhes consulte a [documentação do Render](https://render.com/docs/infrastructure-as-code).
