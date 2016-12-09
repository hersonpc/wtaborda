# Layout de integra��o WTaborda

> **Vers�o 1.0 - Dezembro 2016**

## Introdu��o

Manual de padroniza��o da converg�ncia sistemica de dados para o sistema WTaborda.

## Regras gerais

### Padroniza��o dos arquivos

O arquivo deve **obrigatoriamente**:

1. Ser gerado no padr�o CSV
2. Estar codificado utilizando o padr�o de caracteres ISO-8859-1
3. As colunas devem ser separadas por ";" (ponto-e-virgula)
4. Os campos de texto devem conter aspas duplas no in�cio e fim de cada dado

### Tipos de dados

| Tipo | Descri��o |
|-------|----------------------------|
| `Inteiro` | N�mero pertencente ao conjunto de n�meros inteiro |
| `Num�rico` | N�mero pertencente ao conjunto de n�meros reais |
| `Data` | Data padr�o brasileiro. Mascara: dd/mm/yyyy |
| `Texto` | Texto livre (*Obs: Obedecer o limite quando definido*) |

## Blocos de informa��o

### �ndice

* [Bloco 04 - Fluxo de caixa](#bloco-04---fluxo-de-caixa)
* [Bloco 16 - Aquisicao de bens duraveis](#bloco-16---aquisicao-de-bens-duraveis)
* [Bloco 19 - Contas a pagar no mes](#bloco-19---contas-a-pagar-no-mes)
* [Bloco 30 - Fluxo de caixa projetado](#bloco-30---fluxo-de-caixa-projetado)


### Bloco 04 - Fluxo de caixa

| #  | Campo | [Tipo](#tipos-de-dados) | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0000,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

### Bloco 16 - Aquisi��o de bens duraveis

| #  | Campo | [Tipo](#tipos-de-dados) | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

### Bloco 19 - Contas a pagar no m�s

| #  | Campo | [Tipo](#tipos-de-dados) | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave_item` | Inteiro | 5 | S | N | 00000 | zzz | |
| 04 | `item` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `chave_credor` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `credor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `chave_nf` | Texto | 100 | N | N | | **??????** | |
| 08 | `nf` | Texto | 200 | N | N | | **??????** | |
| 09 | `chave_aquisicao` | Texto | 80 | S | N | | xxx ||
| 10 | `aquisicao` | Texto | 200 | N | N | | **??????** | |
| 11 | `valor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 12 | `nr_parcela` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 13 | `valor_parcela` | Numerico | 8 +2 | S | N | 0,00 | xxx | |
| 14 | `saldo` | Numerico | 8 +2 | S | N | 0,00 | xxx | |
| 15 | `anexo` | Texto | 80 | S | N | | xxx | |

### Bloco 30 - Fluxo de caixa projetado

| #  | Campo | [Tipo](#tipos-de-dados) | Tamanho | Obrigatorio | Fixo | Mascara | Descricao                    | Observacao |
|----|-------|------|:---------:|:-----------:|:----:|:-------:|-------------------------------------------------|------------|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha: Fluxo de caixa | Informar: 04 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

