# O que o patch faz?

Esse patch altera alguns arquivos do retroarch fazendo o spectral elec armazenar os arquivos de salvamentos dos jogos, savestates e prints em pastas separadas das roms. Além de também configurar alguns atalhos para facilitar a jogabilidade no console e facilitar a vida dos player.

# Como aplicar?

Basta copiar o conteúdo dessa pasta e colar no cartão de memória onde está seu spectral elec e se divertir!

# Mudanças

## Pastas:
Saves - Para salvamentos de jogos
Savestates - Para salvamentos do emulador (savestate)
Screenshots - Para prints

## Atalhos:
Botão para atalhos: L2
Botão para reiniciar o jogo: R2
Botão para pausar: Select
Botão para criar savestate: X
Botão para carregar savestate: Y
Botão para voltar um slot de salvamento: L
Botão para avançar um slot de salvamento: R
Botão para tirar print: A
Botão para acelerar o emulador: B
Botão para acelerar o emulador segurando (fast forward): Start

## *Se quiser mudar algum atalho basta mudar o valor entre aspas na frente dele em ambos os arquivos gbx66.cfg e w10.cfg*

## Sendo as funções e suas variáveis:
- Botão de atalho - input_enable_hotkey_btn
- Reiniciar jogo - input_reset_btn
- Pausar - input_pause_toggle_btn
- Criar savestate - input_save_state_btn
- Carregar savestate - input_load_state_btn
- Voltar slot - input_state_slot_decrease_btn
- Avançar slot - input_state_slot_increase_btn
- Tirar print - input_screenshot_btn
- Acelerar emulador - input_toggle_fast_forward_btn
- Acelerar emulador segurando - input_hold_fast_forward_btn

## Os códigos de cada botão para substituir:
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

# *OBS: Não recomendo usar os analógicos como atalho mas caso queira fazer substitua o valor nas variáveis que acaba com _axis invés de _btn*