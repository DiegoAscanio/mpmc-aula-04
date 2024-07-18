## Lógica de Funcionamento para o _Keypad_ sem o uso de bibliotecas

<div class="conteudo small">

- É a segunda etapa do trabalho.
- Sujeito a _ghost keys_ (não tem problema).
- Devem ser usados os resistores _pull-up_ internos do arduino para evitar _bouncing_.

Passos:

1. **Escaneamento das Colunas**: O controlador ativa (ou coloca em nível lógico baixo) uma coluna de cada vez (todas configuradas como saídas).

2. **Leitura das Linhas**:  Enquanto uma coluna está ativa, o controlador lê o estado das linhas (todas configuradas como entradas _pull-up_). Se uma tecla foi pressionada, a linha correspondente estará em nível lógico baixo, indicando que o botão da interseção entre a linha e a coluna foi pressionado.

3. **Processamento**: Com base nas leituras das linhas para cada coluna ativada, o controlador pode determinar exatamente qual botão foi pressionado.

</div>
