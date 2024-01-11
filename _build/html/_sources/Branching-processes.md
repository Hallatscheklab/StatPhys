---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---


# Branching Processes 

What are general patterns we might expect when a population grows out of a single cell?

One of the most basic question is to characterize how a population grows over time. Deterministically, we expect exponential growth if prolifertion at rate $a$ exceeds the rate $b$ of death. In many cases, both quantities are similar, for example in an epidemic situation where $R_0$ is about 1, or for a slightly beneficial mutaiton in a population going through generations. In these near critical cases, it is not obvious whether a population survives rather than goes extinct by chance and, if it survives, what population size distribution on might expect. 

To answer this question, let's first focus on the probability $u$ that the population survives in the long run.

$$ 
u(t+\epsilon)=\left[1-\epsilon (a+b)\right] u(t)+\epsilon a \left[1-(1-u(t))\right]^2 
$$  (br-process-1)

Here, the first term on the right hand side simply says that, conditional on no death or birth event occurs within the time span $\epsilon$, the probability of survival remains unchanged.

$$ 
\partial_t u = (a-b) u - (a+b) u^2. 
$$

Let's assume $s=a-b\ll1$ and measure time in generation, then this equation reads 
    
$$ 
\partial_t u = s u - 2 u^2. 
$$

This is an example of a
math directive with a
label
```{math}
:label: eq-label

z=\sqrt{x^2+y^2}
```

This is an example of a
math block with a label

$$
z=\sqrt{x^2+y^2}
$$  (mylabel)


```{code-cell}
print(2 + 2)
```

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).
