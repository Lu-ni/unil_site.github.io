# Methode Quantitative 1

## Chapitre 1

| Définition | symbole |
| ---------- | ------- |
|            |         |
|            |         |
|            |         |

## Chapitre 2

### Données

Un ensemble $n$ d'éléments qui forme **l'échantillion**. C'est ensemble d'invididu possèdent des caractéristique: **features** ou **variable**

### Types de variables

**Forme tabulaire**

- représentation des variable sous forme de tableau ou $n$ est pour les lignes et $p$ pour les colonnes

**type** 

- **numérique** ou **quantitative** : nombre
- **nominale** ou **catégorielle** : string
- **bimodale** ou **dichotomiques** : bool
- **ordinal** : donne un ordre d'idée sans forcément avoir de relation (toujours,souvent,peu,pas)
- **ouverte** : ni quantitative ni catégorielle := questions ouvertes

**Echelle de quotient** : unité ou les $zéro$ sont semblable et non tronqué (les unité SI) ex. Kelvin

**Echele d'intervalle** : unité défie par une fonction $ax+b$ ou on décalle notre $0$ par $b$. ex le $°C$ ou $°F$

**Echelle absolue ou relative** 

- Absolue : qui ne tolère aucune transformation
- relative : Qui tolère des transformation mais pas la dilatation : l'année 2021 ? d'après quel calendrier ?

**echelle non-linéaire** : suis un autre type de fonction : echele de Richter (séisme)



### indicateurs de tendance centrale

- **moyenne empirique** : noté par une barre $\huge \bar x = \frac{1}{n}\sum_{i=1}^{n} x_i$
- **mode** : voir histogramme
- **médianne** : sépare un ensemble d'élément en 2 : $\huge \frac{\#[a]}{2} = x_{0.5}$

### indicateur de dispertion

indique si les valeurs dans l'échantillion son dispersée ou non.

- **variance empire $s_x^2$** : $\huge var(x)=\boxed{\frac{1}{n}\sum_{i=1}^{n} (x_i-\bar x)²} = \boxed{\overline{(x-\bar x)²}}=\boxed{\overline{x²}-\bar x²}$

```python
def variance(xxx):   
    moyen1 = 0
    for xx in xxx:
        moyen1 += xx*xx       #attention, somme des carré et non pas carré de la somme !!!
    moyen1 = moyen1/len(xxx)
    moyen2 = (sum(xxx)/len(xxx))**2
    return moyen1 - moyen2
```



- **écart type** : $\huge s_x=\sqrt{var(x)}$   : **attention** : s'exprime dans l'unité de $x$
- **entendu** : $x_{max}-x_{min}$
- **intervalle interquartille** : $x_{0.75}-x_{0.25}$
- **intervalle semi-interquartille** : $\frac{x_{0.75}-x_{0.25}}{2}$

### fonctions indicatrices



### fonction de répartition

$\huge{F(x) = \frac{nbr ... observation \le x}{nbr ... observation}=\frac{\#\{x_i|x_i\le x\}}{\#{x_i}=n}}$ 



$\#$ : représente le nombre d'entité dans quelque chose  : $a = [1,2,3]$  : $\#a = 3$

### quantiles

découpage du plot final en "tranche":

- quartile : découpage en 4 : 1,2,3 quartille
- centille : découpage en 100

histograme : le quantile arrive sois dans un mur (on prend le mur) sois un "plateau" (**la on prend la moitié du plateau**)

### histogrammes

chaque bar est une **classe**, le millieu de la plus grande classe est appelé le **mode**

Crée un diagramme en bar pour des valeur **quantitative** (répartition de l'age dans une population)

### barplots

crée un diagramme en bar pour des valeur **catégorielle** (nombre de personnes possédant un chat, chien, péruche )

### boxplots 

<img src="boxplot.png" style="zoom: 50%;" />



**score**:

- centrer : c'est lui enlever le score moyen
- réduire : c'est le diviser par l'écart type
- standardiser : c'est lui enlever le score moyen puis le diviser par l'écart type2
