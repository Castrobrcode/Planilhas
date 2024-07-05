📄 Descrição do Projeto
Este projeto é um script em Python que automatiza a interação com um site para consulta de status de CPF e registra os resultados em planilhas do Excel. Utilizando as bibliotecas selenium para automação do navegador e openpyxl para manipulação de arquivos Excel, o script lê dados de uma planilha, realiza consultas no site, processa os resultados e salva as informações atualizadas em uma nova planilha.

🚀 Funcionalidades
Leitura de Dados: O script lê dados como nome, valor, CPF e data de vencimento de uma planilha Excel (dados_clientes.xlsx).
Automação do Navegador: Utiliza o Selenium WebDriver para abrir um navegador Firefox e navegar até um site de consulta de CPF.
Interação com o Site: Preenche automaticamente o campo de CPF, clica no botão de consulta e extrai o status do CPF.
Processamento de Resultados: Verifica se o status do CPF está "em dia" ou "pendente" e extrai informações adicionais como data de pagamento e método de pagamento, se aplicável.
Armazenamento de Resultados: Salva os resultados da consulta em uma nova planilha Excel (p.xlsx), acrescentando os dados relevantes.
📋 Pré-requisitos
Python 3.x
Selenium
Openpyxl
Navegador Firefox
GeckoDriver (compatível com a versão do Firefox)
🛠️ Instalação
Clone este repositório:
git clone https://github.com/Castrobrcode/Planilhas.git
cd nome-do-repositorio
Instale as dependências:
selenium
openpyxl


pip install selenium openpyxl

Baixe e configure o GeckoDriver:

GeckoDriver
Certifique-se de que o GeckoDriver está no seu PATH.
💻 Como Usar
Prepare a planilha de entrada:

A planilha dados_clientes.xlsx deve estar no diretório planilhas e deve conter as colunas: Nome, Valor, CPF e Data de Vencimento na aba Sheet1.
Execute o script:


python3 main.py
Resultados:

O script abrirá o navegador Firefox, acessará o site de consulta de CPF e processará cada linha da planilha de entrada.
Os resultados serão salvos na planilha p.xlsx no diretório planilhas.
📈 Fluxo do Script
Inicialização:

Carrega a planilha dados_clientes.xlsx.
Inicializa o WebDriver do Firefox e navega até o site de consulta.
Processamento de Linhas da Planilha:

Para cada linha, extrai os dados do cliente e realiza a consulta no site.
Extrai o status do CPF e outras informações adicionais se o CPF estiver "em dia".
Salva os resultados na planilha p.xlsx.
Finalização:

Fecha o navegador.

