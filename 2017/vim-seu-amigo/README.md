# O VIM é seu amigo e não seu inimigo!

Possívelmente, você possui essa concepção sobre o **VIM**:

![Mólusco VIM](https://pics.onsizzle.com/just-memorize-these-fourteen-contextually-dependant-instructions-exiting-vim-eventually-3125824.png)

Mas espere! O **VIM é seu amigo e não seu inimigo!** Ele não é esse monstro que todos pensam.

Você sempre quis saber como sair do `VIM`? É fácil! Aperte os comandos `Esc` + `:` + `q`. 

**Mas não fique apenas nisso! Vem comigo que é sucesso!**

## Antes de começar... Créditos:

O conteúdo dessa apresentação foi baseado no vídeo da apresentação de Magnun Leno, com o título de **"Grupylango - Vim - mais que um editor"** - URL:  [https://www.youtube.com/watch?v=UUzW46SeLhg](https://www.youtube.com/watch?v=UUzW46SeLhg
).

## Público

- Desenvolvedores (frontend/backend)
- QA's
- e todo mundo que quer aprender! :)

## Objetivo da apresentação/workshop

- Acabar com a ideia "Everybody hates VIM";
- Entender o seu "cerne" e design;
- Acabar com o conceito de i\<digita digita digita>ESC:ws<ENTER>
- Entender que o VIM é o editor DIY (Do It yourself - faça você mesmo).

#### Dica importante:

- **Não tente absorver tudo!**
- O VIM tem que estar nos músculos e não na mente (a famosa memória muscular).

## Tempo previsto
2 horas (reduzindo para 1:40)

## Motivos para usar o VIM

- Onipresente;
- Não exige ambiente gráfico;
- É leve;
- É oldschool (tentar entender depois);
- Suporta inúmeras linguagens;
- Customizável, extensível e escriptável;
- Dependendo do caso, supera até editores atuais (Atom, I'm looking at you!);
- **Saúde:** Sem muitas dores nos braços! Esse lance de mouse + teclado complica. Quem nunca sentiu dor com isso?

## Um pouco de história

- Existiam apenas computadores "centrais".
- Eram utilizados "terminais burros".
- Não era comum o uso de "monitores".
- Os terminais eram lentos!
- O "padrão" de comunicação era a TTY:
  - O Teletypewriter ou Teleprinter - 
    [https://www.youtube.com/watch?v=MikoF6KZjm0](https://www.youtube.com/watch?v=MikoF6KZjm0)
- **1971:** Ken Thompson cria "ed", um line editor.
  - Implementa o conceito de modos.
  - Quem é esse cara?
    - Co-Criador do Unix;
    - Co-criador da linguagem C.
- **1976:** Bill Joy cria "ex", outro line editor.
  - Implementa os comandos mais conhecidos do vi
  - Quem é esse cara?
    - Co-Criador do BSD-Unix;
    - Co-Criador da Sun Microsystems.
  - Bill Joy implementa o comando `:visual` (`:vi`)
    - este modo possibilita abrir o arquivo na linha, e não ele inteiro
- **1979:** A situação se inverte...
- **1991:** Bram Moolenaar cria o **VIM**.

## Vim - Modo Visual

**Aqui, chegamos no momento crucial da apresentação.**

![Morfeu - Pílulas](http://img.hbdia.com/2014/02/morpheus.jpg)

Ou seja...

![Pílulas](http://static.wixstatic.com/media/b44ce6_0a4e3e97f7d6427c8993e0ec9bd10937.jpg)

**Se você decidiu seguir adiante...Bora lá!**

## Breve explicações

**Principais modos:**

- Comando
- Inserção
- Visual
- Normal

Entre outros (mas não iremos abordar)...

- Select
- Insert
- Ex
- Operator-pending
- Replace
- Virtual Replace
- Insert Normal
- Insert Visual
- Insert Select

Por quê desses modos?
  - Bill Joy programava em um ADM-3A terminal.

  ![ADM-3A](http://bytecollector.com/images/DSCF2916.JPG)

  De onde vem a ideia de movimentção por `H`, `J`, `K`, `L`? 

 ![Olhe o teclado!](http://www.vintagecomputer.net/LSI/ADM3A/LSI_ADM3A_21818_keyboard.jpg)

O botão `ESC` era no lugar do `CAPS-LOCK`!

**Por consequência ele é ergonômicamente correto!**

## Considerações dos modos

- Modo normal: Ele é o gateway para todos os modos.
- Modo de inserção é para pequenas incursões no código/texto.

Exemplos de teclas que te levam para o modo de inserção:

- `i` -> insere antes do cursor.
- `I` -> insere no início da linha.
- `o` -> insere uma linha abaixo.
- `O` -> insere uma linha acima.
- `a` -> insere após o cursor.
- `A` -> insere no final da linha.
- `s` -> remove o caractér do cursor e posiciona para escrita.
- `S` -> apaga a linha corrente e posiciona para escrita.
- `C` -> apaga conteúdo do cursor até o fim da linha.

Teclas que te levam ao modo visual:

- `v` -> seleciona a linha inteira andando com o cursor;
- `V` -> seleciona a linha inteira, independentemente do andamento do cursor.
- `Ctrl-v` -> Seleção de bloco -> ao você descer ou subir, dá preferência pela seleção de linhas por onde o cursor está.

Teclas que te levam são gateways para os modos:

- `:`

Qual tecla que te tira de qualquer modo?

- `Esc`

## Movimentação

**Principais**

- `gg` -> início do arquivo.
- `G` -> fim do arquivo.
- `:20` + `<ENTER>` ou `20g` -> pula para a linha.
- `<ctrl-u>` -> Paginação para cima.
- `<ctrl-d>` -> Paginação para baixo.
- `w` -> Pula para o começo da palavra.
- `e` -> Pula para o fim da palavra/próxima palavra.
- `b` -> Pula para o começo para.
- `0` ou `^` -> Pula para o inicio da linha. 
- `$` -> Pula para o fim da linha.

**Outros**

- `{` -> pula para o parágrafo acima.
- `}` -> Pula para o parágrafo abaixo.
- `(` -> pula para a frase acima.
- `)` -> pula para a frase abaixo.
- Ir para porcentagem do arquivo *<numer>%*
- Palavras *w*, *W*, *e*, *E*, *b*, *B* e etc
- Centralizando *zb*, *zt*, *zz*
- Saltos na "página virtual" *H*, *m* e *L*
- Saltos entre classes *[[*, *]]*
- Saltos entre métodos *[m*, *]m*
- Entre pares *%*
- Achar par não "casado" \[(, \[{
- Última inserção *gi*
- Último salto *<Ctrl-o>* e *<ctrl-i>*
- gi - Último item que estava sendo inserido
- Infinitas mais... *:help cursor-motions*

## Conversando com o VIM

Similidade com a linguagem escrita:

- Verbos, substantivos, adjetivos, quantitativos...

<quantitativo><verbo><substantivo><adjetivo>

Exemplos:

- Apague a palavra ( `dw` ).
- apague ao redor chaves ( `da}` ).
- 3 vezes apague a palavra ( `3dw` ).
- apague até > ( `dt>` ).
- apague conteúdo de parênteses > ( `di)` ).
- mude dentro da tag ( `cit` ) !!! // ci} / cit] ci' ci".

### Helpers

- encontrar item na linha:
  - f + conteúdo a procurar na linha.
- Incremento ( <Ctrl-a> ) e decremento ( <Ctrl-i> )
  - Ex:
    - 10 -> `<ctrl-a>` -> 11
- `<ctrl-x><ctrl-n>` -> Autocompletar palavra.
- `<ctrl-x><ctrl-l>` -> Autocompletar linha.
- `<ctrl-x><ctrl-f>` -> Autocompleta com o istema de arquivos.
- `<ctrl-x><ctrl-k>` -> Autocompleta com o dicionário.
- `<ctrl-p>` -> Autocompleta o texto.
- Modo replace:
  - r + nova letra
  - R sobrescreve texto da linha
- `Y` -> copia a linha inteira
- `y` -> copia tudo.
- `u` -> desfaz alterações.
- `<ctrl-r>` -> refaz alterações.
- `J` -> mescla linhas ( útil em listas variáveis por exemplo)
- `V` -> seleciona a linha inteira
- `%` -> match com elementos

## Macros

Vídeo simples de entendimento: [https://www.youtube.com/watch?v=lXrymNTLKdo](https://www.youtube.com/watch?v=lXrymNTLKdo)

- Iniciando uma macro: qa
- Encerrando: q
- Executando: @a
- Possível utilizar macros dentro do find/replace
- [Exemplo](./content/exemplo_macro_regex.md)

## Integração com o terminal

**Exemplos:**

- **Pegar as configurações da placa de rede da máquina?**
 - `<ESC>` + `:r! sudo ifconfig`

ou

- **Pega o hostname e retorna para o VIM:**
 - `<ESC>` + `r!hostname -i`

ou 

- **Só mostra o conteúdo:**
 - `<ESC>` + `! cat /etc/hosts`

## Registradores

`:reg`

## Conteúdo Programático

- *Como escreve nessa tela preta?!* - `Esc + i`: Transcrevendo o mussum ipsum.

- *Putz, sem usar o mouse? Como vejo o resto do texto?!* - **Movimentação**: Movendo-se pelo documento.

- *Alterar palavras deve ser um sufoco!* - **Find/Replace**: Alterando palavras com poucos comandos.

- *Ah meu, não tem uns recursos legais pra melhorar isso aqui não?* - **Plugins:** Deixando o VIM mais poderoso e divertido!

  - *Não tem como eu ver uma lista de arquivos dentro de uma pasta?* - **NERDTree**: a sua resposta para árvores de arquivos.

  - *Poxa, umas abas aqui seria uma boa ehin?* - `Esc + :tabnew`
  
  - *E se eu quiser `splitar` (dividir) a tela, nem tem como né?* - `Esc + :vsp`: divida a tela em quantas partes quiser!

  - *Não tem umas cores/uns temas para isso aqui não?* - **Instalando temas**

- *Tá, aprendi bastante, mas como salva esse trem?!* - **Salvar:** Guardando seus dados em sua máquina.

- *Ok, você me convenceu. Mas não tem uma IDE mais bonita/ou mais atualizada para mexer com o VIM não?* - **Visual Studio Code**: utilizando VIM dentro da IDE's atuais.

- *Ok ok! Já me converti! Não tem uns links/materiais interessantes?!* - **Links úteis**: Continue no lado negro da força!

## Recomendações

**Livros Gratuitos**
- A Bite of VIM
- VIM Cookbook
- VIM Book

**Livros Pagos**
- Learing VI and VIM Editors
- Hacking VIM
- Pratical VIM

**Vídeos**
- VIMCasts
- Derek Wyatt's Videos
- VIMBits

**Sites**
- [Vim Ninjas](http://www.vimninjas.com/)
- [USE VIM](https://medium.com/usevim)
- [VIM Bits](https://github.com/kkuchta/Vimbits)
- [VIM Awesome](http://vimawesome.com/)
- [TIL VIM](http://tilvim.com/)
- [r/vim](https://www.reddit.com/r/vim/)
- [r/vimplugins](https://www.reddit.com/r/vimplugins/)
- [r/vim_magic](https://www.reddit.com/r/vim_magic/)
- [VIM | Stack Overflow](https://stackoverflow.com/questions/tagged/vim)

https://code.google.com/archive/p/vimbook/downloads

https://github.com/shinokada/vimnotes/wiki

https://www.youtube.com/watch?v=aHm36-na4-4

http://stevelosh.com/blog/2011/09/writing-vim-plugins/

.vimrc's

### Plugins

**Recomendação:** Não utilize plugins sem um sistema de plugins!

- [Vundle](https://github.com/VundleVim/Vundle.vim)
- [Pathogen](https://github.com/tpope/vim-pathogen)
- [Neobundle](https://github.com/Shougo/neobundle.vim)
- [Vim-plug](https://github.com/junegunn/vim-plug)

**Úteis**

- Airline
- Emmet-vim
- Syntastic
- UltiSnips
- YouCompleteMe
- NERDTree
- TagBar
- GitGutter
- Rainbow Parenthesis
- Fugitive
- Surround
- Matchit
- Lexima
- Ctrl-P
- EasyMotion
- ZoomWin
- ...

### Games

- [VIM Adventures](https://vim-adventures.com/) (educacional)
- [Matrix](https://github.com/uguu-org/vim-matrix-screensaver)
- [Sokoban](https://github.com/vim-scripts/sokoban.vim) (Jogo de empurrar caixas)
- [Snake](http://www.vimsnake.com/)
- [HJKL](https://github.com/vim-scripts/HJKL) (estilo pacman)
- [FlappyVird](https://github.com/mattn/flappyvird-vim) (na minha máquina não rolou)
- [...](http://www.zillions-of-games.com/Vim.html)
