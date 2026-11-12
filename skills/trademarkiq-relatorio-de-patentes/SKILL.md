---
name: trademarkiq-relatorio-de-patentes
description: Monta o relatório de patentes de uma empresa ou de uma tecnologia com os dados do conector TrademarkIQ: carteira no INPI, situação e prazos de cada pedido, o que as reivindicações protegem e as famílias no exterior. Use quando pedirem relatório de patentes, carteira de patentes de uma empresa, levantamento de uma tecnologia, busca de anterioridade de invenção ou mapa de concorrentes em patentes.
---

# TrademarkIQ: relatório de patentes

Dois usos: a carteira de patentes de uma empresa, ou o levantamento do que existe sobre uma tecnologia. Escreva no idioma do usuário.

## 1. O que perguntar antes (só o que faltar)

Se o foco é uma empresa (nome ou CNPJ) ou uma tecnologia (descrição em uma ou duas frases, com o problema que resolve); só o Brasil ou também o exterior; a finalidade (gestão da carteira, liberdade de operação, anterioridade, concorrência).

## 2. Dados: sempre pelas ferramentas do TrademarkIQ

Carteira de uma empresa:
1. `patentes_empresa` (CNPJ ou nome): os pedidos e patentes, por situação.
2. `detalhes_patente` nos relevantes: título, datas, classificação, inventores, depositante, procurador, situação e despachos.
3. `texto_patente` nos principais: resumo e reivindicações. O que a patente protege é o que as reivindicações dizem, não o título.

Levantamento de uma tecnologia:
1. `buscar_patentes` com termos técnicos e sinônimos; repita com 2 ou 3 formulações diferentes.
2. `detalhes_patente` e `texto_patente` nos resultados próximos.
3. Exterior: `buscar_patentes_internacional` e `patente_internacional` (publicações WO, EP, US, CN, JP e outras).

Desenhos industriais ligados ao produto: `buscar_desenhos`, `detalhes_desenho`, `desenhos_titular`. Litígios: `buscar_processos_pi`.

## 3. Formato (PDF, 3 páginas)

Página 1, retrato: abertura com o título como conclusão ("<Empresa> tem N patentes em vigor e M pedidos em exame; K concentram-se em <área>."); quatro números (em vigor, em exame, arquivadas ou extintas, famílias no exterior); gráfico de depósitos por ano; gráfico de barras por área técnica.

Página 2, os ativos: tabela (título, número, depósito, situação, o que protege em uma linha tirada da reivindicação principal, próximo evento).

Página 3, leitura: o que está protegido e até quando, o que caiu em domínio público no Brasil segundo a situação publicada, onde há família no exterior e pontos a conferir com um especialista.

Visual: páginas de 828 x 1170 px; fundo #f4f5f8; cartões brancos com borda #e1e5ee e cantos de 12 px; navy #1b3a6b; dourado #c28a2d (linha de destaque #e6b85c sobre navy); azul #2f5faa; cinza-azulado #b9c2d6; texto #1d2433 e secundário #5d667a. Fontes: Inter no texto, DejaVu Serif em títulos e números. Cabeçalho com o logotipo do TrademarkIQ à esquerda e, à direita, "Em parceria com <escritório>" quando houver. Abertura em bloco navy: linha pequena em caixa alta e dourada, título em serifa escrito como conclusão, e uma linha com o escopo e a data.

## 4. Regras

1. Logotipo: use sempre o logotipo oficial, nunca um desenho próprio nem o nome em texto. Com esta skill instalada, os arquivos estão em `assets/` (`trademarkiq-logo-fundo-claro.png` para fundo branco ou claro, `trademarkiq-logo-fundo-escuro.png` para fundo navy ou escuro, `trademarkiq-icone.png`); copie-os para o diretório de trabalho, porque o ambiente de código não tem rede. Sem a skill, chame `logo_trademarkiq`. Mantenha a proporção, não recolora e não peça o logotipo ao usuário.
2. Endereço: o site é sempre `https://trademarkiq.com.br`. Use só os links que as ferramentas devolvem e cite o número de cada processo.
3. Só entra no relatório o que veio de uma ferramenta. Se um dado não veio, escreva que não está disponível; não estime nem complete de memória.
4. Contagens: todo número de destaque tem de bater com as linhas das tabelas. Se a ferramenta devolveu uma página de um total maior, diga quantos itens existem e quantos estão listados.
5. Uma ferramenta que responde que a área não se aplica à conta, que o plano não a inclui ou que a cota do dia acabou não é falta de dados: omita a seção e diga ao usuário, fora do relatório, o que ficou de fora e por quê.
6. Não explique como as análises são calculadas nem cite fontes internas.
7. Rodapé em todas as páginas: "Fonte: TrademarkIQ (trademarkiq.com.br). Consulta em <data>.", o aviso de que o material usa dados públicos e não é parecer jurídico nem garantia de resultado, e o número da página.
8. Patente arquivada, extinta ou indeferida é uma situação publicada pelo INPI; não conclua que a tecnologia é livre para uso. Membro de família na Europa ou em outro país é um pedido lá, não proteção em vigor.
9. Levantamento de tecnologia não é busca exaustiva nem parecer de patenteabilidade ou de liberdade de operação: o relatório diz quais termos foram buscados e que a conclusão cabe a um especialista em patentes.
10. Descreva o alcance com as palavras das reivindicações; não amplie nem interprete além do texto.
11. Esta skill não fundamenta procedimento de patentes no Manual de Marcas: prazos e etapas de patentes só entram se uma ferramenta os trouxer.

## 5. Construção

HTML com SVG embutido, convertido em PDF por um navegador sem interface, com `@page` em 828 x 1170 px. Antes de entregar, abra as páginas renderizadas e confira: número de páginas, nada cortado pelo rodapé, tabelas sem texto sobreposto, logotipo nítido. Se o usuário pedir só a análise, entregue o mesmo conteúdo em texto, na mesma ordem.
