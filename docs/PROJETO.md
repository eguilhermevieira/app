# Brief do projeto

## Visão
App de comércio local que prioriza estabelecimentos próximos à residência do consumidor em Cacimba de Dentro, Paraíba. Compras podem gerar benefício no posto parceiro. Expansões: central de encomendas em salão disponível e atacado de cerveja para bares.

## Perguntas antes de definir investimento e metas
1. Qual é o orçamento de desenvolvimento, divulgação e capital de giro?
2. Onde fica o posto, quem o opera e como será formalizada sua participação?
3. Qual é o tamanho, aluguel, localização e infraestrutura do salão?
4. Quais comerciantes já confirmaram participação? Quem atualiza preços e estoque?
5. Quais são ticket médio, comissão aceitável, taxas de pagamento e margem por categoria?
6. Quem fará entregas, com qual custo, raio, horários e capacidade?
7. Qual é o público inicial, seus bairros, frequência de compra e uso de celular?
8. Quem financiará os pontos para combustível e como o posto será reembolsado?
9. Como funciona o operador de encomendas existente, seus contratos e volumes?
10. Quais bares têm interesse, volumes, marcas, fornecedores e necessidade de cerveja gelada?
11. Quem administrará e receberá o fundo social? Qual entidade, governança e prestação de contas?
12. O 1% incide sobre produtos, valor total com entrega ou receita da plataforma? Quem suporta o custo?

## Fundo de caridade: requisito proposto, ainda não ativo
Premissa de trabalho para discussão: reservar 1% do valor dos produtos de cada compra concluída, financiado pela plataforma e sem acréscimo ao cliente. Essa base precisa ser confirmada pelos responsáveis. Não confundir a reserva de caridade com o benefício de combustível; são custos distintos.

Exemplo matemático, sem representar tributação ou lançamento contábil:
- Produtos: R$ 100; comissão do app a 6%: R$ 6.
- Benefício de combustível financiado pelo app: R$ 1.
- Reserva de caridade: R$ 1.
- Pagamento/processamento: R$ 1.
- Atendimento e perdas variáveis: R$ 1.
- Contribuição restante: R$ 2 antes de custos fixos e tributos aplicáveis.
Sem a reserva, sobrariam R$ 3. A reserva reduz a contribuição deste exemplo em um terço. Mil pedidos iguais resultariam em R$ 1.000 reservados e R$ 2.000 de contribuição. Comissão de 6% não é receita líquida e depende do contrato.

### Bloqueio e registro operacional
Uma tela mostrando saldo não bloqueia dinheiro. Para implementar de verdade: definir conta/estrutura de segregação e política de movimentação com assessoria contábil/jurídica e instituição de pagamento; não presumir que todo gateway permite split ou retenção para uma entidade social.

Manter um livro de eventos separado com: ID do pedido, valor-base em centavos, percentual, valor reservado, financiador, status do pagamento, data, cancelamentos, estornos, liberações, beneficiário e comprovante de repasse. Tratar arredondamento de modo consistente e conciliar gateway, banco e registros. Reservas não devem ser contadas como lucro disponível. O tratamento contábil e fiscal deve ser definido pelo contador, não por este documento.

Cancelamento, devolução parcial e chargeback precisam ajustar a base e reverter a reserva correspondente. Não realizar repasses sobre pedidos ainda sujeitos à política de liquidação sem prever como financiar reversões. Acesso à movimentação deve ser restrito, autorizado e auditado.

### Comunicação
Somente após implementação e validação: “1% do valor dos produtos deste pedido é destinado ao fundo social da cidade, sem custo adicional para você”, caso essa seja a regra aprovada. Antes disso usar “Proposta de fundo social em desenvolvimento”. Mostrar base de cálculo, responsável, beneficiário, calendário de repasses e relatório de valores reservados e efetivamente repassados. Nunca chamar uma reserva ainda não transferida de doação já entregue. Não prometer benefício fiscal ao cliente.

## Piloto de 12 semanas: estrutura preliminar
Metas finais devem ser definidas após responder às perguntas e calcular a capacidade local.
- Semanas 1–2: entrevistas, acordos com parceiros e desenho operacional. Medir participantes confirmados e demanda observada.
- Semanas 3–4: catálogo, fluxo de compra, regras de entrega e teste supervisionado. Medir sucesso na conclusão sem ajuda, erros e tempo de compra em diferentes idades.
- Semanas 5–8: piloto limitado. Medir pedidos concluídos, faltas de estoque, cancelamentos, pontualidade, contribuição por pedido e custo dos incentivos.
- Semanas 9–12: ajustar e decidir expansão. Medir recompra em 30 dias, custo por comprador, utilização dos pontos, conciliação e contribuição total versus custos fixos.

Não chamar essas etapas de previsão de rentabilidade nem garantir prazo de lançamento.

## Tecnologia necessária para operar e escalar
- Backend e banco de dados: clientes, lojistas, catálogo, estoque, pedidos, itens, pagamentos, agendamentos, entregas, pontos e fundo social.
- Login, permissões por perfil, minimização de dados e política de privacidade.
- Gateway contratado, confirmação por webhook assinado, processamento idempotente, reembolso e conciliação; nunca confiar na tela do cliente para marcar pagamento aprovado.
- Reserva de estoque e capacidade antes de cobrar, expiração da reserva e proteção contra venda simultânea.
- Agenda com capacidade por área/loja/rota; escolha após pagar com tratamento de falta de horário e direito a reembolso.
- Painel de lojista e painel administrativo; importação inicial e futuras integrações com sistemas de estoque.
- Logística com retirada, entrega, rotas, atribuição de entregador e comprovante.
- Razão separado dos pontos e resgate de código de uso único no posto.
- Fundo social com registros imutáveis de eventos, reversões, conciliação e comprovantes.
- Monitoramento, backups, recuperação, suporte e testes reais de acessibilidade.
- Encomendas dependem de contratos e credenciamento; atacado depende de demanda, fornecedores e estrutura aprovada.
