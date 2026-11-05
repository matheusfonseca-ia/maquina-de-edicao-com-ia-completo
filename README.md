# Máquina de Edição com IA Completo

Este repositório entrega os **dez formatos adicionais** da versão completa. Eles se somam aos dez da versão básica, totalizando 20 formatos.

**Requisito:** instale primeiro a [Máquina de Edição com IA Básico](https://github.com/matheusfonseca-ia/maquina-de-edicao-com-ia-basico).

Este é o complemento da Máquina de Edição. **Instale o pacote principal primeiro.**

| Comando | Como fica |
|---|---|
| `/reels-com-broll` | Cortes rápidos, clipes de apoio e frases-chave empilhadas |
| `/ensaio-visual` | Você recortado com notícias, números e provas visuais |
| `/nuvem-de-imagens` | Grupos de imagens acima da cabeça, com visual editorial |
| `/recorte-com-imagens` | Você na frente de imagens que mudam com a fala |
| `/formato-ranking` | Tier list animada que se preenche conforme as avaliações |
| `/aula-em-tela-dividida` | Documento da aula ao lado da câmera, com entrega em PDF |
| `/widgets-de-vidro` | Widgets de vidro em volta da cabeça e gráficos de vidro subindo |
| `/cards-em-orbita` | Seus posts girando em volta da cabeça, em carrossel 3D ou em leque |
| `/capa-de-revista` | Você vira capa de revista e as frases fortes viram colagem vermelha |
| `/grade-do-perfil` | Você no centro da grade do perfil, com os reels e as visualizações em volta |

## Instalar

Extraia este ZIP inteiro, incluindo a pasta `.claude`, e abra um terminal na pasta extraída.

Windows (PowerShell):

```powershell
powershell -ExecutionPolicy Bypass -File .\instalar.ps1
```

Mac/Linux:

```bash
bash instalar.sh
```

Se o pacote principal, o earshot (os efeitos sonoros) ou o motor de efeitos de vídeo (ambos instalados pelo pacote principal) ainda não estiverem instalados, o instalador avisa e para antes de copiar qualquer skill. Quem instalou o principal antes da chegada do earshot só precisa atualizar o principal (`git pull` e o instalador de novo) e depois rodar este. Este complemento adiciona somente as dez skills extras, sem substituir o motor nem os dez formatos da oferta principal. Widgets de Vidro, Cards em Órbita, Capa de Revista e Grade do Perfil usam os efeitos do [claude-video-effects](https://github.com/Vibha-Ramprakash/claude-video-effects) (Vibha Ramprakash, MIT), que vêm com o motor do pacote principal: quem já tinha o principal precisa atualizá-lo antes (`git pull` e o instalador de novo). Versões anteriores das mesmas skills vão para backup; preferências e estilos pessoais são preservados.

Feche e abra o Claude Code. Na pasta de um vídeo, use `/maquina-de-edicao` ou um dos comandos acima. Os novos formatos aparecem no painel conforme a orientação da gravação. Todos usam os estilos visuais do pacote principal e os que você criou.

Para atualizar, baixe a nova versão deste complemento e rode o instalador novamente.

## Baixar pelo GitHub

```bash
git clone https://github.com/matheusfonseca-ia/maquina-de-edicao-com-ia-completo.git
cd maquina-de-edicao-com-ia-completo
```

Depois execute o instalador do seu sistema conforme as instruções acima. Para atualizar a cópia clonada, rode `git pull` e execute o instalador novamente.

### Enquadramento em todos os vídeos

A Máquina mantém o centro da cabeça da pessoa exatamente no centro horizontal da imagem ou da janela da câmera, em todos os formatos e estilos. Ajusta o enquadramento por tomada e durante movimentos, e verifica a centralização antes da revisão e na exportação final. Essa configuração é automática e também vale ao reutilizar preferências antigas.
