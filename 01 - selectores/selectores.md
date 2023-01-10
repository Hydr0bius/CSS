# Selectores

**Selectores de descendencia**: Elementos que se encuentran dentro de un elemento en particular listando los selectores separados por un espacio. Este tipo de selectores solo afectan a elmenetos dentro de otros elementos, sin importar el lugar que ocupa en la jerarquía. En este ejemplo solo afecta al elemento **< p>**:

```CSS
main p{
    font-size: 10px;
}
```

**Multiples selectores**: Para asignar los mismos estilos a elementos con nombres diferentes, podemos declarar los nombres separados por una coma.

```CSS
p, span{
    fon-size: 10px;
}
```

**CSS** incluye sintaxis adicionales para realizar una selección más precisa utilizando los siguientes caracteres;

"**>**" Para referenciar un elemento que es hijo directo de otro elemento. El carácter > indica que el elemento afectado es el elemento de la derecha cuando tiene compo padre al elemento de la izquierda:

```CSS
section > p{
    font-sizes: 10px;
}
```

"**+**" Referencia un elemento que está por otro elemento. Ambos deben compartir el mismo elemento padre. Al aplicar esta regla, solo se modificará el elemento **< p>** dentro del **< h1>** porque es el único que está predecido por este elemento:

```CSS
h1 + p{
    font-size: 10px;
}
```

**~** Crea un selector que afecta a todos los elementos que se ubican a continuación de otro elemento. Este selector es similar al anterior, pero el elemento afectado no tiene que encontrarse inmediatamente después del primer elemento. Esta regla afecta a todos los elementos encontrados, no solo al primero.

```CSS
p~p{
    fon-size: 10px;
}
```

---
## Atributo Id

Para seleccionar un elemento HTML sin considerar su tipo, se puede usar el atributo **Id**. Para referenciar un elemento usando su atributo **Id**, el selector debe incluir el valor del atributo precedido por el carácter numeral (#).

```CSS
#text{
    font-size: 10px;
}
```

---
## Atributo Class

Este atributo es más flexible y se puede asignar a varios elementos dentro del mismo documento.

```HTML
<p class="texto">Frase 1</p>
<p class="texto">Frase 2</p>
```

```CSS
.texto{
    font-size: 10px;
}
```

A un mismo elemento se le peude asignar varias clases.

---
## otros atributos

La sintaxis para definir esta clase de selectores incluye el nombre del elemento seguido del nombre del atributo en corchetes:

```CSS
p[name]{
    font-size:10px;
}
```

Referenciando elementos **< p>** que tienen un atributo *name* con el valor *texto*:

```CSS
p[name="texto"]{
    fon-size:10px;
}
```

*CSS* nos permite combinar carácter **=** con otros caracteres para realizar una selección más específica.

Referencia cualquier elemento **< p>** con un atributo **name** cuyo valor incluye la palabra "**mi**".

```CSS
p[name~="mi"]{
    font-size:10px;
}
```

Referencia cuanlquier elemento **< p>** con el atributo **name** cuyo valor comienza en "**mi**".

```CSS
p[name^="mi"]{
    font-size:10px;
}
```

Referencia cualquier elemento **< p>** con un atributo **name** cuyo valor termina en "**mi**".

```CSS
p[name$="mi"]{
    font-size:10px;
}
```

Referencia cualquier elemento **< p>** con un atributo **name** cuyo valor contiene la cadena de carecteres "**mi**".

```CSS
p[name*="mi"]{
    font-size:10px;
}
```

---
## Seudoclases

Nos permiten referenciar elementos HTML por medio de sus características, como sus posiciones en el código o sus condiciones actuales.

```HTML
<body>
    <main>
        <section>
            <p>Frase1</P>
            <p>Frase2</P>
            <p>Frase3</P>
            <p>Frase4</P>
        </Section>
    </main>
</body>
```

**:nth-child(valor)**: Esta seudoclase selecciona un elemento de una lista de elementos hermanos que se encuentran en la posición especificada por el valor entre paréntesis.

```CSS
section p:nth-child(2){
    fon-size:10px
    color: #fff;
}
section p:nth-child(3){
    color: #ccc;
}
```

Palabras clave **odd** y **even** para esta seudoclase.

* **odd** Afecta a los elementos que son hijos de otro elemento y tienen un índice impar.

```CSS
p:nth-child(odd){
    font-size:25px;
}
```

* **even** Afecta a aquellos que tienen un índice par.

```CSS
p:nth-child(even){
    font-size:25px;
}
```

**:first-child**: ESta seudoclase selecciona el primer elemento de una lista de elementos hermanos.

```CSS
p:first-child{
    font-size:20px;
}
```

**:last-child**: Esta seudoclase selecciona el último elemento de una lista de elementos hermanos.

```CSS
p:last-child{
    font-size:25px;
}
```

**:only-child**: Esta seudoclase selecciona un elemento cuando es el único hijo de otro elemento.

**:first-of-type**: Esta seudoclase selecciona el primer elemento de una lista de elementos del mismo tipo.

**:not(selector)**: Esta seudoclase selecciona los elementos que no coinciden con el selector entre paréntesis.

```CSS
    /* Aplica estilo a todos los elementos excepto <p> */
:not(p){
    margin: 0px;
}
```

[Volver &ldca;](../README.md)