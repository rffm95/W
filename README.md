# W — O Assalto ao Cofre
Protótipo independente para Cheers O Bar. HTML/CSS/JS sem dependências, sem APIs, sem imagens pesadas. Não altera RF.

## Conceito
Uma hora com 21 packs anunciados, preços fixos e quantidades reais. A TV mostra o cofre a avançar com vendas confirmadas pela equipa. Um minijogo gratuito: parar o cronómetro em 7,77 segundos, sem prémio financeiro ou bebida e sem compra necessária. Não mede rapidez de consumo. Ao alcançar 500 €, emitir até 20 vouchers de 3 € exclusivamente em snacks numa próxima visita, compra mínima de 15 €, validade 14 dias, um por pessoa, sem acumulação. Distribuir aos primeiros 20 interessados presentes, sem sorteio, sem exigir compra nesta sessão. Registar o titular no controlo interno do bar para evitar duplicações; a app não recolhe dados pessoais.

## Cenário de vendas (hipótese)
6 × mesa VIP 55 € = 330 €; 10 × duo 12 € = 120 €; 5 × comida 10 € = 50 €. Total 500 €. Não é previsão nem garantia. Garrafas 70 cl da casa com 10 mixers para grupos; nunca marcas premium a este preço sem custos confirmados. A oferta de comida proposta é 2 tostas mistas + 4 mini pizzas. Packs e receitas carecem de validação local.
Com custos líquidos hipotéticos de 22 €, 3,20 € e 3 € por pack, IVA 23% nos dois packs de bebidas e 13% no pack de comida: receita sem IVA 410,10 €, custo variável 179 €, contribuição 231,10 € antes de pessoal, renda, energia e desconto futuro. Reservando o desconto máximo nominal de 60 €, sobram 171,10 € de contribuição conservadora, não lucro líquido. O IVA de cada pack deve seguir os produtos e regras reais do POS; 13% no pack de comida é apenas hipótese de cálculo. Não misturar preços promocionais de packs com comparações a preços de referência não comprovados.

## Operação
1. Testar stock e capacidade: seis mesas de grupos, 20 cocktails e cinco packs de comida numa hora. Não somar estas vendas à faturação habitual como se fossem inteiramente novas: medir substituição de vendas e contribuição incremental.
2. Abrir index.html, carregar Equipa, introduzir custos líquidos reais e taxas verificadas, confirmar e iniciar. A app recusa packs com contribuição inferior a 45% da receita sem IVA. Este limiar é controlo operacional, não garantia de lucro.
3. Faturar no POS primeiro, registar pack na app uma única vez. Limites 6/10/5; vendas recusadas no fim do relógio. Estoque exibido é local, não sincronizado com POS. Vouchers até 20, com código e expiração, entregar por escrito e controlar resgate no POS.
4. Manter o rato/comando com a equipa. Equipa e TV usam o mesmo dispositivo: não existe painel remoto ou login. LocalStorage conserva a sessão e o prazo após recarregar; exportar JSON no fim. Pausa suspende o tempo e vendas.
5. Jogo gratuito, sem aposta, sem álcool como recompensa. Servir segundo as práticas do bar. Não associar a beber depressa. Versão sem álcool nos duos. Rever enquadramento da campanha antes de utilização pública; o protótipo não fornece validação jurídica.

## Frases de lançamento
TV: «UMA HORA. UMA CASA. UM COFRE.»
Equipa: «Hoje temos o Assalto ao Cofre: packs de mesa durante uma hora. O desafio dos 7,77 é gratuito. Se a casa abrir o cofre, há vantagens para voltar.»
Story: «O cofre do Cheers abre hoje. 60 minutos. Packs para partilhar. Um desafio de precisão. Junta a tua mesa.»
Mostrar contagem e stock reais, sem falsos clientes ou reinícios de urgência. A condição dos vouchers deve ser visível desde o começo.

## GitHub Pages
Criar repositório público W na conta rffm95. Colocar index.html, README.md e .github/workflows/pages.yml na raiz da branch main. Em Settings > Pages escolher GitHub Actions e correr Publish W. Endereço previsto após deploy: https://rffm95.github.io/W/ . Não está publicado automaticamente por este ficheiro.

## Limitações
Dialog, requestAnimationFrame, localStorage e fullscreen devem ser testados no browser real VIDAA. Fullscreen exige gesto e suporte. Sem integração, multi-dispositivo, verificação de titulares, resgate online, som ou telemetria. Registos financeiros são estimativas operacionais e não contabilidade.
