# Grade do Perfil

Resumo: você encolhe pro centro da grade do seu perfil com os reels aparecendo em volta e as visualizações em cada um; os reels se empilham atrás da sua cabeça; e a grade enche a parede enquanto um contador sobe.

O visual descrito aqui (cores, fontes, legenda, música) é o **Original do formato**. Se a pessoa escolher outro estilo visual, os efeitos, as posições e o ritmo daqui continuam valendo e a aparência vem do estilo: siga `maquina-de-edicao/referencias/estilos-visuais.md` e a regra de cor de `maquina-de-edicao/referencias/efeitos-de-video.md`.

Formato de efeito: a imagem da câmera sai do `fx.py` original. Siga `maquina-de-edicao/referencias/efeitos-de-video.md` do começo ao fim.

## Como fica

Feito pra quem fala de crescimento no Instagram e mostra o próprio perfil. No gancho, a pessoa encolhe pro quadrado do meio de uma grade 3 × 3 em vidro fosco e os outros oito reels aparecem em volta, um por quadro, cada um com o número de visualizações. Quando a fala fala de quantidade de conteúdo, os reels se empilham atrás da cabeça, um a cada quarto de segundo. Quando a fala traz o resultado, a grade do perfil enche a parede atrás e um card de vidro conta até o número.

## Escolhas que este formato já define

Proporção (vertical 9:16), nível (equivale ao Básico do motor: só câmera cheia, sem gráficos HyperFrames), visual original da legenda (trocado se a pessoa escolher outro estilo visual), capa (quadro da grade já montada), verificação de fontes (desligada).

## Base técnica

- Segue `efeitos-de-video.md`: câmera limpa → plano → conferência por quadros → render do `fx.py` → composição.
- Não vale: layouts B e C, câmera virtual, contato visual obrigatório, gráficos HyperFrames.
- Câmera e efeitos a 30 fps (limite do `fx.py`).

## Entradas extras

- Capas ou prints dos reels da pessoa na pasta `imagens/` (de 8 a 12, retrato). Sem pasta, o `fx.py` usa quadros do próprio vídeo: avise no relatório que a grade fica melhor com as capas de verdade.
- Nome e @ da pessoa (veja "Dados da pessoa" em `efeitos-de-video.md`).
- Visualizações e seguidores só se a pessoa falou ou escreveu. O `place-in-grid` mostra visualizações em todos os quadrados: use só quando ela deu os números (nas observações ou na fala). Sem números, o gancho vira `noise` e o `profile-wall` sai do vídeo.

## Ritmo e corte

- Regras de limpeza do motor.
- Um efeito a cada 8 a 12 s, no máximo 5 por minuto. Entre dois efeitos, pelo menos 2 s de câmera limpa.

## Layouts

Um só: câmera cheia (a câmera limpa com os efeitos do `fx.py`), legenda por cima.

## Direção visual

- Grade, vidro e contadores como no original, em qualquer estilo (é a interface do Instagram).
- Fontes da legenda: Inter 700 e Instrument Serif itálico, locais.

## Gráficos

| Momento da fala | Efeito | Opções | Janela |
|---|---|---|---|
| Gancho, ou "olha o meu perfil" | `place-in-grid` | `images`; `views` = 9 números curtos com `\|` ("1,2M\|840K\|…"), o 9º é o do vídeo atual | 3 a 4 s |
| Quantidade de conteúdo ("postei 100 vídeos", "todo dia") | `noise` | `images`; `size` 0,34 | 2,5 a 3,5 s |
| Resultado em número (seguidores, visualizações) | `profile-wall` | `images`; `count` = o número inteiro (ex: 51000); `label` = o que é ("seguidores", "visualizações"); `name` = @ sem o @; `sub` = de onde é o número ("em 30 dias") | 3,5 a 4 s, terminando na fala do número |

## Legendas

- Inter 700, 58 px, branca, sombra `0 4px 16px rgba(0,0,0,0.7)`.
- De 2 a 3 palavras por bloco, troca seca.
- Centralizada em x, centro em y = 1540.
- Destaque a cada 2–3 blocos: palavra em Instrument Serif itálico, 1,15× o tamanho, rosa Instagram `#FF3D7F`.
- Continua durante `noise`; some durante `place-in-grid` e `profile-wall`.

## Capa e gancho

Quadro 0: o quadro de conferência do efeito do gancho já montado (PNG do `--still`), só no quadro 0, sem título extra.

## Chamada para ação

A de `efeitos-de-video.md`. Neste formato, prefira `tap` (seguir) quando a pessoa pedir pra seguir.

## Áudio

- Música: pop eletrônico leve, 110–120 BPM. ~−24 LUFS.
- Efeitos: impacto abafado no `place-in-grid`, confirmação no fim da contagem do `profile-wall`. Sem riser.

## Saída

`edit/final.mp4`, 1080 × 1920, na taxa de exportação escolhida (a câmera fica a 30 fps), H.264 + AAC 48 kHz.

## Verificação do formato

- Nenhum número inventado nas visualizações nem no contador.
- Nenhum nome ou @ padrão da autora.
- A pessoa na frente dos reels de trás, sem halo de recorte.
