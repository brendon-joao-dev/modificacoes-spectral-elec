# Patch em desenvolvimento

# O que sei até o momento:

Para cada coleção personalizada você deve criar um arquivo .xcc na pasta .emulationstation/collections com o nome da coleção (é um arquivo de .xml renomeado pra .xcc)

# Tipos de coleções:

## Estáticas: Você define os jogos que vão aparecer um a um.
Para isso dentro de um arquivo xml dentro de uma tag `<gamelist>` você coloca cada jogo dentro de uma tag `<game>` dá seguinte forma:

- `<game>` - Para selecionar um jogo especifíco. Dentro dela devemos ter:
    - `<path>` - Apontando pro caminho do jogo (Caminho).
    - `<name>` - Para o nome de exibição (Texto).

Podendo ter também dentro de game:

- `<desc>` - Para descrição (Texto).
- `<image>` - Para capa (caminho .png).
- `<video>` - Para vídeo (caminho).
- `<marquee>` - Para banners (Caminho).
- `<thumbnail>` - Para miniaturas (Caminho).
- `<rating>` - Para avaliação (de 0.0 a 1.0).
- `<releasedate>` - Para data de lançamento (no modelo: 19910101T000000).
- `<developer>` - Para desenvolvera do jogo (Texto).
- `<publisher>` - Para publicadora do jogo (Texto).
- `<genre>` - Para gêneros (separados por vírgula) (Texto).
- `<players>` - Para número de jogadores (Número).
- `<playcount>` - Para números de vezes que você jogou (Número).
- `<lastplayed>` - Para a última vez q você jogou (no modelo: 20231225T183000).
- `<favorite>` - Para favoritos (true ou false).
- `<kidgame>` - Para jogos infantis (true ou false).
- `<region>` - para região do jogo (Texto).
- `<hash>` - para código hash do jogo (Individual para cada jogo) (Texto).
- `<crc>` - para código crc do jogo (Individual para cada jogo) (Texto).
- `<md5>` - para código md5 do jogo (Individual para cada jogo) (Texto).

## Dinâmicas: Funcionam com base em filtros e são geradas automáticamente.

Para isso dentro de um arquivo xml dentro de uma tag `<filter name="nome-da-coleção">` você coloca cada filtro dentro das seguintes possíveis tags:

*Tags básicas:*

- `<system>` - Para filtrar por sistema (Ex: snes) (Texto).
- `<text>` - Para filtrar por nome (Texto).
- `<text desc="true">` - Para filtrar no nome e na descrição (Texto).
- `<genre>` - Para filtrar por gênero (Texto).
- `<year>` - Para filtrar por ano (Número).
- `<publisher>` - Para filtrar por publicadora (Texto).
- `<developer>` - Para filtrar por desenvolvedora (Texto).
- `<players>` - Para filtrar por players (podendo ser individual como "2" ou um intervalo como "2-4") (Número ou intervalo).
- `<rating>` - Para filtrar por nota mínima (Número entre 0 e 1).
- `<region>` - Para filtrar por região (Texto).
- `<md5>` - Para filtrar por código MD5 (individual para cada jogo) (Texto).
- `<crc>` - Para filtrar por código CRC (individual para cada jogo) (Texto).
- `<favorite>` - Para filtrar jogos favoritos (true ou false).
- `<kidgame>` - para filtrar jogos infantis (true ou false).

*Tags avançadas:*

Para filtragem e ordenação mais complexas nas coleções, recebem os nomes das tags básicas escritas como texto.

- `<group>` - Para agrupar (Tags básicas).
    - firstletter - Agrupa pela primeira letra (Argumento especial de group).

- `<ratinggroup>` - Agrupa por nota (Número de 0 a 5).
- `<sort>` - Para ordenar (Tags básicas).
    - `<sort direction="ascending">` - Ordena em ordem crescente (Tags básicas).
    - `<sort direction="descending">` - Ordena em ordem decrescente (Tags básicas).

- `<limit>` - Limita o número de resultados (Número).

*Tags lógicas:*

- `<not>` - Nega o filtro dentro dela (Tags básicas ou avançadas).
- `<exclude>` - Excluir conteúdo que atender ao filtro dentro dela (Tags básicas ou avançadas).
- `<include>` - Para incluir multiplos filtros (Tags básicas ou avançadas).

*Tags de exibição:*

- `<show>` - O que deve ser mostrado (Tags básicas).
- `<hide>` - O que deve ser escondido (Tags básicas).
- `<layout>` - Como deve ser exibido (Opções: grid, list, detailed).
- `<gridsize>` - Caso o layout seja grid(Opções: small, medium, large).

*Tags para tema específico:*

- `<theme>` - Nome do tema a ser usado (Texto).
- `<textcolor>` - Cor do nome do jogo (Código de cores hexadecimais).
- `<backgroundcolor>` - Cor do fundo (Código de cores hexadecimais).
- `<backgroundimage>` - Imagem de fundo (Caminho).
- `<sound>` - Música para tocar quando na coleção (Caminho).
- `<animation>` - Animação especial para a coleção (Opções: none, fade, slide, slideHorizontal, slideVertical)

*OBS: Por segurança coloca todos os textos dos filtros em capslock (tudo em letra maiúscula) para garantir que o filtro vai pegar letras maiúsculas e minúsculas.*

*OBS2: pra essa palhaçada toda funcionar é preciso ter os metadados dos jogos dentro de um arquivo gamelist.xml dentro da pasta de cada emulador.*

*OBS3: `<ratinggroup>` e `<layout>` podem não funcionar no spectral elec.*

*OBS4: Imagens só funcionam como .png.*

*OBS5: Para as tags `<image>` , `<video>` , `<thumbnail>` e `<marquee>` deve existir uma pasta dentro da pasta de cada emulador com os conteúdos que você quer usar.*

Se todas essa tags não forem o suficiente pra você, você também pode usar códigos REGEX pra filtragem complexa dentro de qualquer tag além de poder criar tags próprias de metadados na gamelist.xml e usar elas pra filtrar dentro dos seus filtros. Se divirta organizando suas coleções de jogos retro!

# Exemplos de filtros:

*Filtrando com e (AND lógico):*

`<genre>action, RPG</genre>`

Jogos de RPG de ação (Tem que ter ambos os gêneros).

*Filtrando com ou (OR lógico):*

```
<genre>action</genre>
<genre>RPG</genre>
```

Jogos de ação ou RPG (Tem que ter pelo menos um dos dois gêneros).

*Agrupamento hierárquico:*

```
<group>system</group>
<group>genero</group>
```

Agrupa por sistema depois por gênero.