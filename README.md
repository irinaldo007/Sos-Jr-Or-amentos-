# 📑 Gerador de Orçamentos Profissionais — Sos Jr Soluções

![Status](https://img.shields.io/badge/Status-Produção-success?style=for-the-badge)
![Versão](https://img.shields.io/badge/Versão-1.0.0-blue?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Plataforma-Web%20%7C%20Windows-informational?style=for-the-badge)
![Deploy](https://img.shields.io/badge/Deploy-GitHub%20Pages-222222?style=for-the-badge&logo=githubpages&logoColor=white)

> Sistema web e desktop desenvolvido para automação, padronização e controle na emissão de propostas comerciais e orçamentos técnicos de engenharia e instalações.

---

### 🌐 Acesso Rápido

| Canal | Link |
| :--- | :--- |
| **Aplicação Online (Live Demo)** | [![Acessar](https://img.shields.io/badge/Abrir-GitHub%20Pages-181717?style=flat-square&logo=github)](https://irinaldo007.github.io/Sos-Jr-Or-amentos-/) |
| **Repositório do Código** | [![Repositório](https://img.shields.io/badge/Código-GitHub-blue?style=flat-square&logo=github)](https://github.com/irinaldo007/Sos-Jr-Or-amentos-) |

---

## 🏢 Dados da Empresa

* **Razão Social:** Sos Jr Soluções
* **CNPJ:** `21.117.755/0001-40`
* **Localização:** Porto Velho - RO | CEP: 76525-315
* **Contato Técnico:** +55 (69) 99281-9812

---

## 🎯 Objetivo do Projeto

Eliminar o preenchimento manual de propostas de serviços, garantindo velocidade no cálculo de materiais e mão de obra, cálculo instantâneo de descontos e emissão imediata de orçamentos padronizados em layout oficial A4 para impressão ou exportação em PDF.

---

## 🛠️ Tecnologias Utilizadas

| Camada | Tecnologia | Descrição |
| :--- | :--- | :--- |
| **Estrutura** | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) | Formulários dinâmicos e template de documento A4 |
| **Estilização** | ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) | Design responsivo com regras otimizadas de impressão `@media print` |
| **Lógica** | ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) | Manipulação do DOM, cálculo automático de totais e filtros |
| **Armazenamento** | ![Web Storage](https://img.shields.io/badge/Storage-localStorage-green?style=flat-square) | Persistência local no navegador sem dependência de banco externo |
| **Desktop Runtime** | ![Electron](https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white) | Encapsulamento da aplicação web em janela desktop nativa |
| **Distribuição** | ![electron-builder](https://img.shields.io/badge/Builder-electron--builder-orange?style=flat-square) | Compilação e empacotamento do instalador executável (`.exe`) |

---

## 🚀 Funcionalidades da Versão 1.0.0

* **Formulário de Preenchimento Dinâmico:** Numeração sequencial de proposta, dados completos do cliente, título e descrição detalhada do escopo técnico.
* **Tabela de Itens Inteligente:** Adição e exclusão dinâmica de produtos/serviços com cálculo em tempo real de quantidade, valor unitário e total.
* **Condições Comerciais Flexíveis:** Suporte a PIX, Cartão, Dinheiro, Boleto e Transferência, além de campo para aplicação direta de descontos (R$).
* **Espelho Oficial A4:** Cabeçalho institucional com logo e CNPJ, resumo financeiro discriminado, chave PIX, cláusulas de garantia/validade e linhas de assinatura formais.
* **Gerenciamento & Histórico Local:** Painel com busca rápida por cliente/número, filtros por status (`📝 Rascunho`, `🔍 Em Análise`, `✅ Aprovado`, `❌ Recusado`) e métricas de conversão.
* **Impressão Otimizada:** Gatilho nativo com isolamento do espelho de orçamento e ocultação automática dos botões de controle.
* **Instalador Desktop:** Executável portátil gerado em `exe-output/Sos Jr Orçamentos Setup 1.0.0.exe`.

---

## 📁 Estrutura do Projeto

```bash
Sos presificat/
├── orcamento.html               # Página principal (Formulário + Espelho A4)
├── orcamento-sos-jr.html        # Versão alternativa de layout
├── logo.png                     # Identidade visual institucional
├── electron-main.js             # Processo principal do runtime Electron
├── package.json                 # Metadados e scripts de build
├── converter-logo.bat           # Conversor de imagem para .ico
├── INSTRUÇÕES EXE.txt           # Guia de compilação desktop
├── HISTORICO_DESENVOLVIMENTO.md # Registro detalhado de desenvolvimento
└── exe-output/                  # Instalador executável Windows (.exe)

```

---

## 🔧 Notas Técnicas & Soluções de Build

> [!NOTE]
> **Criação de Symlinks no Windows:**
> O `electron-builder` exigia privilégios de administrador para links simbólicos durante o empacotamento.
> **Solução:** Adicionada a instrução `"signAndEditExecutable": false` nas configurações do `package.json`.

> [!TIP]
> **Arquivo `app.asar` Bloqueado:**
> Processos em segundo plano travavam o arquivo durante novas compilações na pasta padrão.
> **Solução:** Configurado o redirecionamento de saída para o diretório isolado `exe-output/`.

---

## 🗺️ Próximas Melhorias Planejadas

* [ ] Exportação nativa para PDF via biblioteca cliente (`html2pdf.js` / `jsPDF`).
* [ ] Migração do banco local para `IndexedDB` para suportar fotos e anexos.
* [ ] Cadastro e seleção de templates de serviços pré-configurados.
* [ ] Integração com WhatsApp API para envio direto da proposta ao cliente.
* [ ] Dashboard com gráficos de faturamento mensal e taxa de aprovação.

---

## 📂 Como Executar Localmente

1. Clone o repositório:
```bash
git clone [https://github.com/irinaldo007/Sos-Jr-Or-amentos-.git](https://github.com/irinaldo007/Sos-Jr-Or-amentos-.git)

```


2. Acesse a pasta do projeto:
```bash
cd Sos-Jr-Or-amentos-

```


3. Para rodar a versão web:
* Abra o arquivo `orcamento.html` em qualquer navegador.


4. Para rodar no Electron (modo Desktop):
```bash
npm install
npm start

```



---

## 👨‍💻 Autor

**Desenvolvido por Irinaldo Soares da Silva Junior**

*Engenheiro Civil | Técnico em Eletrotécnica | Graduando em Análise e Desenvolvimento de Sistemas (ADS)*



---

*Projeto desenvolvido com foco em normas técnicas, segurança e engenharia aplicada.*
