# Integração JSON

Material de apoio para a documentação do processo de integração com o sistema WTaborda via envio de documentos online no formato [JSON](https://pt.wikipedia.org/wiki/JSON).

## Diagrama de sequencia

![Diagrama de sequencia](./conteudo/v0/uml/diagrama_sequencia.png)

## Estrutura dos arquivos JSON

Nesta sessão descrevemos o modelo de estrutua dos arquivos.

### Transação 4

* JSON: [wtaborda_transasao_4.json](./conteudo/v0/wtaborda_transasao_4.json)  
* PDF: [wtaborda_transasao_4_exemplo.pdf](./conteudo/v0/wtaborda_transasao_4_exemplo.pdf)  

![Manual modelo](./conteudo/v0/wtaborda_transasao_4_manual.png)  


### REST Rotas

Método | Rota | Descrição
-----|-----|-----
**POST** | /lancamento | Envio do lote de transação.
**GET** | /lotes | Consulta relação os lotes 
**GET** | /lote/*{id}* | Consulta o detalhamento do lote *(recupera o status do processamento do lote bem como o histórico de erros identificados)*
**DELETE** | /lote/*{id}* | Solicita o estorno do lote

