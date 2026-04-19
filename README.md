---
Bem-vindo ao repositório principal do **Ami**, o assistente virtual exclusivo do **Shopping do Sicredi**! 
Este projeto foi idealizado para apoiar a operação de Customer Experience (CX) do nosso marketplace, garantindo respostas rápidas, precisas e padronizadas para o time e para nossos associados.

## 🎯 O Problema e a Solução

**O Desafio:** Atualmente, lidamos com um grande volume de ligações e contatos repetitivos sobre as políticas de trocas e devoluções do nosso Marketplace.

**A Solução:** O Ami atua como uma primeira linha de atendimento inteligente. Ele é capaz de ler e interpretar nossa base de conhecimento para responder prontamente às dúvidas, impactando diretamente na redução da volumetria de atendimento humano e melhorando a experiência de jornada do usuário.

## 🤖 Conheça o Ami

O Ami não é apenas um chatbot genérico, ele possui uma persona desenhada para o contexto do Sicredi:
* **Personalidade:** Consultivo, Direto e Educativo.
* **Tom de Voz:** Informal, Técnico e Didático.
* **Segurança em 1º Lugar:** O agente opera sob regras estritas de *anti-alucinação*. Ele baseia suas respostas estritamente nos dados fornecidos, admite quando não tem a informação e é bloqueado para não compartilhar dados sensíveis.

## 🏗️ Arquitetura do Projeto

A arquitetura foi estruturada para manter a segurança das informações ao mesmo tempo em que oferece escalabilidade:

```mermaid
flowchart TD
    A[Associado / Equipe CX] -->|Mensagem| B[Interface Streamlit]
    B --> C[LLM GPT-4]
    C <--> D[Base de Conhecimento]
    C --> E[Validação Anti-Alucinação]
    E --> F[Resposta Segura]

## Estrutura do Repositório

```
📁 ami-shopper/
│
├── 📄 README.md                      # Documentação principal
│
├── 📁 data/                          # Dados para a base de conhecimento
│   └── base_shopping_sicredi.md      # Políticas de Troca e Devolução
│
├── 📁 docs/                          # Documentação detalhada do projeto
│   ├── 01-documentacao-agente.md     # Persona, uso e arquitetura
│   ├── 02-base-conhecimento.md       # Estratégia de dados
│   ├── 03-prompts.md                 # Engenharia de prompts e edge cases
│   ├── 04-metricas.md                # Cenários de teste e resultados
│   └── 05-pitch.md                   # Roteiro da apresentação do agente
│
├── 📁 src/                           # Código da aplicação funcional
│   ├── app.py                        # Interface no Streamlit
│   └── requirements.txt              # Dependências
│
└── 📁 assets/                        # Recursos visuais e roteiros
```



