# Addon Bedrock: Cidadão que dorme à noite

Este pacote cria um mob `addon:cidadao` com geometria humanoide (`geometry.humanoid`) e textura do Steve.

## Estrutura

- `behavior_packs/cidadao_sleep_bp`: comportamento (IA, sensores e eventos de dormir).
- `resource_packs/cidadao_sleep_rp`: cliente/render, geometria humanoide e textura Steve.

## Como instalar

1. Copie `cidadao_sleep_bp` para a pasta `behavior_packs` do Minecraft Bedrock.
2. Copie `cidadao_sleep_rp` para a pasta `resource_packs` do Minecraft Bedrock.
3. Ative os dois pacotes no mundo.
4. (Opcional) Ative modo criativo e use:

```mcfunction
/summon addon:cidadao
```

## Como funciona

- O sensor de ambiente dispara evento quando é noite e adiciona `addon:night_sleep`.
- Esse grupo inclui:
  - `minecraft:behavior.move_to_bed`
  - `minecraft:behavior.sleep`
- Quando volta a ser dia, remove o grupo de sono.

## Observação

As APIs de IA podem variar entre versões do Bedrock. Este exemplo foi montado para versões recentes (1.20+). Se sua versão for antiga/preview e algum componente falhar, ajuste os nomes dos goals com base no comportamento vanilla do aldeão.
