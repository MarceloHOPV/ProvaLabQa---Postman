# ProvaLabQa---Postman
Repositório para armazenar os testes postman da Prova de QA

# Prova - Teste de API com Postman

## Descrição do Projeto
Este projeto foi desenvolvido como parte da prova da disciplina **S206 - Qualidade de Software**. Ele utiliza o Postman para testar a **The Cat API** com dois cenários diferentes de teste. Um teste positivo e um teste negativo foram implementados, seguindo as especificações fornecidas.

## Estrutura do Projeto
- **Teste Positivo**: 
  - Endpoint: `GET /v1/images/search`
  - Descrição: Recupera uma lista de imagens de gatos, validando o parâmetro `limit`.
  - Status esperado: **200**.
  - Validação: O corpo da resposta deve conter um array com no máximo 5 itens.

- **Teste Negativo**:
  - Endpoint: `POST /v1/favourites`
  - Descrição: Tenta favoritar uma imagem com uma chave de API (`x-api-key`) inválida.
  - Status esperado: **401**.
  - Validação: A resposta deve conter a mensagem de erro "AUTHENTICATION_ERROR".

## Requisitos
- Ferramentas utilizadas:
  - **Postman**
  - **Newman** (para exportar o relatório de testes)
- A API utilizada requer uma chave de autenticação (API Key).

## Como Executar os Testes
1. **Configuração do Ambiente**:
   - Baixe o [Postman](https://www.postman.com/downloads/).
   - Obtenha uma API Key válida em [The Cat API](https://thecatapi.com/).

2. **Importar Coleção no Postman**:
   - Faça o download do arquivo de coleção.
   - Importe a coleção no Postman.

3. **Executar os Testes**:
   - Abra a coleção importada no Postman.
   - Configure os headers e parâmetros como descrito acima.
   - Execute cada requisição para verificar os resultados.

4. **Exportar Relatório com Newman**:
   - Instale o Newman: `npm install -g newman`
   - Execute o comando:
     ```bash
     newman run <arquivo_da_colecao>.json -r html --reporter-html-export <nome_do_relatorio>.html
     ```

## Relatório de Testes
Os resultados dos testes foram exportados em formato HTML usando o **Newman** e podem ser encontrados no repositório deste projeto.

## Observações
- Não foi utilizado um ambiente (`environment`) no Postman, conforme solicitado no enunciado.
- Todos os testes foram validados manualmente antes de exportar os relatórios.

---

**Professor**: Christopher Lima

**Disciplina**: S206 - Qualidade de Software
