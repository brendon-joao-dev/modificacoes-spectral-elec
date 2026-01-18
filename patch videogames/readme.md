# O que o patch faz?

Ativa o Nintendo DS fazendo uso do core MelonDS (Versão antiga), também dá pra usar o core Desmume. Tentei também usar o core MelonDSDS (versão atual do MelonDS) porém não funcionou. Além disso o patch também adiciona pastas para diversos outros videogames de possível emulação porém q não tinham pastas. *Atenção: O emulador de Nintendo DS até vai abrir os jogos porém de forma travada demais para jogar, não recomendo o uso!*

# Como aplicar?

Basta copiar o conteúdo dessa pasta e colar no cartão de memória onde está seu spectral elec e se divertir!

# O que ainda vou desenvolver?

Ainda vou baixar roms pra cada um dos 92 videogames no total e testar quais funciona e quais não, desabilitando os que não funcionam.

# Mudanças

Com base nos quatro arquivos es_systems.cfg eu criei pastas para cada videogame que eles indicam ser possível emular verificando a presença dos cores no spectral elec (*Testei o Dreamcast porém ele não funciona portanto não está presente*).

Para o Nintendo DS eu criei tags systems em cada um dos quatro arquivos da forma abaixo sendo que o arquivo .emulationstation/es_systems.cfg já possuia e nos demais eu apenas copiei ela mudando a interface que ele usaria de acordo com o arquivo e colocando esses blocos perto do Nintendo 64. A interface é oq vem em na tag "command" antes do nome do core. Caso queira usar o Desmume basta mudar ele pro default ou apagar os outros dois tanto na tag "core" quanto na "command". Já pro melonDSDS caso queira tentar fazer ele funcionar basta baixar o core no site oficial (na versão de linux ou android (Ambas eu testei e não funcionou)) colocar o arquivo do core e o .info dentro da pasta cores do spectral elec e colocar ele como padrão em cada um dos arquivos e/ou apagar os demais da mesma forma q pro desmume.

```
    <system>
		<name>nds</name>
		<fullname>Nintendo DS</fullname>
		<manufacturer>nds</manufacturer>
		<release>2004</release>
		<hardware>portable</hardware>		
		<path>/storage/roms/nds</path>
		<extension>.nds</extension>
		<command>/sdcard/minigui/retroarch -y 12  -c /sdcard/minigui/gbx66.cfg -L /storage/cores/melonds_libretro.so %ROM%</command>
		<command>/sdcard/minigui/retroarch -y 12  -c /sdcard/minigui/gbx66.cfg -L /storage/cores/melondsds_libretro.so %ROM%</command>
		<command>/sdcard/minigui/retroarch -y 12  -c /sdcard/minigui/gbx66.cfg -L /storage/cores/desmume2015_libretro.so %ROM%</command>
		<platform>nds</platform>
		<theme>nds</theme>
		<emulators>
            <emulator name="libretro">
                <cores>
                    <core default="true">melonds</core>
                    <core>melondsds</core>
                    <core>desmume2015</core>
                </cores>
            </emulator>
        </emulators>
	</system>
```