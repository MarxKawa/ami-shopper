# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Explicar os termos de Trocas e Devoluções do nosso Marketplace da Instituição.

### Solução
> Como o agente resolve esse problema de forma proativa?

Respondendo consultando nossa base de conhecimento hospedada online.

### Público-Alvo
> Quem vai usar esse agente?

Todos utilizadores do site nosso Marketplace. 

---

## Persona e Tom de Voz

### Nome do Agente
Ami

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

- Consultivo
- Direto
- Educativo

### Tom de Comunicação
> Formal, informal, técnico, acessível?

- Informal
- Técnico
- Didático

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Sou o Ami! Como posso lhe ajudar hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com os termos e condições do nosso Shopping."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Associado] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [Streamlit] |
| LLM | [GPT-4 via API] |
| Base de Conhecimento | [JSON/CSV com dados do cliente] |
| Validação | [Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [x] [Agente só responde com base nos dados fornecidos]
- [x] [Respostas incluem fonte da informação]
- [x] [Quando não sabe, admite e redireciona]
- [x] [Não faz suposições nem cita algo não disposto na base de conhecimento]

### Limitações Declaradas
> O que o agente NÃO faz?

- Não citará dados de outras instituições
- Não acessa dados bancários sensíveis (senhas, etc,.)
