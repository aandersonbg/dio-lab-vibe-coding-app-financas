# 💸 App de Finanças Pessoais (vibe finance) com Vibe Coding por Ari Anderson

Este projeto foi desenvolvido como um Desafio de Projeto da DIO de Vibe Coding utilizando o Lovable e o Copilot Web. A proposta é criar um aplicativo de organização financeira pessoal baseado em interações em linguagem natural.

---

## 📝Segindo a proposta da aula o  PRD Refinado foi refinado no Copilot Web; 
Os seguintes arquivos: 
├─ index.html
├─ styles.css
├─ script.js
├─ README.md
└─ PRD.md 
foram desenvolvido apartir de interaçõe e refinamentos com o Copilot web.

- A primeira interação com o Copilot após as aulas foi solicitar a interpretação de uma imagem que resumia a proposta:

<img width="797" height="439" alt="image" src="https://github.com/user-attachments/assets/c531196d-f4b3-4a73-86bf-c97e663f484b" />

A partir da analise e algumas interaçãoes e refinamentos, cheguei a as seguintes informaçãoes:
O curso “Criando um APP de Organização de Finanças Pessoais com Vibe Coding” da DIO.
Conteúdos do desafio:

Criar PRD
Criar Layout
Criar Repositório
Entregar Projeto


Isso significa que a proposta é criar um app simples mas funcional, com foco em:

Cadastro de transações
Organização de entradas/saídas
Dashboard simples

após a solicitação foram gerados os arquivos citados inicialmente e o copilot me trouxe o relatório:
linhas

🎉 Pronto! Você tem um APP Web completo
Ele inclui:
✔ Balanço de entradas, saídas e total
✔ Cadastro de transações
✔ Listagem dinâmica
✔ Layout estilo dark/Vibe Coding
✔ Código simples para postar no GitHub Pages



Com base nisso, posso te entregar um web app completo, estilo Vibe Coding, em HTML + CSS + JS (puro), facilmente hospedável em GitHub Pages.


```markdown
# PRD - App de Organização Financeira com Conversa Natural

## Visão Geral
Criar um aplicativo de organização de finanças pessoais que funcione por meio de conversas em linguagem natural.  
O objetivo é tornar o controle financeiro mais intuitivo, acessível e livre de burocracias como planilhas ou formulários complexos.

## Problema a Resolver
Muitas pessoas abandonam o controle financeiro por acharem os aplicativos atuais complicados, exigindo entradas manuais e oferecendo pouca personalização.  
Queremos resolver isso com uma experiência conversacional fluida e recomendações automáticas que se adaptam ao perfil do usuário.

## Público-Alvo
Pessoas que desejam começar a organizar suas finanças de forma prática e sem complicações — especialmente iniciantes que não têm familiaridade com apps financeiros tradicionais.

##
```

---

## 💬 Interações com o Lovable

> A partir dos arquivos enviados desenvolva este projeto;
>analisando arquivos e o projeto, o que pode ser melhorado?
 resposta do Lovable:
 Analisando o projeto, identifiquei estas melhorias principais:

🐛 Bugs/Problemas:

sonner.tsx importa next-themes (não faz sentido num projeto Vite/React — vai quebrar em produção)
Sem tratamento de datas com fuso horário — new Date(t.data) pode gerar datas erradas
🏗️ Arquitetura: 3. Dados no localStorage — frágil, sem backup. Migrar para Lovable Cloud (banco de dados + autenticação) daria persistência real e acesso multi-dispositivo 4. Sem edição de transações — só adiciona e remove 5. Sem paginação na lista — performance degrada com muitas transações

🎨 UI/UX: 6. Sem modo claro (dark-only) — pode incomodar alguns usuários 7. Formulário não dá feedback visual de sucesso (toast) ao adicionar transação 8. Sem gráfico de categorias (pizza/donut) para ver distribuição de gastos 9. Tabela não é responsiva em telas pequenas — poderia virar cards no mobile

📦 Features úteis: 10. Importar JSON (já tem exportar, falta o inverso) 11. Filtro por período de datas na lista 12. Metas/orçamento por categoria

-Quer que eu priorize e implemente algumas dessas melhorias? Posso começar pelas correções de bugs e adicionar toasts + edição de transações, ou prefere focar em outra área?
Respodi que sim, e ordenei a implementção.

> Crie botões na tela principal para as abas

extrato (entradas x saídas) gasto por categorias transações

caso deseje implementar mais botões e funções que julgar pertinente ao projeto, implemente-as!

> adicione filtros a tela "adicionar" com as categorias já cadastradas e sugestões mais comuns de categorias neste tipo de aplicativo

>adicione a opção de ocultar valores e de temas para diferentes públicos

retorno lovable: :

👁️ Ocultar/Mostrar Valores — Botão no header que esconde todos os valores monetários (cards, gráficos, lista) com ••••••. Persiste no localStorage.

🎨 5 Temas Visuais:

🌃 Neon — escuro com cyan (original)
☀️ Claro — clean e minimalista
🌅 Pôr do Sol — tons quentes laranja
🌊 Oceano — azul profundo
🌿 Floresta — verde natural

 >> Créditos esgotados

---

## 🎯 Resultado Final

Acesse o protótipo funcional no Lovable:  
**[financevibe-app] (https://financevibe-app.lovable.app/)**



---

## 🔍 Funcionalidades do App de Organização Financeira

O app possibilita ao usuário registrar suas movimentações financeiras, acompanhar o balanço geral e visualizar a evolução ao longo dos meses através de gráficos interativos.

🚀 Principais Funcionalidades
✔ Cadastro de transações
O usuário pode adicionar transações detalhadas com:

Descrição
Valor
Tipo (Entrada / Saída)
Categoria
Data

✔ Resumo financeiro automático
O app calcula em tempo real:

Total de Entradas
Total de Saídas
Saldo geral

✔ Listagem com filtros inteligentes
A listagem mostra todas as transações com:

Filtragem por tipo
Busca por texto
Ordenação por data

✔ Exclusão de transações
Remoção prática com apenas um clique.
✔ Gráfico interativo (Chart.js)
Um gráfico de barras exibe a comparação entre entradas e saídas nos últimos:

3 meses
6 meses
12 meses

✔ Persistência de dados
Todas as transações são armazenadas automaticamente no localStorage, mantendo os dados mesmo após fechar o navegador.
✔ Exportar e limpar dados

Exportação de todas as transações em JSON
Limpeza completa com confirmação


🎨 Design e Experiência
O layout utiliza:

Glassmorphism para painéis translúcidos
Neon cyan como cor de destaque (estética Vibe Coding)
Sombras suaves, bordas brilhantes e microinterações
Tema escuro com excelente contraste
Responsividade total (desktop, tablet e mobile)


📱 Responsividade
O app foi projetado no conceito mobile-first, garantindo:

Reorganização automática das grades
Redução inteligente de colunas
Interface limpa e fluida até em 360px de largura


---

## 🧠 Reflexão

### O que funcionou bem?  
A base e os arquivos foram desenvolvidos com as iterações com o copilot Web e cosequentemente carregados no lovable .

### O que não funcionou como o esperado?  
limitações nas iterações com o lovable.

### O que aprendi sobre conversar com IAs?  
uma ferramenta que vai além do uso pessoaal, mas algo que pode ser utilizad para desenvolvimento profissional.
