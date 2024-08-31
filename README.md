# Web Scraper para Notícias do Omelete

Este projeto é um script em Python que utiliza Selenium e BeautifulSoup para automatizar a coleta de notícias do site [Omelete](https://www.omelete.com.br/). O script busca por notícias relacionadas ao "Deadpool", rola a página para carregar mais conteúdos, e salva as informações em um arquivo de texto.

## Pré-requisitos

- Python 
- Selenium
- BeautifulSoup4
- ChromeDriver

## Instalação

1. **Instale as dependências**:

    Você pode usar `pip` para instalar as dependências necessárias. Certifique-se de ter o `pip` instalado:

    ```bash
    pip install selenium beautifulsoup4
    ```

3. **Baixe o ChromeDriver**:

    O ChromeDriver é necessário para que o Selenium interaja com o navegador Chrome. Baixe a versão apropriada do [ChromeDriver](https://sites.google.com/chromium.org/driver/) e coloque-o na pasta `driverevio` dentro do diretório do projeto.

    Certifique-se de que o caminho para o ChromeDriver no código (`CHROME_DRIVER_PATH`) está correto. No código fornecido, o caminho é configurado como:

    ```python
    CHROME_DRIVER_PATH = ROOT_FOLDER / 'driverevio' / 'chromedriver.exe'
    ```

## Uso

1. **Execute o script**:

    Após configurar o ambiente e garantir que o ChromeDriver está no caminho correto, execute o script Python:

    ```bash
    python seu_script.py
    ```

2. **Verifique o arquivo de saída**:

    O script irá gerar um arquivo `deadpool.txt` no diretório do projeto com os títulos e datas das notícias coletadas.

## Funcionamento

- O script abre o site Omelete e navega até a página de notícias.
- Realiza uma busca por "Deadpool" usando o campo de pesquisa.
- Rola a página para baixo e clica no botão "VER MAIS" até que não haja mais conteúdo para carregar.
- Coleta as notícias, extrai os títulos e datas, e os salva em um arquivo de texto.

## Observações

- Certifique de ter o navegador Google Chrome instalado na mesma versão do ChromeDriver.
- Caso haja mudanças no layout do site, você pode precisar ajustar os seletores no código.

## Contribuição

Se você deseja contribuir para o projeto, por favor, faça um fork do repositório e envie um pull request com suas alterações.
