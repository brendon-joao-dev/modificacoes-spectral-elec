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