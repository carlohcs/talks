# O VIM é seu amigo e não seu inimigo!

Você sempre quis saber como sair do `VIM`? É fácil! Aperte os comandos `Esc + : + q`. Mas vai ficar só nisso? Vem conosco que é sucesso!

*Conteúdo baseado em: https://www.youtube.com/watch?v=UUzW46SeLhg*

## Público:

- Desenvolvedores (frontend/backend)
- QA's
- Outros (todo mundo que quer aprender!)

## Objetivo do workshop

- Acabar com a ideia "Everybody hates VIM";
- Entender o seu "cerne" e design;
- Acabar com o conceito de i\<digita digita digita>ESC:ws<ENTER>
- Entender que o VIM é o editor DIY (Do It yourself - faça você mesmo);
- Não tente absorver tudo!
- VIM tem que estar nos músculos, e não na mente (a memória muscular)

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
- Sem muitas dores nos braços! Ess lance de mouse + teclado complica. Quem nunca sentiu dor disso?

## Um pouco de história

- Existiam apenas computadores "centrais"
- Eram utilizados "terminais burros"
- Não era comum o uso de "monitores"
- Os terminais eram lentos!
- O "padrão" de comunicação era a TTY:
  - O Teletypewriter ou Teleprinter (imagem!)
    [https://www.youtube.com/watch?v=MikoF6KZjm0](https://www.youtube.com/watch?v=MikoF6KZjm0)
- **1971:** Ken Thompson cria "ed", um line editor
  - Implementa o conceito de modos
  - Quem?
    - Co-Criador do Unix
    - Co-criador da linguagem C
- **1976:** Bill Joy cria "ex", outro line editor
  - Implementa os comandos mais conhecidos do vi
  - Quem?
    - Co-Criador do BSD-Unix
    - Co-Criador da Sun Microsystems
  - Bill Joy implementa o comando `:visual` (`:vi`)
    - este modo possibilita abrir o arquivo na linha, e não ele inteiro
- **1979:** a situação se inverte...
- **1991:** Bram Moolenaar cria o VIM

Vim - Modo Visual

- Aqui, chegamos no momento que não é possível mais voltar.

- Pílula Azul - você pode sair e desistir e pensar que tudo isso aqui foi um sonho.

- Pílula vermelha - você pode entrar na toca do coelho, e conhecer uma gama de conteúdos incríveis.

## Breve explicações

**Principais modos:**

- Comando
- Inserção
- Normal

Mas...

- Visual
- Select
- Insert
- Ex
- Operator-pending
- Replace
- Virtual Replace
- Insert Normal
- Insert Visual
- Insert Select

Por quê?
  - Bill Joy programava em um ADM-3A terminal.

  ![ADM-3A](http://bytecollector.com/images/DSCF2916.JPG)

  De onde vem a ideia de `H`, `J`, `K`, `L`
 ![Olhe o teclado!](http://www.vintagecomputer.net/LSI/ADM3A/LSI_ADM3A_21818_keyboard.jpg)

O botão ESC era no lugar do CAPS-LOCK!

Por consequência ele é ergonômicamente correto!
  - Keep yout damn hands in the home row

## Itens-chave

- Modo normal: Ele é o gateway para todos os modos.

- Modo de inserção é para pequenas incursões no código/texto.

Exemplos de teclas que te levam para o modo de inserção:
- `i` e `I`
- `o` e `O`
- `a` e `A`
- `s` e `S`
- `C`

Teclas que te levam ao modo visual:

- `v`, `V`, `Ctrl-v`

Telcas que te levam ao modo de comando:

- `:`

Qual tecla que te tira de qualquer modo?

- `Esc`

## Movimentação

ctrl + d - paginação pra baixo

ctrl + u - paginação pra cima

gg = início do arquivo

G = fim do arquivo

:20 + ENTER ou 20g

{} - Pular parágrafos

() - Pular frases

w e e - Pular palavras

-> # Se Movimentando no VIM <-

Paginação *gg* e *G*

Paginação *<ctrl-u>* e *<ctrl-d>*

Ir diretamente para número de linha *<numer>G*

Ir para porcentagem do arquivo *<numer>%*

Parágrafos *{* e *}*

Frases *(* e *)*

Palavras *w*, *W*, *e*, *E*, *b*, *B* e etc

Inicio e fim de linha *0*, *$* e *^*

Centralizando *zb*, *zt*, *zz*

Saltos na "página virtual" *H*, *m* e *L*

Saltos entre classes *[[*, *]]*

Saltos entre métodos *[m*, *]m*

Entre pares *%*

Achar par não "casado" \[(, \[{

Última inserção *gi*

Último salto *<Ctrl-o>* e *<ctrl-i>*

gi - Último item que estava sendo inserido

Infinitas mais... *:help cursor-motions*

## Conversando com o VIM

Similidade com a linguagem escrita

- Verbos, substantivos, adjetivos, quantitativos...

<quantitativo><verbo><substantivo><adjetivo>

Ex:

- Apague a palavra ( `dw` )
- apague ao redor chaves ( `da}` )
- 3 vezes apague a palavra ( `3dw` )
- apague até > ( `dt>` )
- apague conteúdo de parênteses > ( `di)` )
- mude dentro da tag ( `cit` ) !!! // ci} / cit] ci' ci"
- encontrar item na linha:
  - f + conteúdo a procurar na linha

- Modo replace:
  - r + nova letra
  - R sobrescreve texto da linha

- Y - copia a linha inteira
- y copia tudo 

- u desfaz alterações
- ctrl + r - refaz alterações

- J - mescla linhas ( útil em listas variáveis por exemplo)
- V - seleciona a linha inteira
- % - match com elementos

- incremento:
  - Ex:
    - 10 -> ctrl + a -> 11

- Macros

[https://www.youtube.com/watch?v=lXrymNTLKdo](https://www.youtube.com/watch?v=lXrymNTLKdo)
  - iniciando uma macro: qa
  - encerrando: q
  - executando: @a

Incremento ( <Ctrl-a> ) e decremento ( <Ctrl-i> )
Autocompletar palavra ( <ctrl-x><ctrl-n> )
Autocompletar linha ( <ctrl-x><ctrl-l> )
Autocompletar Sistema de Arquivos ( <ctrl-x><ctrl-f> )
Autocompletar dicionário ( <ctrl-x><ctrl-k> )

Autocompletar: ctrl + p

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
