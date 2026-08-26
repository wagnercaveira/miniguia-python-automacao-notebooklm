# 🐍 Miniguia de Estudo — Python para Automação de Tarefas

## 1. Introdução

Python é uma linguagem de programação conhecida por sua sintaxe clara, facilidade de aprendizado e grande biblioteca padrão.

Uma das possibilidades de utilização da linguagem é o desenvolvimento de scripts capazes de automatizar tarefas relacionadas ao computador, arquivos, diretórios e sistema operacional.

Este miniguia foi desenvolvido a partir da análise das fontes selecionadas no NotebookLM e tem como objetivo servir como material de consulta para os primeiros estudos sobre Python aplicado à automação.

---

# 2. O que é Python?

Python é uma linguagem de programação de alto nível, interpretada e com suporte à programação orientada a objetos.

Entre suas características estão:

* sintaxe considerada simples e legível;
* tipagem dinâmica;
* estruturas de dados de alto nível;
* biblioteca padrão extensa;
* possibilidade de utilização em diferentes plataformas;
* capacidade de criação de scripts e aplicações.

Para quem está começando, Python permite aprender conceitos fundamentais de programação sem que a sintaxe seja excessivamente complexa.

### Conceito-chave

> Python pode ser utilizado tanto para desenvolver aplicações quanto para criar scripts destinados à execução de tarefas específicas.

**Fonte principal:** The Python Tutorial.

---

# 3. O que é automação de tarefas?

No contexto deste estudo, automação de tarefas pode ser entendida como a utilização de programas ou scripts para executar automaticamente operações que poderiam exigir intervenção manual.

As fontes selecionadas não apresentam uma definição teórica única e direta para o conceito de automação de tarefas. Entretanto, a documentação dos módulos `os` e `pathlib` demonstra diversos recursos que podem ser utilizados para automatizar operações relacionadas a arquivos, diretórios e ao sistema operacional.

Exemplos:

* procurar arquivos;
* listar diretórios;
* verificar a existência de arquivos;
* ler e escrever informações;
* criar diretórios;
* processar vários arquivos;
* gerar informações automaticamente.

### Conceito-chave

> Automação consiste em transformar uma tarefa repetitiva em um processo que pode ser executado por um programa com pouca ou nenhuma intervenção manual.

**Observação:** essa definição representa uma síntese do processo de estudo e não uma definição literal encontrada em uma única fonte.

---

# 4. Por que utilizar Python para automação?

Python apresenta características que favorecem a criação de scripts.

Entre elas:

### Facilidade de desenvolvimento

A sintaxe da linguagem facilita a criação e manutenção de scripts.

### Biblioteca padrão

Python possui uma biblioteca padrão extensa, oferecendo recursos para diversas tarefas.

### Interação com o sistema

Módulos como `os` permitem acessar funcionalidades relacionadas ao sistema operacional.

### Manipulação de arquivos

O módulo `pathlib` oferece ferramentas específicas para trabalhar com caminhos e sistemas de arquivos.

### Portabilidade

Python está disponível para diferentes plataformas, embora algumas funcionalidades possam apresentar diferenças dependendo do sistema operacional.

---

# 5. Fundamentos necessários

Antes de desenvolver automações, é importante conhecer os fundamentos da linguagem.

## 5.1 Variáveis e tipos de dados

Variáveis permitem armazenar informações que serão utilizadas pelo programa.

Entre os tipos de dados básicos estão:

* números;
* strings;
* listas;
* tuplas;
* conjuntos;
* dicionários.

---

## 5.2 Condições

Estruturas como:

```python
if
elif
else
```

permitem que o programa tome decisões.

Exemplo:

```python
from pathlib import Path

arquivo = Path("relatorio.txt")

if arquivo.exists():
    print("O arquivo existe.")
else:
    print("O arquivo não existe.")
```

---

## 5.3 Loops

Os loops permitem executar uma operação várias vezes.

Exemplo:

```python
for arquivo in arquivos:
    print(arquivo)
```

Isso é especialmente importante em automação porque frequentemente precisamos processar vários arquivos ou diretórios.

---

## 5.4 Funções

Funções permitem organizar operações em blocos reutilizáveis.

Exemplo:

```python
def mostrar_arquivo(nome):
    print(nome)
```

A utilização de funções ajuda a organizar scripts maiores.

---

# 6. Trabalhando com arquivos

A manipulação de arquivos é uma das áreas mais importantes para automação.

Python possui recursos para:

* abrir arquivos;
* ler informações;
* escrever informações;
* criar arquivos;
* verificar arquivos;
* localizar arquivos;
* trabalhar com diretórios.

Um exemplo simples utilizando `pathlib`:

```python
from pathlib import Path

arquivo = Path("exemplo.txt")

arquivo.write_text("Arquivo criado automaticamente.")

conteudo = arquivo.read_text()

print(conteudo)
```

Nesse exemplo, o Python cria um arquivo, grava informações e depois lê o conteúdo.

---

# 7. O módulo `os`

O módulo `os` fornece funcionalidades para interação com o sistema operacional.

Entre suas possibilidades estão:

* consultar o diretório de trabalho;
* alterar o diretório atual;
* listar diretórios;
* criar diretórios;
* remover arquivos;
* trabalhar com variáveis de ambiente;
* percorrer estruturas de diretórios.

Exemplo:

```python
import os

print(os.getcwd())
```

O comando apresenta o diretório de trabalho atual.

---

# 8. O módulo `pathlib`

O `pathlib` fornece uma abordagem orientada a objetos para trabalhar com caminhos do sistema de arquivos.

Exemplo:

```python
from pathlib import Path

pasta = Path("documentos")

if pasta.exists():
    print("A pasta existe.")
```

Também podemos utilizar métodos para procurar arquivos.

```python
from pathlib import Path

pasta = Path(".")

arquivos_python = list(pasta.glob("**/*.py"))

for arquivo in arquivos_python:
    print(arquivo)
```

Esse exemplo procura arquivos Python dentro da estrutura de diretórios a partir do caminho especificado.

---

# 9. Exemplos de automação

A partir dos conhecimentos estudados, algumas possibilidades são:

### Organização de arquivos

Criar um script que identifica arquivos por extensão e os direciona para determinadas pastas.

### Busca automática

Localizar arquivos específicos dentro de várias pastas.

### Relatórios

Percorrer diretórios e gerar informações sobre arquivos encontrados.

### Leitura e processamento

Ler arquivos automaticamente, processar seus conteúdos e gerar novos arquivos.

### Monitoramento

Verificar periodicamente informações relacionadas a arquivos e diretórios.

---

# 10. Cuidados ao criar automações

Automação não significa simplesmente executar uma tarefa rapidamente.

Um script mal elaborado pode causar problemas.

## 10.1 Arquivos importantes

Scripts que excluem ou movimentam arquivos devem ser testados cuidadosamente.

Uma operação recursiva configurada incorretamente pode atingir arquivos que não deveriam ser modificados.

---

## 10.2 Tratamento de erros

Operações com arquivos podem gerar erros.

Por exemplo:

```python
try:
    arquivo = Path("dados.txt")
    conteudo = arquivo.read_text()
except FileNotFoundError:
    print("Arquivo não encontrado.")
```

O tratamento de exceções permite que o programa responda de maneira controlada a determinadas situações.

---

## 10.3 Portabilidade

Um script pode apresentar comportamentos diferentes dependendo do sistema operacional.

Por isso, é importante considerar as diferenças entre ambientes Windows, Linux e outros sistemas.

---

## 10.4 Links simbólicos

Varreduras recursivas que seguem links simbólicos precisam ser utilizadas com cuidado, pois podem resultar em ciclos de diretórios.

---

## 10.5 Testes

Antes de executar uma automação em arquivos importantes:

1. testar em uma pasta de testes;
2. utilizar arquivos sem importância;
3. verificar os resultados;
4. somente depois utilizar dados reais.

---

# 11. Trilha de aprendizagem

A partir das pesquisas realizadas, foi organizada a seguinte sequência:

### Nível 1 — Fundamentos

Aprender:

* variáveis;
* tipos de dados;
* strings;
* listas;
* operações básicas;
* execução de scripts.

### Nível 2 — Controle de fluxo

Aprender:

* `if`;
* `elif`;
* `else`;
* `for`;
* `while`;
* funções;
* estruturas de dados.

### Nível 3 — Arquivos

Aprender:

* leitura;
* escrita;
* entrada e saída;
* módulos;
* JSON;
* tratamento de erros.

### Nível 4 — Automação

Aprender:

* `os`;
* `pathlib`;
* arquivos;
* diretórios;
* busca;
* processamento em lote.

### Nível 5 — Segurança e boas práticas

Aprender:

* tratamento de exceções;
* portabilidade;
* links simbólicos;
* operações destrutivas;
* testes;
* utilização segura de scripts.

---

# 12. Glossário

| Termo                   | Significado                                                                        |
| ----------------------- | ---------------------------------------------------------------------------------- |
| **Python**              | Linguagem de programação utilizada para desenvolver aplicações e scripts.          |
| **Script**              | Programa normalmente criado para executar uma tarefa ou conjunto de tarefas.       |
| **Automação**           | Execução programática de tarefas que poderiam ser realizadas manualmente.          |
| **Interpretador**       | Programa responsável por executar o código Python.                                 |
| **String**              | Tipo de dado utilizado para representar texto.                                     |
| **Lista**               | Estrutura de dados que permite armazenar uma sequência de elementos.               |
| **Função**              | Bloco de código reutilizável destinado à realização de uma operação.               |
| **Módulo**              | Arquivo ou componente que disponibiliza código que pode ser reutilizado.           |
| **Biblioteca padrão**   | Conjunto de módulos disponibilizados junto ao Python.                              |
| **Sistema de arquivos** | Estrutura utilizada pelo sistema operacional para organizar arquivos e diretórios. |
| **Diretório**           | Estrutura utilizada para organizar arquivos e outros diretórios.                   |
| **`os`**                | Módulo Python que fornece recursos de interação com o sistema operacional.         |
| **`pathlib`**           | Módulo Python destinado ao trabalho orientado a objetos com caminhos de arquivos.  |
| **Path**                | Representação de um caminho de arquivo ou diretório.                               |
| **Loop**                | Estrutura utilizada para repetir operações.                                        |
| **Exceção**             | Situação de erro ou condição excepcional durante a execução do programa.           |
| **Portabilidade**       | Capacidade de um programa funcionar em diferentes plataformas.                     |
| **Link simbólico**      | Referência que aponta para outro arquivo ou diretório.                             |

---

# 13. Prompts reutilizáveis

Os prompts abaixo podem ser utilizados futuramente para revisar o conteúdo estudado.

## Prompt 1 — Revisão geral

> Com base exclusivamente nas fontes disponíveis, faça uma revisão dos principais conceitos de Python relacionados à automação de tarefas. Explique o conteúdo para um iniciante e apresente exemplos simples.

---

## Prompt 2 — Teste de conhecimento

> Crie 10 perguntas sobre Python e automação de tarefas utilizando exclusivamente as fontes disponíveis. Não apresente as respostas inicialmente. Depois que eu responder, corrija minhas respostas e explique meus erros.

---

## Prompt 3 — Revisão de arquivos

> Explique como Python pode ser utilizado para trabalhar com arquivos e diretórios. Compare os recursos do módulo os e do módulo pathlib e apresente exemplos simples.

---

## Prompt 4 — Aprendizagem progressiva

> Estou estudando Python para futuramente desenvolver automações. Com base nas fontes disponíveis, identifique quais conhecimentos devo estudar primeiro, quais devo estudar depois e quais dependem de conhecimentos anteriores.

---

## Prompt 5 — Análise de código

> Analise o código Python abaixo considerando que sou iniciante. Explique cada parte do código, identifique possíveis erros ou riscos e sugira melhorias somente quando elas puderem ser sustentadas pelas fontes disponíveis.

---

## Prompt 6 — Preparação para prática

> Com base nas fontes disponíveis, proponha um pequeno exercício prático de Python relacionado à manipulação de arquivos. O exercício deve ser adequado para um iniciante e deve permitir aplicar os conceitos estudados.

---

# 14. Conclusão

O estudo demonstrou que Python possui recursos que podem ser utilizados na criação de scripts para automatizar diversas tarefas relacionadas ao sistema operacional e ao gerenciamento de arquivos.

Também foi possível perceber que a utilização de Inteligência Artificial exige pensamento crítico.

Durante os testes realizados no NotebookLM, a melhoria dos prompts produziu respostas mais organizadas e adequadas aos objetivos do estudo.

Ao mesmo tempo, algumas limitações das fontes e possíveis pontos de verificação foram identificados.

Dessa forma, o NotebookLM foi utilizado não apenas como ferramenta para obter respostas, mas como apoio ao processo de pesquisa, organização, revisão e aprendizagem.

---

## 📚 Fontes utilizadas

* Python Documentation
* The Python Tutorial
* os — Miscellaneous operating system interfaces
* pathlib — Object-oriented filesystem paths

As informações detalhadas sobre a curadoria das fontes podem ser encontradas no arquivo [`fontes/fontes.md`](../fontes/fontes.md).

Os testes de prompts e as dificuldades encontradas durante o processo estão documentados em [`prompts/prompts-utilizados.md`](../prompts/prompts-utilizados.md).
