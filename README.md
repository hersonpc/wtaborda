# Layout de exportacao WTaborda

> **Versão 1.0 - Dezembro 2016**

## Introducao

## Regras gerais

O arquivo deve **obrigatoriamente**:

1. Ser gerado na extensao CSV
2. Utilizar a codificacao ISO-8859-1
3. As colunas devem ser separadas por ";" (ponto-e-virgula)
4. Os campos de texto devem conter aspas no início e fim de cada dado

## Blocos de informacoes

### Bloco 04 - Fluxo de caixa

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | Sim | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | Sim | Não | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | Sim | Não | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | Sim | Não | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | Sim | Não | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | Não | N | | **??????** | |
| 08 | `historico` | Texto | 200 | Não | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | Sim | Não | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |


### Bloco 30 - Fluxo de caixa projetado

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | Sim | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | Sim | Não | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | Sim | Não | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | Sim | Não | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | Sim | Não | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | Não | N | | **??????** | |
| 08 | `historico` | Texto | 200 | Não | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | Sim | Não | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

### Bloco 19 - Contas a pagar no mes

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | Sim | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | Sim | Não | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave_item` | Inteiro | 5 | Sim | Não | 00000 | zzz | |
| 04 | `item` | Texto | 100 | Sim | Não | | Descricao da movimentacao | |
| 05 | `chave_credor` | Texto | 100 | Sim | Não | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `credor` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `chave_nf` | Texto | 100 | Não | N | | **??????** | |
| 08 | `nf` | Texto | 200 | Não | N | | **??????** | |
| 09 | `chave_aquisicao` | Texto | 80 | Sim | Não | | xxx ||
| 10 | `aquisicao` | Texto | 200 | Não | N | | **??????** | |
| 11 | `valor` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 12 | `nr_parcela` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 13 | `valor_parcela` | Numerico | 8 +2 | Sim | Não | 0,00 | xxx | |
| 14 | `saldo` | Numerico | 8 +2 | Sim | Não | 0,00 | xxx | |
| 15 | `anexo` | Texto | 80 | Sim | Não | | xxx | |

### Bloco 16 - Aquisicao de bens duraveis

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | Sim | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | Sim | Não | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | Sim | Não | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | Sim | Não | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | Sim | Não | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | Sim | Não | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | Não | N | | **??????** | |
| 08 | `historico` | Texto | 200 | Não | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | Sim | Não | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |







