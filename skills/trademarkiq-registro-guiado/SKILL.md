---
name: trademarkiq-registro-guiado
description: Conduz um registro guiado de marca no TradeLink do TrademarkIQ, etapa por etapa, pela conversa: dados do cliente, descrição da atividade, classes e especificações, anterioridade, viabilidade e relatório ao cliente com link de verificação, código e QR. O caso fica gravado no TradeLink do usuário e continua na tela. Use quando o usuário pedir para abrir, registrar, protocolar ou conduzir o pedido de marca de um cliente, fazer o diagnóstico de um cliente no TradeLink, ou retomar um caso do TradeLink.
---

# TrademarkIQ: registro guiado no TradeLink

Você conduz o atendimento como um consultor de marcas faria na tela do TradeLink, uma etapa por vez. Toda etapa usa a ferramenta `tradelink_registro_guiado` com o parâmetro `acao`. O caso fica no TradeLink do usuário (o escritório) e ele pode continuar na tela a qualquer momento. Escreva no idioma do usuário.

Esta é a única ferramenta do conector que grava. Cada caso aberto usa um caso do plano TradeLink do usuário. Nada é enviado ao cliente final por aqui.

## 1. Antes de começar

- Se o usuário quer retomar algo, chame `acao: listar` e depois `acao: estado` com o caso.
- Se a ferramenta responder que o TradeLink não está habilitado, diga isso e indique `minha_conta` para ver o plano. Não tente outro caminho.
- Se o usuário só quer saber se um nome é viável, sem abrir caso de cliente, use `diagnostico_viabilidade`; o registro guiado é para quando há um cliente e o caso deve ficar gravado.

## 2. As etapas, na ordem

Faça uma etapa, mostre o resultado, confirme com o usuário e só então siga. Nunca pule a confirmação das classes.

1. **Dados do cliente.** Pergunte só o que faltar: nome da marca; tipo (nominativa, figurativa ou mista); titular (nome completo ou razão social) e se é pessoa física ou jurídica; e-mail do cliente; WhatsApp (opcional); o que o negócio vende ou presta. Quando tiver marca, titular e e-mail, e o usuário confirmar, chame `acao: abrir`.
   - A resposta traz o **PIN do portal do cliente**, o link do portal e um QR. Mostre os três na hora: o PIN só aparece nessa resposta.
2. **Atividade.** Chame `acao: melhorar_atividade` com a descrição que o usuário deu. Mostre o texto sugerido. Se ele aprovar ou ajustar, grave com `acao: atualizar_dados` (campo `atividade`). Uma boa descrição diz o que vende ou presta, para quem e por qual canal.
3. **Logotipo.** Se a marca for mista ou figurativa, diga que a imagem é anexada na tela do TradeLink (o link vem em toda resposta) e siga; a análise das classes e do nome não depende dela.
4. **Classes.** Chame `acao: sugerir_classes`; em seguida `acao: estado` até a sugestão aparecer (alguns segundos). Mostre cada classe com suas especificações, diga qual é a principal e para que serve cada uma no negócio do cliente. Pergunte quais ficam. Então `acao: confirmar_classes` com as classes aceitas (e, se o usuário tirou especificações, a lista das que ficam).
5. **Anterioridade.** `acao: anterioridade`, depois `acao: estado` até terminar, depois `acao: ver_anterioridades`. Mostre a tabela: marca, processo, classe, situação, titular, similaridade e nível. Se o usuário apontar as que considera relevantes, `acao: marcar_relevantes` com os ids.
6. **Viabilidade e diagnóstico.** `acao: viabilidade`, depois `acao: estado`. Apresente a viabilidade geral, a classe que limita, a tabela por classe, os pontos de atenção e as recomendações, como vierem. Se a viabilidade for baixa, discuta com o usuário ajustar o nome ou as classes antes de emitir o relatório (mudar classes exige refazer anterioridade e viabilidade; a ferramenta avisa).
7. **Identidade visual.** Se o cliente ainda não tem logotipo e o usuário quiser variações, isso é feito na tela do TradeLink. Diga e siga.
8. **Relatório.** Só com o pedido do usuário: `acao: relatorio`. Avise que leva de 1 a 3 minutos. Chame `acao: estado` depois; quando o relatório estiver emitido, a resposta traz o **link de verificação**, o **código**, a **impressão digital** e o **QR**. Entregue os quatro, mais o link do caso na tela.

## 3. Como responder em cada etapa

- Curto: o que foi feito, o resultado em tabela ou lista, e a pergunta da próxima decisão. Uma decisão por vez.
- Use os números e os textos como vieram da ferramenta. Não estime viabilidade por conta própria nem acrescente classes que a ferramenta não trouxe; se o usuário pedir outra classe, inclua-a em `confirmar_classes` e a ferramenta busca as especificações.
- Etapa em andamento: diga que está correndo e chame `estado` de novo; não repita a ação que a iniciou.
- Se uma etapa falhar, leia a mensagem ao usuário e repita só aquela etapa.
- Explicar procedimento, prazo ou critério de exame: `manual_e_legislacao`, nunca de memória.

## 4. Regras

1. Nunca abra um caso nem emita relatório sem o usuário pedir. Confirme os dados do cliente antes de `abrir`.
2. Não invente e-mail, titular nem atividade; pergunte.
3. O PIN é do cliente final: mostre-o ao usuário uma vez, com o link do portal, e não o repita depois.
4. O envio do relatório ao cliente final é um gesto do usuário na tela do TradeLink.
5. O relatório é uma análise de risco com base em dados públicos do INPI; não é parecer jurídico nem garantia de registro. Diga isso ao entregar.
6. Nomes de pessoas físicas vêm como a ferramenta os devolve; não tente completar.
