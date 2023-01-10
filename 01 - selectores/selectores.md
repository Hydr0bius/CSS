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
    fon-zise: 10px;
}
```

**Atributo Id**

Para seleccionar un elemento HTML sin considerar su tipo, se puede usar el atributo **Id**. Para referenciar un elemento usando su atributo **Id**, el selector debe incluir el valor del atributo precedido por el carácter numeral (#).

```CSS
#text{
    font-zise: 10px;
}
```

**Atributo Class**

Este atributo es más flexible y se puede asignar a varios elementos dentro del mismo documento.

[Volver &ldca;](../README.md)