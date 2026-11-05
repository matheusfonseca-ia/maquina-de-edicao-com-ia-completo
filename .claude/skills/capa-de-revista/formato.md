# Capa de Revista

Resumo: você vira capa de revista, com o título atrás da cabeça e as chamadas em volta; nas frases de impacto, a imagem fica preto e branco, uma palavra vermelha gigante aparece atrás de você e três frases batem na tela.

O visual descrito aqui (cores, fontes, legenda, música) é o **Original do formato**. Se a pessoa escolher outro estilo visual, os efeitos, as posições e o ritmo daqui continuam valendo e a aparência vem do estilo: siga `maquina-de-edicao/referencias/estilos-visuais.md` e a regra de cor de `maquina-de-edicao/referencias/efeitos-de-video.md`.

Formato de efeito: a imagem da câmera sai do `fx.py` original. Siga `maquina-de-edicao/referencias/efeitos-de-video.md` do começo ao fim.

## Como fica

Visual editorial. No gancho, a pessoa vira a capa: o título da revista em letras vermelhas enormes atrás da cabeça, a linha da edição em cima, as chamadas do lado e o código de barras no canto. No meio do vídeo, a frase mais forte vira colagem: a imagem fica preto e branco, uma palavra vermelha gigante brilha atrás e três frases curtas batem uma depois da outra. No fechamento, uma capa clássica de revista, em serifa elegante e cor quente de filme.

## Escolhas que este formato já define

Proporção (vertical 9:16), nível (equivale ao Básico do motor: só câmera cheia, sem gráficos HyperFrames), visual original da legenda (trocado se a pessoa escolher outro estilo visual), capa (quadro da capa de revista já montado), verificação de fontes (desligada).

## Base técnica

- Segue `efeitos-de-video.md`: câmera limpa → plano → conferência por quadros → render do `fx.py` → composição.
- Não vale: layouts B e C, câmera virtual, contato visual obrigatório, gráficos HyperFrames.
- Câmera e efeitos a 30 fps (limite do `fx.py`).

## Entradas extras

Nome da pessoa ou do perfil pro título da revista (veja "Dados da pessoa" em `efeitos-de-video.md`), quando o título não sair da fala.

## Ritmo e corte

- Regras de limpeza do motor.
- Poucos efeitos e grandes: de 3 a 4 por vídeo de até 60 s, um a cada 12 a 18 s.

## Layouts

Um só: câmera cheia (a câmera limpa com os efeitos do `fx.py`), legenda por cima.

## Direção visual

- No Original do formato: vermelho original (sem `color`) no `cover-star` e no `red-collage`; o `editorial` com a cor original.
- Com outro estilo: `color` = cor de destaque no `cover-star` e no `red-collage`; `accent` = cor de destaque no `editorial`.
- Fontes da legenda: Archivo Black e Instrument Serif itálico, locais.

## Gráficos

| Momento da fala | Efeito | Opções | Janela |
|---|---|---|---|
| Gancho (primeira frase) | `cover-star` | `text` = título curto (nome da pessoa ou a palavra do tema, até 9 letras); `issue` = linha da edição em português ("EDIÇÃO IA · 2026"); `lines` = 3 chamadas curtas da fala com `\|` | 3 a 4 s |
| A frase mais forte do meio | `red-collage` | `text` = a palavra mais forte (até 6 letras); `lines` = 3 frases curtas da fala com `\|` (até 14 caracteres cada); `tag` = "REC · " + tema em caixa alta | 3 a 4 s |
| Fechamento (antes da chamada pra ação) | `cover-star` com `look=editorial` | `text` = título; `issue` = linha da edição; `lines` = 3 linhas com `\|` (a 2ª é a frase de destaque); `right` = 2 linhas com `\|` | 3 a 4 s |
| Vídeo longo (mais de 60 s): uma segunda frase forte | `red-collage` | como acima, outra palavra | 3 a 4 s |

Todos os textos saem da fala, em português. Nunca deixe os padrões ("VIBE", "THE AI ISSUE", "22 effects", "One clip, 42 looks").

## Legendas

- Archivo Black, 54 px, branca, caixa alta, sombra `0 4px 14px rgba(0,0,0,0.7)`.
- De 2 a 3 palavras por bloco, troca seca.
- Centralizada em x, centro em y = 1540.
- Destaque a cada 2–3 blocos: palavra em Instrument Serif itálico (sem caixa alta), 1,2× o tamanho, vermelho `#E82434`.
- Some durante todos os efeitos deste formato.

## Capa e gancho

Quadro 0: o quadro de conferência do `cover-star` do gancho com a capa completa (PNG do `--still`), só no quadro 0, sem título extra.

## Chamada para ação

A de `efeitos-de-video.md` (`comment-box` ou `tap`).

## Áudio

- Música: batida de moda, 95–105 BPM, baixo grave e caixa seca. ~−24 LUFS.
- Efeitos: impacto abafado na entrada de cada capa, impacto em cada frase do `red-collage` (no máximo 3). Sem riser.

## Saída

`edit/final.mp4`, 1080 × 1920, na taxa de exportação escolhida (a câmera fica a 30 fps), H.264 + AAC 48 kHz.

## Verificação do formato

- Título da capa atrás da cabeça, sem cobrir o rosto.
- Nenhum texto padrão da autora nas capas.
- Frases do `red-collage` legíveis e dentro da tela.
