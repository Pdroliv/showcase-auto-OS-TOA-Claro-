# showcase-auto-OS-TOA-Claro-
# Auto OS - Automação RPA para Plataforma TOA (Claro)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Playwright](https://img.shields.io/badge/Playwright-Verde?logo=playwright)
![Tkinter](https://img.shields.io/badge/Tkinter-GUI-orange?logo=tkinter)
![Pandas](https://img.shields.io/badge/Pandas-Data-purple?logo=pandas)

> Um script de automação (RPA) com interface gráfica completa para processar Ordens de Serviço (OS) na plataforma TOA da Claro Brasil (`clarobrasil.etadirect.com`).

![GIF da Aplicação em Funcionamento](demo.gif)

---

## ⚠️ Sobre este Repositório

Este é um repositório de **demonstração (portfólio)** para um projeto comercial (RPA) que desenvolvi.

**O código-fonte completo é privado** para proteger a propriedade intelectual e os contratos com clientes. O objetivo aqui é demonstrar as funcionalidades, a arquitetura e as tecnologias que utilizei para resolver um problema de negócio real.

---

## 🎯 O Problema
O processo de "Baixa de OS" na plataforma TOA (Claro) é um fluxo de trabalho manual, repetitivo e sujeito a erros. Cada OS exige múltiplos cliques, preenchimento de campos idênticos e validações, consumindo horas de trabalho operacional.

## 💡 A Solução
O **Auto OS** é um robô (RPA) que automatiza 100% desse fluxo. O usuário simplesmente carrega uma planilha de contratos, gerencia seus logins, e aperta "Iniciar". O robô cuida de todo o processo, desde o login (incluindo 2FA) até a geração de relatórios, liberando a equipe operacional para tarefas de maior valor.

## ✨ Funcionalidades Principais

* **Interface Gráfica (GUI) Completa:**
    * Construído com Python, Tkinter e **ttkbootstrap** para uma experiência de usuário moderna.
    * Controles de execução (Iniciar, Pausar, Parar).
    * Log em tempo real na própria tela.

* **Módulo 1: Preparador de Planilhas:**
    * Carrega planilhas (`.xlsx`/`.csv`) de contratos.
    * Filtra dados por colunas (ex: COP, Operador).
    * Identifica e exporta contratos duplicados.
    * Valida cruzada com relatórios anteriores para remover contratos "já feitos".
    * Gera a planilha final `contratos_para_automacao.xlsx`.

* **Módulo 2: Automação (Robô):**
    * **Gerenciador de Logins:** Armazena múltiplos perfis de login (usuário, senha, 2FA) de forma segura.
    * **Login Automatizado:** Lida com o fluxo de login na plataforma TOA, incluindo autenticação de dois fatores (2FA).
    * **Processamento em Lote:** Lê a planilha e processa cada contrato sequencialmente.
    * **Navegação Inteligente:** Preenche automaticamente as etapas "Dados do Atendimento", "Foto OS Digital" e "Assinatura OS Digital".

* **Módulo 3: Relatórios (Feedback):**
    * Gera um relatório final em Excel (`execution_report_...xlsx`).
    * Formata o relatório com cores (Verde para Sucesso, Vermelho para Erro) para fácil visualização do status de cada contrato.

## 🛠️ Tecnologias Utilizadas

* **Python 3:** Linguagem principal.
* **Playwright:** (Core da Automação) Para automação de navegador moderna e robusta, substituindo o Selenium por ser mais rápido e estável.
* **Tkinter & ttkbootstrap:** (Core da GUI) Para a criação da interface gráfica amigável.
* **Pandas:** Para toda a manipulação de dados e leitura/escrita de arquivos Excel/CSV.
* **Openpyxl:** Usado especificamente para aplicar estilos e cores no relatório final do Excel.

## 📸 Mais Screenshots

**Preparador de Planilhas**
![Tela do Preparador](tela-preparador.png)

**Gerenciador de Logins**
![Tela de Login](tela-login.png)

**Relatório Final (Exemplo)**
![Relatório em Excel](relatorio-exemplo.png)
