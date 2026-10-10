# Perto — comércio local de Cacimba de Dentro (PB)

Primeira versão navegável, responsiva e sem dependências. Catálogo ilustrativo, busca, filtros, carrinho, resumo, pagamento simulado e agendamento após pagar. Inclui ampliação de texto, instruções de instalação e histórico local de pedidos de teste.

## Subir no GitHub
1. Descompacte o ZIP.
2. Crie um repositório no GitHub.
3. Envie todos os arquivos e a pasta docs para a raiz do repositório; index.html deve ficar na raiz.
4. Para publicar, em Settings → Pages escolha Deploy from a branch, branch main e pasta / (root).
5. Abra a URL indicada pelo GitHub Pages. HTTPS é necessário para o service worker.

Não exige npm, compilação ou servidor backend. Para executar localmente: `python3 -m http.server 8000` e abra http://localhost:8000.

## Arquivos
- index.html: interface, estilos, catálogo e lógica do protótipo.
- manifest.webmanifest: configuração do app instalável.
- icon.svg: ícone da marca provisória.
- sw.js: service worker mínimo; não implementa uso offline.
- docs/PROJETO.md: escopo, perguntas, fundo social e evolução técnica.
- docs/PROMPT-CLAUDE.md: instrução para colaboração com Claude.

## Limites desta versão
Não recebe pagamentos, não conecta lojas reais e não envia pedidos. Distâncias e horários são ilustrativos. Histórico fica somente no navegador. Estoque é manual e demonstrativo. Benefício e reserva social previstos são calculados separadamente sobre produtos, sem entrega. Conciliação, resgate no posto e bloqueio financeiro do fundo de caridade ainda não estão implementados. Não há bloqueio financeiro real de 1%.

A instalação varia conforme navegador e sistema; o manifesto e o ícone SVG são ponto de partida. Antes do lançamento, gerar ícones PNG adequados, validar instalação em Android/iOS e realizar testes presenciais com crianças e idosos. Não foi realizada inspeção visual em navegador nesta entrega.

## Evolução
Manter o fluxo: escolha → resumo → pagamento → agendamento → confirmação. Antes de qualquer cobrança real, verificar disponibilidade e reservar capacidade de atendimento; permitir escolher o horário depois de pagar sem risco de pagamento sem atendimento. Definir cancelamento e reembolso.

O nome Perto é provisório. Não incluí credenciais nem configurações da hospedagem anterior.
