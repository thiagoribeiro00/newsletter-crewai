# Newsletter Generator AI

O **Newsletter Generator AI** é uma aplicação que utiliza inteligência artificial para gerar boletins informativos (newsletters) de maneira automatizada, personalizando o conteúdo com base em temas e mensagens fornecidas pelo usuário. A aplicação integra diferentes agentes de IA, cada um com uma função específica, como pesquisa de conteúdo, edição de texto e formatação de newsletters em HTML.

O objetivo principal do projeto é simplificar o processo de criação de newsletters, tornando-o mais eficiente e personalizado, através da colaboração de várias ferramentas baseadas em IA. O sistema realiza a busca de conteúdos relevantes, edita o texto conforme as necessidades do usuário e formata a saída em um arquivo HTML pronto para distribuição.

## Funcionalidade

O sistema funciona em três etapas principais:

1. **Pesquisa de Conteúdo**: Através de um agente de pesquisa, são recuperados conteúdos relacionados ao tema fornecido, com um foco em artigos recentes (última semana).
2. **Edição de Conteúdo**: O conteúdo pesquisado é refinado e adaptado para se alinhar à mensagem e ao tom desejados pelo usuário.
3. **Formatação e Geração de Newsletter**: Um agente designer cria um layout HTML personalizado com base nas informações fornecidas e no conteúdo editado, gerando o arquivo final da newsletter.

## Tecnologias e Ferramentas Utilizadas

O projeto faz uso de várias tecnologias e ferramentas para garantir um fluxo de trabalho eficiente e a geração automatizada de newsletters:

### 1. **CrewAI**
- **Função no Projeto**: Utilizada para organizar os agentes de IA e orquestrar o fluxo de trabalho.

### 2. **LangChain**
- **Função no Projeto**: Usado para integrar agentes como o **ChatAnthropic**, **ChatGroq**, **ChatGoogleGenerativeAI** e outros, permitindo interações entre eles para realizar as tarefas de pesquisa, edição e formatação.

### 3. **Streamlit**
- **Função no Projeto**: Utilizado para a interface do usuário, permitindo aos usuários inserir dados, visualizar o progresso e fazer o download das newsletters geradas.

### 4. **Exa API**
- **Função no Projeto**: Usada para obter conteúdos relacionados ao tema da newsletter a partir de fontes externas.

### 5. **Python**
- **Função no Projeto**: A linguagem principal para desenvolvimento de todo o sistema, incluindo a lógica de orquestração dos agentes e o gerenciamento do fluxo de trabalho.

### 6. **Exa Py**
- **Função no Projeto**: Facilitando a integração com a Exa API para buscar artigos relacionados ao tópico da newsletter.

## Estrutura do Projeto

- **`newsletter_gen/`**: Contém o código principal do sistema, incluindo a definição dos agentes e das ferramentas de IA.
- **`config/`**: Armazena arquivos de configuração, como templates de newsletter e a configuração de agentes.
- **`logs/`**: Armazena os logs gerados durante a execução das tarefas.
- **`src/`**: Contém scripts auxiliares para carregar templates e executar funções relacionadas à geração de newsletters.


## Instalação

Certifique-se de ter Python >=3.10 <=3.13 instalado em seu sistema. Este projeto usa [Poetry](https://python-poetry.org/) para gerenciamento de dependências e manipulação de pacotes, oferecendo uma experiência perfeita de configuração e execução.

Primeiro, se ainda não o fez, instale o Poetry:

```bash
pip install poetry
```

Em seguida, navegue até o diretório do seu projeto e instale as dependências:

1. Primeiro bloqueie as dependências e depois instale-as:
```bash
poetry lock
```
```bash
poetry install
```
## Running the Project

Para iniciar sua equipe de agentes de IA e iniciar a execução de tarefas, execute isto na pasta raiz do seu projeto:

```bash
poetry run newsletter_gen
```

Este comando inicializa o Crew newsletter-gen, montando os agentes e atribuindo-lhes tarefas conforme definido em sua configuração.

Este exemplo, não modificado, irá executar a criação de um arquivo `report.md` com a saída de uma pesquisa sobre LLMs no folser raiz

## Compreendendo seus agentes

A equipe da geração de boletins informativos é composta por vários agentes de IA, cada um com funções, objetivos e ferramentas exclusivos. Esses agentes colaboram em uma série de tarefas, definidas em `config/tasks.yaml`, aproveitando suas habilidades coletivas para atingir objetivos complexos. O arquivo `config/agents.yaml` descreve as capacidades e configurações de cada agente da sua equipe.


