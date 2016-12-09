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

| Tipo | Descri��o | Conceito | Observa��es |
|---|---|---|---|
| `Inteiro` | N�mero pertencente ao conjunto de n�meros naturais | [Wikip�dia](https://pt.wikipedia.org/wiki/N%C3%BAmero_inteiro) | |
| `Num�rico` | N�mero pertencente ao conjunto de n�meros racionais | [Wikip�dia](https://pt.wikipedia.org/wiki/N%C3%BAmero_real) | |
| `Data` | Data no padr�o brasileiro | [Wikip�dia](https://pt.wikipedia.org/wiki/Data) | Mascara: dd/mm/yyyy |
| `Texto` | Texto alphanum�rico | [Wikip�dia](https://pt.wikipedia.org/wiki/Alfanum%C3%A9rico) | Obs: Obedecer o limite quando definido |

## Blocos de informa��o

### �ndice

* [Bloco 04 - Fluxo de caixa](#bloco-04)
* [Bloco 16 - Aquisicao de bens duraveis](#bloco-16)
* [Bloco 17 - Remunera��o dos membros da diretoria](#bloco-17)
* [Bloco 18 - Concilia��o banc�ria](#bloco-18)
* [Bloco 19 - Contas a pagar no mes](#bloco-19)
* [Bloco 20 - Contrato de servi�os terceirizados](#bloco-20)
* [Bloco 21 - Outros investimentos](#bloco-21)
* [Bloco 22 - Custo corporativo compartilhado](#bloco-22)
* [Bloco 29 - RH contrato no m�s](#bloco-29)
* [Bloco 30 - Fluxo de caixa projetado](#bloco-30)
* [Bloco 31 - Pagamento RPA](#bloco-31)


### Fluxo de caixa
#### Bloco 04

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 04 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0000,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

[Voltar para indice](#indice)

### Aquisi��o de bens duraveis
#### Bloco 16

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 16 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

[Voltar para indice](#indice)

### Remunera��o dos membros da diretoria
#### Bloco 17

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 17 |

### Bloco 18 - Concilia��o banc�ria

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 18 |

[Voltar para indice](#indice)

### Contas a pagar no m�s
#### Bloco 19

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
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

[Voltar para indice](#indice)

### Contrato de servi�os terceirizados
#### Bloco 20

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 20 |

[Voltar para indice](#indice)

### Outros investimentos
#### Bloco 21

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 21 |

[Voltar para indice](#indice)

### Custo corporativo compartilhado
#### Bloco 22

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 22 |

[Voltar para indice](#indice)

### RH contrato no m�s
#### Bloco 29

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 29 |

[Voltar para indice](#indice)

### Fluxo de caixa projetado
#### Bloco 30

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 30 |
| 02 | `movimento` | Texto | 7 | S | N | mm/yyyy | Mes/Ano em que ocorreu a movimentacao | |
| 03 | `chave` | Inteiro | 5 | S | N | 00000 | Usar codigo referente ao movimento | Ver [plano de contas](plano_de_contas.md) |
| 04 | `descricao` | Texto | 100 | S | N | | Descricao da movimentacao | |
| 05 | `data` | Texto | 100 | S | N | dd/mm/yyyy | Data da movimentacao (data pagamento) | |
| 06 | `valor` | Numerico | 8 +2 | S | N | 0,00 | Data da movimentacao (data pagamento) | |
| 07 | `texto` | Texto | 100 | N | N | | **??????** | |
| 08 | `historico` | Texto | 200 | N | N | | **??????** | |
| 09 | `anexo` | Texto | 80 | S | N | | Descricao do nome do anexo que apresenta a comprovacao da movimentacao financeira | |

[Voltar para indice](#indice)

### Pagamento RPA
#### Bloco 31

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 31 |


[Voltar para indice](#indice)

