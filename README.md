📊 Dashboard de Absenteísmo — Service Center Campinas
Dashboard interativo de análise de absenteísmo para a operação Service Center Campinas do Mercado Livre. Desenvolvido em HTML puro (sem dependências externas além de Chart.js e Google Fonts), roda diretamente no browser sem necessidade de servidor.


🗂️ Estrutura do Repositório
Absente-smo-SVC/
├── README.md
└── absenteismo_svc_am_wXX.html   ← dashboard da semana (substituir wXX pelo número da semana)


🚀 Como usar
1. Baixar o arquivo
Clique no arquivo .html → botão Download raw file → salve na sua máquina.
2. Abrir no browser
Dê dois cliques no arquivo. Ele abrirá direto no Chrome ou Edge com todos os dados da última semana já carregados.
3. Atualizar os dados semanalmente
Exporte o CSV do sistema (relatório de absenteísmo)
Abra o dashboard no browser
Clique em "Carregar CSV" no canto superior direito
Arraste o arquivo CSV ou clique para selecionar
Os dados atualizam automaticamente ✅

Importante: o CSV deve conter as colunas Nome_Completo, Nome_TL, Empresa, Status_Reporte, Status_Escala, Data_Ops e SUPERVISOR.


🧭 Navegação
O dashboard tem 3 abas principais:

Aba
O que mostra
Geral
KPIs da operação, farol por TL, gráfico de evolução diária. Ao clicar no nome de um TL no farol, aparece o detalhe com ABS por semana, reincidentes e todos os faltantes daquele TL.
Agências
Visão específica dos operadores de agência (Randstad, Adecco, R&T, Actual), com alertas para quem tem ≥ 3 faltas.
Padrões
Identificação automática de padrões suspeitos de falta: repetição no mesmo dia da semana (≥ 3x) e emenda de folga (≥ 3x adjacente ao dia de folga).



🔍 Filtros disponíveis
Todos os filtros funcionam nas 3 abas simultaneamente:

Filtro
Descrição
Mês
Filtra por Março ou Abril (multi-seleção)
Semana
Filtra por semana operacional W14–W18 (Dom→Sáb)
Data da falta
Filtra por datas específicas
Team Leader
Filtra por um ou mais TLs (agrupados por supervisora)
Supervisão
Filtra entre Jaciane Nabor e Priscila Oliveira
Empresa
Filtra por ML, Randstad, Adecco, R&T ou Actual



📐 Lógica de cálculo
ABS (Absenteísmo):

ABS% = (FI + FJ) / Escalonados × 100

Meta: ≤ 5,0%

Tipos de falta:

FI — Falta Injustificada + Abandono
FJ — Atestado, Suspensão, Falecimento, Gestante, Folga Prêmio
Excluídos — INSS, Licença Maternidade, Férias, Feriado, Banco de Horas

Reincidentes: operadores com ≥ 2 faltas no período selecionado.

Padrão de dia da semana: operador que faltou ≥ 3x no mesmo dia da semana.

Emenda de folga: falta ocorrida no dia imediatamente anterior ou posterior ao dia de folga do operador (conforme escala no CSV). ≥ 3 ocorrências = padrão suspeito.

⚠️ Um mesmo dia de falta pode ser contado tanto no padrão de dia da semana quanto na emenda de folga — por isso não some os dois contadores.


🏷️ Semanas operacionais (2026)
Semana
Período
W14
29/03 → 04/04
W15
05/04 → 11/04
W16
12/04 → 18/04
W17
19/04 → 25/04
W18
26/04 → 28/04


A semana operacional começa no Domingo e termina no Sábado.


🔄 Atualização semanal (passo a passo)
Exporte o CSV do período desejado
Renomeie o arquivo HTML da semana anterior (ex: absenteismo_svc_am_w18.html)
Abra no browser e carregue o novo CSV
Verifique se os dados estão corretos
Faça upload da nova versão no GitHub (Add file → Upload files)
Mantenha as versões anteriores para histórico


👩‍💼 Responsáveis
Supervisora
TLs
Jaciane Nabor de Almeida
Claudio, Davi, Elizeu, Everton, Izabela, Mikael, Suelen, Vanessa
Priscila Oliveira
Ariel, Hemily, Regiane, Wanderson



🛠️ Tecnologias
HTML5 + CSS3 + JavaScript — sem framework, roda offline
Chart.js 4.4 — gráfico de evolução diária
Google Fonts — Playfair Display, DM Sans, DM Mono
Dados embutidos — os dados da semana ficam dentro do próprio arquivo HTML; ao carregar um novo CSV, os dados são atualizados em memória



Service Center Campinas · Mercado Livre · 2026

