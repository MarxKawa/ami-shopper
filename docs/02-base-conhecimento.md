# Base de Conhecimento

## Dados Utilizados

Arquivo da pasta `data`, por exemplo:

| Arquivo | Formato | Para que serve no Ami? |
|---------|---------|---------------------|
| `base_shopping_sicredi.md` | MD | Contextualizar sobre as regras e políticas de Trocas e Devoluções |


---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Inserido o arquivo com as políticas e regras do setor de Trocas e Devoluções do site Shopping do Sicredi. 

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

O arquivo é carregado no início da sessão e os dados incluídos no contexto do prompt.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

São consultados dinamicamente no arquivo.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Prazo para Trocas e Devoluções:
- O prazo para trocas e devoluções de produtos é de até 7 (sete) dias corridos, a contar da data de entrega, conforme previsto no CDC (Código de Defesa do Consumidor).
```
