# Máquina de Edição com IA Completo

Este repositório entrega os **seis formatos adicionais** da versão completa. Eles se somam aos seis da versão básica, totalizando 12 formatos.

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

Se o pacote principal ainda não estiver instalado, o instalador avisa e para antes de copiar qualquer skill. Este complemento adiciona somente as seis skills extras, sem substituir o motor nem os seis formatos da oferta principal. Versões anteriores das mesmas skills vão para backup; preferências e estilos pessoais são preservados.

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
