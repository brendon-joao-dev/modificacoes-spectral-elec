# Patch do retroarch

Cria atalhos pra funções que melhoram o uso do console

## .config/retroarch/retroarch.cfg
Padrão de caminhos: ~/

## .emulationstation/retroarch/retroarch.cfg
Padrão de caminhos: ~/sdcard/

## minigui/gbx66.cfg
Padrão de caminhos: /sdcard/

## minigui/w10.cfg
Padrão de caminhos: ~/userdata/

### Códigos de cada botão
A: 30
B: 48
X: 45
Y: 21
L: 38
R: 19
L2: 44
R2: 46
Start: 28
Select: 54
D-pad up (cima): 103
D-pad left (esquerda): 105
D pad right (direita): 106
D-pad down (baixo): 108
Analógico L (esquerdo) - cima (X+): +0
Analógico L (esquerdo) - esquerda (Y-): -1
Analógico L (esquerdo) - direita (Y+): +1
Analógico L (esquerdo) - baixo (X-): -0
Analógico R (esquerdo) - cima (X+): +2
Analógico R (esquerdo) - esquerda (Y-): -3
Analógico R (esquerdo) - direita (Y+): +3
Analógico R (esquerdo) - baixo (X-): -2

# Patch do emulationstation

Teste de mais configurações essas pro menu principal do videogame mas pode ser que dependa de binários compilados que não dá pra alterar

## .emulationstation/es_systems.cfg
- Testar melhor, ShowFilenames
- Testar a parada dos arquivos ocultos, ShowHiddenFiles
- Testar icones personalizados ShowManualIcon
- Descobrir onde mostra os savestates ShoSaveStates
- Descobrir sobre recent.sort
- Descobrir como organizar coleções de gênero do sistema
- Descobrir como colocar informações dos jogos 
- Testar ScreenSaverGameInfo 
- Testar TransitionStyle

## .emulationstation/deep_es_settings.cfg
- Testar mais configurações que sejam interessantes

# Patch das capas

Instruções pra adicionar capas pros jogos

# Patch das coleções

Instruções pra ativar e criar coleções de jogos personalizadas

# Patch dos temas

Para análise e futura construção de um tema e modificações dos existentes

# Patch pra "mais videogames"

Ativa o nintendoDS apesar que trava muito e adiciona outros videogames que já existem porém só por baixo dos panos