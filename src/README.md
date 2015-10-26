<!--

WARNING!! DON'T EDIT THE FILE README.md on the root of the project, that one is a GENERATED FILE!

You should just edit the source file at src/README.md - the one which stars with ## @@title 

-->

## @@title

@@description

<img src="img/cover.png" class="logo" />

@@author @ [AvenueCode](http://www.avenuecode.com)

*@@email*

@@date

---

## ReactJS

ReactJS é uma biblioteca Javascript criada inicialmente para resolver problemas no desenvolvimento de funcionalidades do Facebook e Instagram. Assim como BackboneJS, AngularJS, EmberJS, etc, o ReactJS vem se tornando realmente popular nos últimos anos e tem gerado muitas dúvidas e soluções interessantes.

> O ReactJS não é um framework e por isso não pode ser comparado aos exemplos anteriores de maneira total. Eles fora utilizados somente para demonstrar a popularidade comparativa entre eles de acordo com informações atuais da comunidade de desenvolvimento.

Esta simples documentação visa fornecer informações sobre alguns aspéctos estruturais de funcionamento deste relativamente novo e muito eficiente framework.

---

## Componentes

Componentes são a base estrutural da construção usando ReactJS. Podemos pensar em componentes como uma view (ou subview) completa ou como somente um card ou barra de navegação em uma estrutura mais complexa.

Os componentes ReactJS são implementados a partir da declaração de uma "classe", onde alguns métodos são utilizados para controlar sua renderização e seu ciclo de vida. Esta classe é então instanciada e vinculada a uma versão do DOM, denominada Virtual DOM.

Os componentes ReactJS são utilizados como tags normais, incluindo a possibilidade de receber propriedades dos componentes externos através de atributos, assim como qualquer tag HTML padrão.

---

## Uma Analogia Plausível

Mesmo sendo incompatível uma comparação entre o ReactJS e os frameworks listados anteriormente, devido ao primeiro se tratar de uma biblioteca, tecnicamente falando, é ainda possível fazer uma analogia direta:

> É possível dizer que, no contexto da camada de view, o ReactJS é uma união de dois mundos, considerando o BackboneJS e o AngularJS como referência.

Essa conclusão se deve a suas observações importantes:

1. Como no BackboneJS, a ideia de componente se torna bem visível, onde o isolamento do mesmo se dá de forma natural. No BackboneJS, isso é realizado através do atributo `el` do objeto, no ReactJS, de forma implementada internamente pela biblioteca.
2. Como no AngularJS, ao contrário do BackboneJS, as atribuições de ação, são definidas de forma declarativa, no próprio template, não necessitando vincular os elementos da view aos handlers programaticamente, como ocorre no segundo.

---

## Virtual DOM

Como dito antes, o Virtual DOM é uma versão leve da estrutura mantida pelo browser. Sua utilização se deve a uma melhor performance durante o ciclo de vida dos componentes, permitindo uma interação entre eles e o núcleo da biblioteca muito mais rápida do que se houvesse a necessidade de um acesso direto ao DOM, que depende de uma cadeia de acesso muito maior.

---

## Montagem

Com o advento do Virtual DOM, visto que este não é o que está renderizado no browser, mas somente uma representação de tal conteúdo, cria-se a necessidade de se transformar esta representação em uma renderização real. A este processo chamamos de Montagem.

A montagem ocorre com a chamada do método (de implementação obrigátoria) <b>render()</b> do componente em questão. 

Uma curiosidade sobre o método <b>render()</b> é que, mesmo sendo obrigatório na implementação do componente, ele pode retornar <b>null</b>. Nesse caso, o component passará pelo mesmo ciclo de vida da montagem, mas não terá conteúdo exibido no browser. Casos de uso para esse tipo de cenário incluem componentes abstratos como controles de roteamento e mecanismos de gerenciamento de eventos globais.

---

## Ciclo de Vida

O ciclo de vida dos componentes ReactJS seguem quatro cenários básicos:

1. Montagem
2. Alteração de Propriedades
3. Alteração de Estado
4. Desmontagem

---

### Renderização Inicial

<center>
![Renderização Incial](https://drive.google.com/uc?export=download&id=0B7CeDPlZO-G6Z0NabWxDcUgtOTA "Renderização Inicial")
</center>

---

## Alteração de Propriedade(s)

<center>
![Renderização Incial](https://drive.google.com/uc?export=download&id=0B7CeDPlZO-G6TDR5MXJ1YWFjYlE "Alteração de Propriedade(s)")
</center>

---

## Alteração de Estado

<center>
![Renderização Incial](https://drive.google.com/uc?export=download&id=0B7CeDPlZO-G6VldSdVBXNTFHV3c "Alteração de Estado")
</center>

---

## Desmontagem

<center>
![Renderização Incial](https://drive.google.com/uc?export=download&id=0B7CeDPlZO-G6MnVqTTNYRVZTVFk "Desmontagem")
</center>