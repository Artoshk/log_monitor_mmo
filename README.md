# Simulação e Análise de Logs de MMORPG

Este projeto utiliza um notebook Jupyter para simular a geração de logs de um MMORPG (Massively Multiplayer Online Role-Playing Game) fictício no formato JSON Lines. Após a geração, os logs são processados e analisados usando Pandas e visualizados com Matplotlib/Seaborn para extrair insights sobre a atividade dos jogadores e possíveis comportamentos suspeitos.

Ele foi desenvolvido como atividade avaliativa da disciplina de Logs.

## Desenvolvedores:
### Anderson Luiz Karl - 2417571
### George Ferreira de Alencar - 2326888
### Maria Elisa Gomes de Matos - 2417598
### Saynarah Cruz Nabuco - 2417049

## Objetivos

*   **Simular** a geração de logs de eventos de jogo (login, logout, PvP, PvE, trocas, drops de item, atividades suspeitas) em formato JSON Lines.
*   **Processar** os logs gerados utilizando a biblioteca Pandas para carregar, limpar e preparar os dados para análise.
*   **Visualizar** métricas importantes como:
    *   Concentração de jogadores no mapa (heatmap).
    *   Locais mais populares.
    *   Distribuição dos tipos de eventos.
    *   Jogadores com mais eliminações PvP ou de chefes (Boss Kills).
    *   Jogadores com mais drops de itens raros.
    *   Atividade suspeita por tipo e por jogador.
    *   Atividade geral ao longo do tempo.
*   **Demonstrar** como esses logs podem ser usados para monitoramento e análise de comportamento dentro do jogo.

## Requisitos

*   [UV](https://docs.astral.sh/uv/) (gerenciador de pacotes e ambientes virtuais Python) instalado.

## Instalação e Configuração com UV

O **UV** é usado para gerenciar o ambiente virtual e as dependências do projeto de forma rápida e eficiente.

1.  **Clone o repositório:**
    ```bash
    git clone git@github.com:Artoshk/log_monitor_mmo.git
    cd log_monitor_mmo
    ```

2.  **Instale o UV:**
    Caso ainda não tenha o UV instalado, siga as instruções na [documentação oficial](https://docs.astral.sh/uv/install.sh). Um método comum para Linux/macOS é:
    ```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
    ```
    Para outros métodos, consulte a documentação.

3.  **Sincronize o ambiente e instale as dependências:**
    No terminal, dentro do diretório do projeto, execute:
    ```bash
    uv sync
    ```
    Este comando irá:
    *   Criar um ambiente virtual chamado `.venv` no diretório do projeto (se ele não existir).
    *   Instalar todas as dependências listadas no arquivo `pyproject.toml` (ou `requirements.txt` se você o usar com `uv pip sync`) dentro deste ambiente virtual.

## Como Executar o Notebook

1.  **Ative o ambiente virtual:**
    *   **Manualmente (Linux/macOS):** `source .venv/bin/activate`
    *   **Manualmente (Windows CMD):** `.venv\Scripts\activate.bat`
    *   **Manualmente (Windows PowerShell):** `.venv\Scripts\Activate.ps1`
    *   *Nota: Editores como VS Code geralmente detectam o ambiente `.venv` e oferecem a opção de ativá-lo automaticamente ou selecionar o interpretador Python correto.*

2.  **Inicie o Jupyter:**
    No terminal com o ambiente ativado, inicie o Jupyter Lab ou Notebook:
    ```bash
    jupyter lab
    ```
    ou
    ```bash
    jupyter notebook
    ```

3.  **Abra o Notebook:**
    Navegue até o arquivo `.ipynb` do projeto na interface do Jupyter e abra-o.

4.  **Selecione o Kernel Correto:**
    Dentro do notebook, certifique-se de que o kernel selecionado seja o do ambiente virtual `.venv`. Geralmente, ele aparece com um nome como ".venv" ou similar na lista de kernels disponíveis.

5.  **Execute as Células:**
    Execute as células do notebook sequencialmente. Você pode usar "Run All" (Executar Todas) no menu ou executar célula por célula (usando Shift+Enter).

## Arquivo de Log Gerado

A execução da simulação no notebook criará (ou sobrescreverá) um arquivo chamado `game_logs.jsonl` no mesmo diretório. Este arquivo contém os logs simulados no formato JSON Lines, que são então lidos e processados pelas células subsequentes de análise e visualização.

---

Sinta-se à vontade para adaptar os nomes dos arquivos e URLs conforme necessário.
