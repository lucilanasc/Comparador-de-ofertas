# Comparador-de-ofertas
Este é um comparador de preços inteligente em tempo real feito em Python. Utiliza Playwright para mineração de dados (Web Scraping) assíncrona no Buscapé e CustomTkinter para uma interface gráfica (GUI) moderna e multi-thread.

# 🔍 Buscador de Ofertas Inteligente

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Playwright](https://img.shields.io/badge/Playwright-Automated-green.svg)
![CustomTkinter](https://img.shields.io/badge/UI-CustomTkinter-orange.svg)

Uma aplicação desktop moderna e eficiente desenvolvida em Python para monitoramento e comparação de preços em tempo real. O software automatiza a busca de produtos na web, minera as informações de forma inteligente e entrega ao usuário uma lista organizada das melhores ofertas, ordenadas do menor para o maior preço.

---

## 🚀 Demonstração



https://github.com/user-attachments/assets/73c14199-3f21-4266-8e3a-ee5eb32763c7



---

## 🛠️ Arquitetura e Soluções Técnicas

Para garantir uma aplicação robusta com nível de produção, o projeto foi estruturado separando a lógica de interface da lógica de automação:

* **Interface Gráfica Humana (GUI):** Construída com **CustomTkinter**, oferecendo um design moderno com suporte nativo a modo escuro/claro e componentes responsivos.
* **Processamento em Segundo Plano (Multi-threading):** A busca de dados na web pode levar alguns segundos. Para evitar que a interface gráfica congele ou pareça travada para o usuário, a automação roda em uma linha de execução separada (`threading.Thread`).
* **Automação de Alto Desempenho (Playwright Async):** Utilização do **Playwright** em modo assíncrono para controlar o motor do navegador Chromium. A estratégia garante velocidade na raspagem de dados.
* **Bypass de Bloqueios (Persistent Context):** Implementação de gerenciamento de sessão persistente (`launch_persistent_context`) para armazenar cookies e históricos locais, simulando o comportamento de um usuário real e mitigando bloqueios por CAPTCHA.
* **Seletores Robustos (Fallback & Herança):** Mineração de dados baseada em seletores genéricos por tags nativas (como `h2` e herança estrutural), tornando o script resiliente a mudanças dinâmicas no layout do site alvo.

---

## 📋 Como Executar o Projeto

### Pré-requisitos
Antes de começar, você precisará ter o Python instalado em sua máquina.

##PASSO A PASSO##

1. Clonar o Repositório

2. Instalar as Dependências
Instale os pacotes necessários utilizando o gerenciador de pacotes do Python:

No CMD:
pip install playwright customtkinter pandas 

3. Instalar os Motores do Navegador
Inicialize os binários do Chromium necessários para o Playwright:

No CMD:
playwright install chromium

4. Rodar a Aplicação
Execute o arquivo principal da interface gráfica:
python interface.py

-----------------------------------

📈 Próximos Passos (Roadmap de Evolução)
[ ] Implementar exportação automática dos resultados para planilhas Excel (.xlsx) ou arquivos .csv utilizando a biblioteca Pandas.

[ ] Adicionar suporte a múltiplos sites em paralelo (ex: Buscapé + Zoom + Google Shopping).

[ ] Migrar a interface para a web utilizando Streamlit para permitir deploy em nuvem pública.

Desenvolvido por Lucila de Souza Monteiro do Nascimento - Sinta-se à vontade para se conectar ou dar uma ⭐️ no projeto!
