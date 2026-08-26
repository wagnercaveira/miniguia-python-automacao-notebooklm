# 🧠 Engenharia de Prompts e Cicatrizes

## 1. Objetivo

Durante o desenvolvimento deste projeto foram realizados testes progressivos de prompts no NotebookLM.

O objetivo foi observar como diferentes formas de formular uma pergunta poderiam alterar a qualidade, profundidade e utilidade das respostas produzidas pela Inteligência Artificial.

A estratégia utilizada foi começar com uma pergunta simples e aumentar gradualmente o nível de especificidade, contexto e estrutura das solicitações.

---

# 2. Teste 1 — Prompt inicial

## Prompt utilizado

> Explique o que é Python e o que é automação de tarefas.

## Resultado

O NotebookLM apresentou uma explicação sobre Python baseada na documentação disponível.

Entretanto, ao abordar automação de tarefas, identificou que as fontes disponíveis não apresentavam uma definição conceitual direta sobre o termo.

A resposta relacionou a automação principalmente aos recursos dos módulos `os` e `pathlib`, apresentando possibilidades de interação com arquivos, diretórios e o sistema operacional.

## Limitação identificada

A pergunta era muito ampla e as fontes disponíveis não cobriam diretamente o conceito de automação de tarefas.

## 🩹 Cicatriz 1 — Curadoria das fontes

O primeiro teste demonstrou que uma resposta da Inteligência Artificial depende também da qualidade e abrangência das fontes fornecidas.

### Aprendizado

Uma pergunta simples pode produzir uma resposta correta, mas insuficiente para o objetivo do estudo.

Foi necessário considerar não apenas a elaboração dos prompts, mas também a qualidade da curadoria das fontes.

---

# 3. Teste 2 — Prompt contextualizado

## Prompt utilizado

> Com base exclusivamente nas fontes disponíveis neste notebook, explique o que é Python e como ele pode ser utilizado para automatizar tarefas. Apresente a explicação para uma pessoa que está começando a estudar programação e inclua exemplos práticos de automação. Quando as fontes não apresentarem informações suficientes sobre determinado conceito, deixe isso explícito em vez de inventar informações.

## Estratégias utilizadas

Neste segundo teste foram adicionadas instruções mais específicas:

* utilização exclusiva das fontes disponíveis;
* definição do público como iniciante;
* solicitação de exemplos práticos;
* orientação para informar quando as fontes fossem insuficientes;
* orientação para não inventar informações.

## Resultado

A resposta tornou-se mais didática e apresentou exemplos relacionados à utilização dos módulos `os` e `pathlib`.

Também foram apresentados exemplos de código relacionados à busca, leitura, escrita e análise de arquivos.

## 🩹 Cicatriz 2 — Necessidade de contexto

O segundo teste demonstrou que definir o público, o objetivo e o tipo de resposta desejada pode melhorar significativamente a utilidade da resposta.

### Aprendizado

Quanto mais claramente o objetivo é apresentado, maior a possibilidade de obter uma resposta adequada à necessidade do estudante.

---

# 4. Teste 3 — Prompt estruturado

## Prompt utilizado

> Analise o conteúdo das fontes disponíveis neste notebook e produza um guia introdutório sobre Python aplicado à automação de tarefas.
>
> O material deve ser direcionado a uma pessoa iniciante em programação.
>
> Organize a resposta obrigatoriamente nas seguintes seções:
>
> 1. Conceito de Python
> 2. Conceito de automação de tarefas
> 3. Relação entre Python e automação
> 4. Principais conceitos de Python necessários para começar
> 5. Utilização do módulo os
> 6. Utilização do módulo pathlib
> 7. Exemplos de automações possíveis
> 8. Diferença entre uma simples operação com arquivos e um processo automatizado
> 9. Cuidados que um iniciante deve ter ao criar scripts de automação
>
> Para cada seção:
>
> * explique o conceito de maneira simples;
> * utilize somente informações sustentadas pelas fontes disponíveis;
> * indique as fontes utilizadas;
> * quando as fontes não forem suficientes para responder completamente, informe explicitamente essa limitação;
> * não invente informações.
>
> Ao final, apresente uma lista com os 5 principais conhecimentos que um iniciante deveria dominar antes de criar seu primeiro script de automação.

## Estratégias utilizadas

O terceiro prompt apresentou uma estrutura muito mais detalhada.

Foram definidos:

* objetivo;
* público-alvo;
* tópicos obrigatórios;
* formato da resposta;
* necessidade de referências;
* tratamento das limitações das fontes;
* restrição contra informações não sustentadas pelas fontes.

## Resultado

O NotebookLM produziu uma resposta estruturada em nove partes, abordando:

* Python;
* automação;
* relação entre Python e automação;
* fundamentos da linguagem;
* módulo `os`;
* módulo `pathlib`;
* exemplos;
* diferenças entre operações simples e automação;
* cuidados e limitações.

A resposta também apresentou as fontes utilizadas para sustentar os tópicos.

---

# 5. 🩹 Cicatriz 3 — Respostas convincentes precisam ser verificadas

Apesar da evolução dos resultados, o terceiro teste também mostrou uma questão importante.

Uma resposta pode estar:

* bem estruturada;
* bem escrita;
* acompanhada de referências;
* tecnicamente convincente;

e ainda assim exigir verificação crítica de detalhes.

Durante a análise da resposta foram identificadas afirmações técnicas que merecem conferência individual antes de serem utilizadas como material definitivo de estudo.

## Aprendizado

A Inteligência Artificial deve ser utilizada como ferramenta de apoio ao aprendizado, e não como substituta da análise crítica.

As respostas precisam ser comparadas com as fontes originais sempre que houver dúvidas ou informações técnicas específicas.

---

# 6. Comparação dos testes

| Teste   | Estratégia             | Resultado                             |
| ------- | ---------------------- | ------------------------------------- |
| Teste 1 | Pergunta simples       | Resposta introdutória, porém limitada |
| Teste 2 | Prompt contextualizado | Resposta mais didática e prática      |
| Teste 3 | Prompt estruturado     | Resposta organizada e mais abrangente |

A evolução demonstrou que a elaboração de prompts mais específicos contribuiu para obter respostas mais alinhadas ao objetivo do estudo.

---

# 7. Principais aprendizados sobre prompts

Durante os testes foram identificados alguns princípios importantes:

### 1. Definir o objetivo

A IA precisa saber o que se pretende obter com a pergunta.

### 2. Definir o público

Informar que o conteúdo é destinado a um iniciante ajuda a direcionar a linguagem da resposta.

### 3. Definir o formato

Solicitar seções, listas, exemplos ou etapas ajuda a organizar o resultado.

### 4. Restringir as fontes

Solicitar que a resposta utilize exclusivamente determinadas fontes ajuda a manter o estudo baseado no material selecionado.

### 5. Pedir transparência sobre limitações

Instruir a IA a informar quando as fontes forem insuficientes reduz o risco de aceitar informações não sustentadas pelo material estudado.

### 6. Verificar as respostas

Mesmo quando uma resposta parece correta, informações técnicas devem ser verificadas nas fontes originais.

---

# 8. Conclusão

Os testes demonstraram que a qualidade da interação com uma ferramenta de Inteligência Artificial depende não apenas da tecnologia utilizada, mas também da capacidade do usuário de formular perguntas, fornecer contexto, definir objetivos e analisar criticamente as respostas.

O processo de tentativa, identificação de limitações e melhoria dos prompts foi utilizado como parte do próprio processo de aprendizagem.
