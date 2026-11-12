# TrademarkIQ Plugin

**Inteligência de marcas do Brasil e do mundo, direto no seu assistente de IA.**
**Trademark intelligence for Brazil and the world, right inside your AI assistant.**

Conector **oficial** do TrademarkIQ, mantido por Ricardo Vinhas, responsável pelo [TrademarkIQ](https://trademarkiq.com.br). / **Official** TrademarkIQ connector, maintained by Ricardo Vinhas, who is responsible for [TrademarkIQ](https://trademarkiq.com.br).

[Português](#português) · [English](#english)

---

## Português

O [TrademarkIQ](https://trademarkiq.com.br) reúne a base completa do INPI, atualizada a cada Revista da Propriedade Industrial (RPI), e uma base internacional com dados de marcas de muitos países. Este plugin liga as duas ao seu assistente via MCP: você pergunta em linguagem natural e recebe números de processo, situação, titulares, datas e links para as fontes oficiais.

### Por que é diferente

- **Base completa do INPI**, com busca fonética e atualização a cada RPI.
- **Base internacional**: Américas, Europa e os registros de Madri, com marcas parecidas, mercado de cada país, mês a mês, e a data até a qual os dados de cada país estão atualizados.
- **Brasil e exterior conectados**: pedidos de estrangeiros no INPI por país de origem e por via de depósito, e quais escritórios brasileiros trabalham com quais escritórios estrangeiros.
- **Risco e viabilidade**: colidência classe a classe, classificação de Nice a partir da descrição do negócio e diagnóstico de viabilidade de registro.
- **Contencioso em todo o Judiciário**: processos de marcas nos 6 TRFs e nos TJs de praticamente todos os estados, além dos tribunais superiores, com estatísticas por tribunal, e a jurisprudência (acórdãos) do STJ e do STF.
- **Patentes e desenhos industriais**: busca, ficha completa, reivindicações e a carteira de qualquer titular, no Brasil e no exterior.
- **Sua carteira, inteira**: na conta de Empresa ou de escritório, representantes, clientes, histórico, financeiro, desenhos, contratos, software, conflitos, ameaças, cobertura internacional e processos judiciais, cada um com a sua franquia por plano. Cada conta vê só o que lhe está atribuído.
- **Somente leitura**: as 61 ferramentas apenas consultam.

### O que dá para perguntar

- "O nome Aurora Café já está registrado no INPI para cafeteria?"
- "Quais classes de Nice preciso para abrir uma loja online de cosméticos naturais?"
- "Qual o risco de colidência da marca Vertice na classe 35?"
- "Existem marcas parecidas com Vertice na Europa e nos Estados Unidos?"
- "Quais países mais depositam marcas no Brasil?"
- "Que desenhos industriais a Ambev depositou em 2025 e em que classes de Locarno?"
- "Quais patentes de baterias de lítio foram concedidas no Brasil e quem as depositou?"
- "Faça um resumo da carteira da minha empresa: marcas, desenhos, software e contratos."
- "Quais clientes do meu escritório têm marcas vencendo nos próximos 90 dias?"
- "Como o TRF2 e o TJSP tratam ações de nulidade de registro de marca?"

### Ferramentas

- **Sua conta:** `minha_conta` (plano, ferramentas disponíveis e consultas restantes hoje, no seu idioma)
- **Logotipo para relatórios:** `logo_trademarkiq` (logotipo oficial do TrademarkIQ, versões para fundo claro, fundo escuro e ícone)
- **Guia de relatório:** `guia_de_relatorio` (como montar o diagnóstico de marca para cliente ou o estudo de mercado: perguntas, ferramentas, formato e regras)
- **Busca e registro:** `buscar_marcas`, `detalhes_marca`, `obter_logo`, `classificar_atividade`, `classes_de_nice`, `presenca_digital`, `manual_e_legislacao`
- **Desenhos industriais:** `buscar_desenhos`, `detalhes_desenho`, `desenhos_titular`
- **Patentes:** `buscar_patentes`, `detalhes_patente`, `texto_patente`, `patentes_empresa`, `buscar_patentes_internacional`, `patente_internacional` (internacionais no plano Enterprise)
- **Risco e viabilidade:** `analisar_colidencia`, `diagnostico_viabilidade`
- **Internacional:** `analise_internacional`, `mercado_por_pais`, `atualizacao_por_pais`, `origem_depositos_brasil`, `ranking_procuradores`, `relacoes_internacionais`
- **Mercado e índice TIQ:** `consultar_indice_tiq`, `valores_de_dimensao`, `ranking_tiq`, `relatorio_de_mercado`
- **RPI:** `rpi_edicoes`, `rpi_resumo`, `rpi_despachos`
- **Judicial e jurisprudência:** `buscar_processos_pi`, `processo_pi`, `estatisticas_juris`, `jurisprudencia_pi`
- **Carteira de Empresa e escritório (a carteira inteira):** `carteira_representantes`, `carteira_clientes`, `carteira_historico`, `carteira_financeiro`, `carteira_desenhos`, `carteira_contratos`, `carteira_software`, `carteira_conflitos`, `carteira_ameacas`, `carteira_internacional`, `carteira_judicial`
- **Negócio do escritório (CRM ligado à conta):** `crm_resumo`, `crm_funil`, `crm_servicos`, `crm_equipe`, `crm_oportunidades`
- **Carteira da conta conectada:** `meu_portfolio`, `resumo_portfolio`, `eventos_portfolio`, `criticos_portfolio`, `vencimentos_portfolio`, `colidencias_ultima_rpi`, `contencioso_portfolio`

### Aviso

As análises são de risco, com base em dados públicos, e não constituem parecer jurídico nem garantia de registro ou de indeferimento.

---

## English

[TrademarkIQ](https://trademarkiq.com.br) combines the complete database of the Brazilian Patent and Trademark Office (INPI), updated with every issue of the official gazette (RPI), with an international trademark database covering many countries. This plugin connects both to your AI assistant through MCP: ask in plain language and get application numbers, status, owners, dates and links to the official sources.

### Why it is different

- **The complete INPI database**, with phonetic search, refreshed with every gazette issue.
- **An international database**: the Americas, Europe and the Madrid System registers, with similar marks, each country's market month by month, and the date up to which each country's data is current.
- **Brazil and abroad, connected**: foreign filings at INPI by country of origin and filing route, and which Brazilian firms work with which foreign firms.
- **Risk and viability**: class-by-class conflict analysis, Nice classification from a business description and a registration viability diagnosis.
- **Litigation across the whole judiciary**: trademark lawsuits from all six federal regional courts (TRFs) and the state courts of justice (TJs) of practically every state, plus the superior courts, with statistics by court, and the case law (rulings) of the STJ and STF.
- **Patents and industrial designs**: search, full record, claims and the portfolio of any holder, in Brazil and abroad.
- **Your whole portfolio**: on a Company or firm account, representatives, clients, history, financial, designs, contracts, software, conflicts, threats, international coverage and court cases, each with its own daily allowance per plan. Each account sees only what is assigned to it.
- **Read-only**: all 61 tools only query data.

### What you can ask

- "Is the name Aurora Café already registered at INPI for a coffee shop?"
- "Which Nice classes do I need to open an online store for natural cosmetics?"
- "What is the conflict risk of the mark Vertice in class 35?"
- "Are there marks similar to Vertice in Europe and the United States?"
- "Which countries file the most trademarks in Brazil?"
- "Which industrial designs did Ambev file in 2025, and in which Locarno classes?"
- "Which lithium battery patents have been granted in Brazil, and who filed them?"
- "Summarise my company's portfolio: trademarks, designs, software and contracts."
- "Which of my firm's clients have marks expiring in the next 90 days?"
- "How do the TRF2 and the TJSP treat lawsuits to annul a trademark registration?"

### Tools

- **Your account:** `minha_conta` (plan, available tools and calls left today, in your language)
- **Logo for reports:** `logo_trademarkiq` (official TrademarkIQ logo, light-background, dark-background and icon versions)
- **Report guide:** `guia_de_relatorio` (how to build the trademark diagnosis for a client or the market study: questions, tools, layout and rules)
- **Search and registration:** `buscar_marcas`, `detalhes_marca`, `obter_logo`, `classificar_atividade`, `classes_de_nice`, `presenca_digital`, `manual_e_legislacao`
- **Industrial designs:** `buscar_desenhos`, `detalhes_desenho`, `desenhos_titular`
- **Patents:** `buscar_patentes`, `detalhes_patente`, `texto_patente`, `patentes_empresa`, `buscar_patentes_internacional`, `patente_internacional` (international ones on the Enterprise plan)
- **Risk and viability:** `analisar_colidencia`, `diagnostico_viabilidade`
- **International:** `analise_internacional`, `mercado_por_pais`, `atualizacao_por_pais`, `origem_depositos_brasil`, `ranking_procuradores`, `relacoes_internacionais`
- **Market and TIQ index:** `consultar_indice_tiq`, `valores_de_dimensao`, `ranking_tiq`, `relatorio_de_mercado`
- **Gazette (RPI):** `rpi_edicoes`, `rpi_resumo`, `rpi_despachos`
- **Court cases and case law:** `buscar_processos_pi`, `processo_pi`, `estatisticas_juris`, `jurisprudencia_pi`
- **Company and firm portfolio (the whole portfolio):** `carteira_representantes`, `carteira_clientes`, `carteira_historico`, `carteira_financeiro`, `carteira_desenhos`, `carteira_contratos`, `carteira_software`, `carteira_conflitos`, `carteira_ameacas`, `carteira_internacional`, `carteira_judicial`
- **Firm business (CRM linked to the account):** `crm_resumo`, `crm_funil`, `crm_servicos`, `crm_equipe`, `crm_oportunidades`
- **Connected account's portfolio:** `meu_portfolio`, `resumo_portfolio`, `eventos_portfolio`, `criticos_portfolio`, `vencimentos_portfolio`, `colidencias_ultima_rpi`, `contencioso_portfolio`

Tool names are in Portuguese; the assistant answers in your language.

### Disclaimer

Analyses are risk assessments based on public data. They are not legal advice nor a guarantee that a mark will be registered or refused.

---

## MCP server / Servidor MCP

- URL: `https://mcp.trademarkiq.com.br`
- Transport / Transporte: streamable HTTP
- Auth / Autenticação: OAuth with a TrademarkIQ account (dynamic client registration accepted)

```json
{
  "mcpServers": {
    "trademarkiq": {
      "type": "streamable-http",
      "url": "https://mcp.trademarkiq.com.br"
    }
  }
}
```

The manifest is in [`plugin.json`](plugin.json) and the server config in [`mcp.json`](mcp.json).

## Licença / License

Os arquivos deste repositório (manifestos, configuração e documentação) são distribuídos sob a [licença MIT](LICENSE). A licença **não** se estende ao serviço TrademarkIQ, às bases de dados nem ao acesso à API, que seguem os próprios termos e exigem autenticação com uma conta TrademarkIQ.

The files in this repository (manifests, configuration and documentation) are distributed under the [MIT license](LICENSE). The license does **not** extend to the TrademarkIQ service, its databases or API access, which are governed by their own terms and require authentication with a TrademarkIQ account.

## Links

- Website: https://trademarkiq.com.br
- Support / Suporte: https://trademarkiq.com.br/contato
- Privacy / Privacidade: https://trademarkiq.com.br/politica-de-privacidade
- Terms / Termos de uso: https://trademarkiq.com.br/termos-de-uso

## Skills de relatório / Report skills

A pasta `skills/` traz duas skills prontas, com o logotipo oficial em `assets/`:

- `trademarkiq-diagnostico-de-marca`: relatório de diagnóstico de viabilidade de uma marca para cliente, no Brasil ou noutro país (PDF de 3 páginas).
- `trademarkiq-estudo-de-mercado`: estudo de mercado de marcas em uma página (país, setor, classe, América Latina, escritórios).

Em assistentes que aceitam skills (por exemplo o Claude), instale a pasta da skill ou o respectivo ZIP. Nos demais, o conector entrega o mesmo conteúdo pela ferramenta `guia_de_relatorio` e o logotipo por `logo_trademarkiq`.

The `skills/` folder ships two ready-made skills, with the official logo in `assets/`: a trademark viability diagnosis report for a client (Brazil or any other country) and a one-page trademark market study. In assistants that support skills (Claude, for example), install the skill folder or its ZIP. Elsewhere, the connector serves the same content through the `guia_de_relatorio` tool and the logo through `logo_trademarkiq`.
