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
- **Sua carteira**: vencimentos, eventos, pontos críticos e colidências do último relatório de monitoramento.
- **Somente leitura**: as 31 ferramentas apenas consultam.

### O que dá para perguntar

- "O nome Aurora Café já está registrado no INPI para cafeteria?"
- "Quais classes de Nice preciso para abrir uma loja online de cosméticos naturais?"
- "Qual o risco de colidência da marca Vertice na classe 35?"
- "Existem marcas parecidas com Vertice na Europa e nos Estados Unidos?"
- "Quais países mais depositam marcas no Brasil?"
- "Como o TRF2 e o TJSP tratam ações de nulidade de registro de marca?"

### Ferramentas

- **Busca e registro:** `buscar_marcas`, `detalhes_marca`, `obter_logo`, `classificar_atividade`, `classes_de_nice`
- **Risco e viabilidade:** `analisar_colidencia`, `diagnostico_viabilidade`
- **Internacional:** `analise_internacional`, `mercado_por_pais`, `atualizacao_por_pais`, `origem_depositos_brasil`, `ranking_procuradores`, `relacoes_internacionais`
- **Mercado e índice TIQ:** `consultar_indice_tiq`, `valores_de_dimensao`, `ranking_tiq`, `relatorio_de_mercado`
- **RPI:** `rpi_edicoes`, `rpi_resumo`, `rpi_despachos`
- **Judicial e jurisprudência:** `buscar_processos_pi`, `processo_pi`, `estatisticas_juris`, `jurisprudencia_pi`
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
- **Your portfolio**: renewals, events, critical items and the conflicts from your latest monitoring report.
- **Read-only**: all 31 tools only query data.

### What you can ask

- "Is the name Aurora Café already registered at INPI for a coffee shop?"
- "Which Nice classes do I need to open an online store for natural cosmetics?"
- "What is the conflict risk of the mark Vertice in class 35?"
- "Are there marks similar to Vertice in Europe and the United States?"
- "Which countries file the most trademarks in Brazil?"
- "How do the TRF2 and the TJSP treat lawsuits to annul a trademark registration?"

### Tools

- **Search and registration:** `buscar_marcas`, `detalhes_marca`, `obter_logo`, `classificar_atividade`, `classes_de_nice`
- **Risk and viability:** `analisar_colidencia`, `diagnostico_viabilidade`
- **International:** `analise_internacional`, `mercado_por_pais`, `atualizacao_por_pais`, `origem_depositos_brasil`, `ranking_procuradores`, `relacoes_internacionais`
- **Market and TIQ index:** `consultar_indice_tiq`, `valores_de_dimensao`, `ranking_tiq`, `relatorio_de_mercado`
- **Gazette (RPI):** `rpi_edicoes`, `rpi_resumo`, `rpi_despachos`
- **Court cases and case law:** `buscar_processos_pi`, `processo_pi`, `estatisticas_juris`, `jurisprudencia_pi`
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
