# A cada commit nesse arquivo terá o que foi alterado em cada arquivo e o que isso impacta no sistema
- {+} adição
- {~} modificação
- {-} remoção

## .config/emulationstation/es_settings.cfg

## .config/retroarch/retroarch.cfg
- {~} savestate_auto_index = true
    - Faz o sistema indexar os savestates, ou seja a cada savestate o sistema cria um novo slot se houver espaço invés de substituir
- {~} savestate_auto_load = true
    - Faz o sistema carregar automaticamente os saves ao iniciar os jogos
- {~} savestate_auto_save = true
    - Faz os jogos salvarem automaticamente ao sair de um jogo

## .emularionstation/retroarch/retroarch.cfg
- {~} savestate_auto_index = true
    - Faz o sistema indexar os savestates, ou seja a cada savestate o sistema cria um novo slot se houver espaço invés de substituir
- {~} savestate_auto_load = true
    - Faz o sistema carregar automaticamente os saves ao iniciar os jogos
- {~} savestate_auto_save = true
    - Faz os jogos salvarem automaticamente ao sair de um jogo

## .emulationstation/es_settings.cfg
- {+} bool FavoritesFirst = true
    - Faz com que os favoritos apareçam no topo das listas
- {~} string CollectionSystemsAuto = all,favorites,recent
    - Faz o sistema criar as pastas todos, favoritos e jogados recentes
- {~} string FolderViewMode = always
    - Faz as pastas aparecerem nas galerias de jogos
- {~} string StarupSystem = all
    - Faz o sistema sempre iniciar na galeria todos

.emulationstation/es_systems.cfg
mudei o tipo de economia de bateria (Power saving mode) - string PowerSaverMode
mostrar fps (Show framerate) - bool DrawFramerate
buscar por imagem com mesmo nome da rom (search for local art) - bool LocalArt
(control emulationstation with first joystick only) - bool FirstJoystickOnly
acessar savestates com botão norte e opções do jogo com o sul (acess game options with nort button) - bool GameOptionsAtNorth
mostra sistemas vazio (show empty systems) - bool LoadEmptySystems
ligue (show hidden files) - bool ShowHiddenFiles
(show saveestate manager) - bool ShowSaveStates
screensaver settings - int ScreenSaverTime <!-- aparentemente em milisegundos -->
Procurar pelas coleções de jogos zelda e pokemon - string CollectionSystemCustom <!-- entre as aspas os nomes das coleções -->
ligue (start on gamelist) - bool StartupOnGameList
mostrar pastas com jogos (show folders) - string FolderViewMode = having multiple games
(gamelist view style) - string gamelistViewStyle
bandeira antes do nome (show region flag: no, before name, after name) - string ShowFlags = 1


mudei menu retroarch (retroarch menu driver)
Buscar por opções de preload (preload ui elements on boot e preload metadata media on boot)
(show clock)
ligue (show savestate icon)
(integer scaling)