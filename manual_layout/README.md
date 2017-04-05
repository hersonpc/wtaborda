# Layout de integração WTaborda

> **Nota Técnica 2016.001 - Versão 0.1.0 - Dezembro 2016**

## Introdução

Nesta nota técnica descrevemos o manual de padronização da convergência sistemica de dados para o sistema WTaborda. Para acompanhamento e controle das prestações de contas das Organizações Sociais de Saude (OSS) em parceiria com a Secretaria de Saúde do Estado.

## Regras gerais

### Padronização dos arquivos

O arquivo deve **obrigatoriamente**:

1. Ser gerado no padrão CSV
2. Estar codificado utilizando o padrão de caracteres ISO-8859-1
3. As colunas devem ser separadas por ";" (ponto-e-virgula)
4. Os campos de texto devem conter aspas duplas no início e fim de cada dado

### Tipos de dados

| Tipo | Descrição | Conceito | Observações |
|---|---|---|---|
| `Inteiro` | Número pertencente ao conjunto de números naturais | [Wikipédia](https://pt.wikipedia.org/wiki/N%C3%BAmero_inteiro) | |
| `Numérico` | Número pertencente ao conjunto de números racionais | [Wikipédia](https://pt.wikipedia.org/wiki/N%C3%BAmero_real) | |
| `Data` | Data no padrão brasileiro | [Wikipédia](https://pt.wikipedia.org/wiki/Data) | Mascara: dd/mm/yyyy |
| `Texto` | Texto alphanumérico | [Wikipédia](https://pt.wikipedia.org/wiki/Alfanum%C3%A9rico) | Obedecer o limite de quantidade de caracteres, quando definido |

## Blocos de informação

### <a name="index"/>Índice</a>

* [Bloco 04 - Fluxo de caixa](#bloco-04)
* [Bloco 16 - Aquisicao de bens duraveis](#bloco-16)
* [Bloco 17 - Remuneração dos membros da diretoria](#bloco-17)
* [Bloco 18 - Conciliação bancária](#bloco-18)
* [Bloco 19 - Contas a pagar no mes](#bloco-19)
* [Bloco 20 - Contrato de serviços terceirizados](#bloco-20)
* [Bloco 21 - Outros investimentos](#bloco-21)
* [Bloco 22 - Custo corporativo compartilhado](#bloco-22)
* [Bloco 29 - RH contrato no mês](#bloco-29)
* [Bloco 30 - Fluxo de caixa projetado](#bloco-30)
* [Bloco 31 - Pagamento RPA](#bloco-31)


### <a name="bloco-04"/>Bloco 04 - Fluxo de caixa</a>

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

[Voltar para índice](#index)

### <a name="bloco-16"/>Bloco 16 - Aquisição de bens duraveis</a>

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

[Voltar para índice](#index)

### <a name="bloco-17"/>Bloco 17 - Remuneração dos membros da diretoria</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 17 |

[Voltar para índice](#index)

### <a name="bloco-18"/>Bloco 18 - Conciliação bancária</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 18 |

[Voltar para índice](#index)

### <a name="bloco-19"/>Bloco 19 - Contas a pagar no mês</a>

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

[Voltar para índice](#index)

### <a name="bloco-20"/>Bloco 20 - Contrato de serviços terceirizados</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 20 |

[Voltar para índice](#index)

### <a name="bloco-21"/>Bloco 21 - Outros investimentos</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 21 |

[Voltar para índice](#index)

### <a name="bloco-22"/>Bloco 22 - Custo corporativo compartilhado</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 22 |

[Voltar para índice](#index)

### <a name="bloco-29"/>Bloco 29 - RH contrato no mês</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 29 |

[Voltar para índice](#index)

### <a name="bloco-30"/>Bloco 30 - Fluxo de caixa projetado</a>

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

[Voltar para índice](#index)

### <a name="bloco-31"/>Bloco 31 - Pagamento RPA</a>

| #  | Campo | Tipo | Tamanho | Obrigatorio | Fixo | Mascara | Descricao | Observacao |
|----|---|---|:---:|:---:|:---:|:---:|---|---|
| 01 | `codigo` | Inteiro | 3 | S | S | 000 | Descreve o tipo da planilha | Informar: 31 |


[Voltar para índice](#index)

