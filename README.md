## Emulação do CP 400 Color II no MAME

O CP 400 foi um computador de 8 bits, pra uso doméstico, produzido no Brasil pela Prológica na década de 1980. Era compatível com o TRS-80 Color Computer 2 da Tandy/RadioShack. Outro computador também produzido no Brasil e compatível com o CoCo2 foi o Codimex CD-6809.

A segunda versão, o CP 400 Color II, lançado no final de 1985, possuía como características técnicas um microprocessador Motorola 6809E com estrutura interna de 16 bits e externa de 8 bits, frequência de clock de 1,6 MHz, ROM de 16 Kbytes com programa monitor e interpretador Basic, RAM total de 64 Kbytes e vídeo no modo texto de 16 linhas por 32 colunas e no modo gráfico com resolução de 256x192 pontos.

O CP 400 Color II tinha um teclado com 59 teclas tipo ASCII incorporado ao gabinete, uma saída de RF para ligação a uma TV e saída para monitor de vídeo composto. Além de saídas para joysticks, porta serial, porta para gravador cassete e suportava cartuchos e controlador de disquetes de 5 1/4.

![CP400](img/cp400-caixa.jpg?raw=true)

### Conteúdo deste repositório

:computer: arquivos no formato ROM BIOS, de cada computador;<br />
:floppy_disk: imagens de disquetes, com alguns jogos.

### Como instalar

:point_right: *As instruções deste documento estão exemplificadas para o sistema Linux e partem do pressuposto de que o MAME já esteja instalado.*

Copie os arquivos ROM BIOS para os respectivos diretórios, em `/usr/share/mame/roms/`, de acordo com o computador escolhido:

#### Prológica CP 400 Color II

| Arquivos     | Diretório                     |
| ------------ | ----------------------------- |
| cp400bas.rom | /usr/share/mame/roms/**cp400c2**/ |
| cp400dsk.rom |                               |

#### Tandy Color Computer 2

| Arquivos     | Diretório                   |
| ------------ | --------------------------- |
| bas12.rom    | /usr/share/mame/roms/**coco2**/ |
| disk11.rom   |                             |
| extbas11.rom |                             |

#### Codimex CD-6809

| Arquivos           | Diretório                    |
| ------------------ | ---------------------------- |
| cd6809bas84.rom    | /usr/share/mame/roms/**cd6809**/ |
| cd6809extbas84.rom |                              |
| cd6809dsk.u16      |                              |

### Como iniciar a emulação

#### Prológica CP 400 Color II

`$ mame cp400c2 -window -flop1 disquete.dsk`

#### Tandy Color Computer 2

`$ mame coco2 -window -flop1 disquete.dsk`

#### Codimex CD-6809

`$ mame cd6809 -window -flop1 disquete.dsk`

![Prompt](img/cp400-prompt.gif?raw=true)

:point_right: Carregue dois ou mais disquetes com `-flop1 ... -flop2 ...`

### Ambiente MAME

Na janela de execução do MAME, pressione as teclas para:

**Tab**         -> abrir o menu do MAME;<br />
**Scroll Lock** -> alternar entre modos de emulação.

### Executando um jogo

No prompt do CP 400, digite os seguintes comandos para listar o conteúdo do disquete, carregar um jogo e executar o jogo que está carregado:

`DIR`

`LOADM "CALIXTO.TRD"`

`EXEC`

### Manipulando arquivos no disquete

No prompt do CP 400, use o comando `KILL` para apagar um arquivo do disquete, ex.:

`KILL "SHENANI.BIN"`

No prompt do CP 400, digite os seguintes comandos para listar o conteúdo de cada disquete e use o comando `COPY TO` para copiar um arquivo:

`DIR 0`

`DIR 1`

`COPY "SHENANI.BIN:1" TO "SHENANI.BIN:0"`

### Conteúdo dos disquetes

| :one: | :two: | :three: | 
| ----- | ----- | ------- |
| Pooyan | Joust | Draconia |
| Zaxxon | Quix | Goldrun2 |
| Time Bandit | ColorCar | Shock |
| Donkey King | Cuber | Junior |
| Astro-Blast | Lunar Rover | Mrs Pac |
| Frogger | Trapfall | Marble Maze |
| Cashman | Tut's Tomb |  |
| Galagon | Dinowars |  |

| :four: | :five: | :six: | 
| ------ | ------ | ----- |
| Shenanigans | Module | Gold Runner |
| Trekboer | Crash | Gold Runner II |
| Black Sanctun | Prot | Candy Co |
| Calixto Island | Vortex Factor |  |
| Seaquest |  |  |

### Alguns jogos

![Calixto Island](img/Calixto_Island.jpg?raw=true)

![Donkey King](img/Donkey_King.jpg?raw=true)

![Galagon](img/Galagon.jpg?raw=true)

![Pooyan](img/Pooyan.jpg?raw=true)

![Shock](img/Shock.jpg?raw=true)

![Zaxxon](img/Zaxxon.jpg?raw=true)

![Tut's Tomb](img/Tuts_Tomb.jpg?raw=true)

### Referências

- ADDAIR, P. *Indo além com o CP 400 color*. São Paulo, Editele, 1985.

- ARMANDO *Tirando da caixa um CP 400 Color II da Prológica*. Fevereiro de 2017. Disponível em: <https://forum.fiozera.com.br/t/tirando-da-caixa-um-cp-400-color-ii-da-prologica/88>

- *Datassette: Sua fonte de informações para equipamentos clássicos*. Disponível em: <https://datassette.org/>

- FERREIRA, R. M. *Programas para o CP-400 Color*. 2 de janeiro de 2013. Disponível em: <http://sites.mpc.com.br/ric/cp400/cocomain.htm>

- GREENFIELD, L. *The Tandy Color Computer*. Disponível em: <http://www.nausicaa.net/~lgreenf/cocopage.htm>

- MADEIRA, D. *Emulando o CP 400 no MESS*. Dan Scientia, 7 de agosto de 2011. Disponível em: <http://dan-scientia.blogspot.com/2011/08/emulando-o-cp-400-no-mess.html>

- MIRSHAWKA, V. *Brincando com o TRS-Color*. São Paulo, Nobel, 1985.

- SABBATINI, M. *The Color Computer games review page*. Disponível em: <http://www.icepeople.net/coco/index.html>

- *The Official Site of the MAME Development Team*. Disponível em: <https://www.mamedev.org/>

- *TRS-80 Color Computer Archive*. Disponível em: <https://colorcomputerarchive.com/>

- VALOIS, R. *TRS-Color: Guia de referência*. Rio de Janeiro, Campus, 1986.

- YAKOWENKO, B *Color Computer stuff*. October 5, 2002. Disponível em: <http://www.cs.unc.edu/%7Eyakowenk/coco.html>
