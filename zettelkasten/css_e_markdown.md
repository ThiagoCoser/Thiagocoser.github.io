# CSS e Markdown

Utilizando um código html no arquirvio MD, alguns problemas acontecem, como a aplicação ocorrendo apenas quando se converte a página para html e si. Isto foge um puco da própria função do markdonw, em tornar a legibilidade mais clara do corpo do texto. Seguem 2 pequenos testes para customização CSS.

#### Problema 1

<img src="/assets/images/tagscss.jpg" style='height: 100%; width: 100%; object-fit: contain'/>

Senti a necessidade do gráfico criado pelo FOAM possuir um sistema de cores, para assim destacar melhor as tags, os cartões em si e das algumas notas mais relevantes, no caso, os textos maiores de estudo que contém tópicos. Para isso, precisamos editar o .json das configurações do VS Code:

> Ctrl + Shift + P e o comando Open Settings (JSON)

ou

> File > Preferences > Settings (procure o JSON por lá)

Retirado desta documentação, para aplicação do código a seguir:

https://foambubble.github.io/foam/user/features/graph-visualization.html#graph-navigation

```css
/*Formatação para objetos do FOAM Graph*/
 "foam.graph.style": {
        "background": "#202020",
        "fontSize": 15,
        "lineColor": "#277da1",
        "lineWidth": 0.3,
        "node": {
            "note": "#2b8fc5",
            "tag": "#ffffff",
            "feature": "#d0813f",
            "placeholder": "#545454",
        }
    }

```


#### Problema 2

A função de criação automática de uma tabela de conteúdo cria bullets automáticos e a única maneira de modificar isso foi através de um estilo customizado.

### Frutas
1. Banana
2. Maçã
2.2 Verde
2.3 Vermelha
### Legumes

- [CSS e Markdown](#css-e-markdown)
      - [Problema 1](#problema-1)
    - [Frutas](#frutas)
    - [Legumes](#legumes)



```html

<!-- Importa um css externo-->
<link rel="stylesheet" href="assets/css/styles.css" />
```
ou

```html
<!-- Aplica direto na página-->

<style>

Classe do estilo css aqui.


</style>

```

Com isto, podemos poder chamar a classe e aplicar o estilo.
```html
<div class="remove-bullets">

  Objeto a ter estilo aplicado. No caso, a tabela de conteúdos (TOC) gerada automaticamente pelo puglin Markdown All in One.

</div>

```


```css

.remove-bullets ul {
  list-style: none;
    list-style-type: none;

  }

  .remove-bullets ol {
  list-style: none;
    list-style-type: none;

  }

```

 https://getcssscan.com/blog/how-to-remove-bullets-from-li-css
