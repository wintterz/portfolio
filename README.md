# Portfólio — Bruno Meirelles

Coletânea de projetos de automação e desenvolvimento que construí resolvendo problemas reais de operação (comércio exterior, fiscal, vendas, RH e TI). Cada item descreve o **problema**, a **solução**, o **stack** e o **resultado**.

> Os projetos foram desenvolvidos em ambiente corporativo; por isso este portfólio apresenta estudos de caso, sem o código ou dados internos.

---

## 🧾 Emissor de Commercial Invoice (Exportação)

**Problema:** a emissão de invoices de exportação era manual, propensa a erro e com formatos diferentes por região.  
**Solução:** aplicação em **Flask** que gera invoices em **PDF** (ReportLab) e **Excel** (openpyxl, com os templates reais da empresa) a partir dos dados do ERP, com bifurcação **América/Europa** (moeda, bloco bancário e campos de FOB/frete/seguro por região).  
**Stack:** Python · Flask · ReportLab · openpyxl · PostgreSQL (psycopg2) · PyInstaller  
**Resultado:** emissão padronizada e em segundos, usada pela equipe de exportação.

## 📦 DUIMP App

**Problema:** o processamento de declarações de importação (DUIMP) exigia muitos passos manuais e divisão de notas por regras complexas.  
**Solução:** aplicativo desktop em **tkinter**, em produção, com aba de NCM/alíquota por filial, suporte a declarações complementares e um motor de divisão de notas por item com regra de três níveis.  
**Stack:** Python · tkinter  
**Resultado:** padronização e agilidade no processamento das declarações.

## 🔁 Gerador de Tradução (Normalizador de Invoices)

**Problema:** cada fornecedor envia invoices em um layout diferente, exigindo retrabalho de tradução/conferência.  
**Solução:** normalizador multi-fornecedor com arquitetura **core + adapters** — o núcleo trata a lógica comum e cada fornecedor tem um adaptador próprio, facilitando adicionar novos sem mexer no core.  
**Stack:** Python  
**Resultado:** padronização dos dados de entrada e base extensível para novos fornecedores.

## ⚙️ Automação de CST no ERP (RPA)

**Problema:** alterar a tributação (CST Estadual) de dezenas de registros no ERP, uma a uma, é lento e sujeito a erro.  
**Solução:** app com interface em **CustomTkinter** que usa **Playwright** (Chromium próprio com login automático) para alterar os registros em massa, executado de forma supervisionada.  
**Stack:** Python · CustomTkinter · Playwright  
**Resultado:** alteração em lote confiável, com validação antes da execução.

## 🕒 Automação de Espelho de Ponto (RH)

**Problema:** o RH extraía manualmente os relatórios de ponto de cada filial, todo mês.  
**Solução:** automação em **Playwright/Python** que navega no sistema de ponto, filtra o período, exporta os relatórios das filiais e salva automaticamente na nuvem (SharePoint).  
**Stack:** Python · Playwright  
**Resultado:** ~140 arquivos processados no backfill + rotina mensal recorrente, sem intervenção manual.

## 📊 Automação de Relatório Fiscal (Protocolo de Tributos)

**Problema:** o relatório mensal de notas de serviço tomadas era montado manualmente em planilha.  
**Solução:** solução em **Excel + Power Query** conectada ao banco via **ODBC**, cruzando documentos fiscais por CNPJ e número da nota, com complemento de dados cadastrais via **API REST** (ReceitaWS).  
**Stack:** Power Query · SQL · ODBC · API REST  
**Resultado:** relatório atualizável que vive junto da equipe fiscal, sem montagem manual.

---

## 📚 Outros projetos

- **Monitor da integração Sintel/mdiweb** — reconciliação de pedidos importados para o ERP, sinalizando falhas silenciosas.
- **Alertas de preço zerado (Zapier)** — e-mail diário sinalizando produtos ativos sem preço (~789 itens): PostgreSQL → Zapier → Outlook.
- **CUSTO DIÁRIO (Zapier)** — consulta diária de variações de custo formatada em tabela e enviada por e-mail à diretoria.
- **Upload de fotos de produtos** — automação de carga de 4.400+ itens com auditoria final no banco.
- **Mapa de Compras** — substituição de planilha manual de 14 abas por workbook Power Query + SQL.
- **Resumo por Margem Bruta** — automação de fechamento mensal em Python com interface gráfica (CustomTkinter).
- **Gerador de Arquivo de Importação** — app desktop que gera o arquivo de pedido no layout padrão do ERP a partir de dados colados/importados.
- **Mapeamento de campos do ERP** — documentação navegável (HTML) das telas do sistema para treinamento de novos colaboradores.

---

### 📫 Contato

📧 brumxw@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/bruno-meirelles-0b35b51b9/) · 📍 Jundiaí, SP
