# Processo de Dispatch de Produto — DiaNorth

Checklist interno para confirmação e envio de pedidos. Nenhuma mensagem ao
cliente é enviada antes de todas as etapas de verificação serem concluídas.

## Fluxo

1. **Confirmar o pedido**
   - Validar dados do pedido (produto, variante, quantidade, endereço).
   - Confirmar que o pagamento foi aprovado.

2. **Verificar estoque**
   - Checar se o item está disponível fisicamente antes de prosseguir.
   - Se não houver estoque: **não enviar mensagem de confirmação**. Contatar
     o cliente informando o prazo de reposição ou oferecer alternativa/estorno.

3. **Inspecionar o produto**
   - Conferir estado do item (sem defeitos, sem avarias na embalagem).
   - Conferir se o item corresponde exatamente ao pedido (modelo, tamanho, cor).
   - Se reprovar na inspeção: separar o item, não despachar, e providenciar substituição.

4. **Enviar mensagem ao cliente**
   - Só depois que as etapas 2 e 3 forem aprovadas.
   - Mensagem confirma o pedido e informa que o produto foi verificado e
     está pronto para envio/despacho.

## Regra de ouro

> Nenhuma mensagem sai antes da verificação de estoque **e** da inspeção do produto.
