---
{"dg-publish":true,"permalink":"/misc-research/math-jax-quick-reference/","title":"MathJax quick reference","tags":["clips","mathjax","guides","obsidian"],"noteIcon":""}
---


# MathJax basic tutorial and quick reference - Mathematics Meta Stack Exchange
2023-02-28
[Source](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)

## Website Usage

> [!HIDDEN]-
> To see how any formula was written in any question or answer, including this one, right-click on the expression and choose "Show Math As > TeX Commands". (When you do this, the '$' will not display. Make sure you add these: see the next point. There are also [other ways](https://math.meta.stackexchange.com/questions/659/how-to-view-latex-source-of-equations) to view the code for the formula or the whole post.)

## Inline vs Displayed Formulas
### Inline
Enclose the formula in `$`…`$`. 

> [!EXAMPLE]+ Example
> `$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$`  
> 
> to show $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$ as part of the line.

### Displayed and centred
Enclose formula in `$$`…`$$`.

> [!EXAMPLE]+ Example
> `$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$`  
> to show
> $$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$
> which has a line of its own.

## Greek Letters
Lowercase: `\alpha`, `\beta`, …, `\omega`: $\alpha$, $\beta$, …, $\omega$. 
Uppercase: `\Gamma`, `\Delta`, …, `\Omega`: $\Gamma$, $\Delta$, …, $\Omega$. 
Other Greek capital letters: use Latin $A, B, E$, and so on. 
Some Greek letters have variant forms: `\epsilon \varepsilon` $\epsilon$, $\varepsilon$, `\phi \varphi` $\phi$, $\varphi$, and others.

## Superscripts and Subscripts
`^` and `_`. 

Superscript:
`x_i^2` becomes $x_i^2$

Subscript:
`\log_2 x` becomes $\log_2 x$

## Groups
`{…}`
A “group” is either a single symbol, or any formula surrounded by curly braces. 

Superscripts, subscripts, and other operations apply only to the next “group”.

If you do `10^10`, you will get a surprise: $10^10$. But `10^{10}` gives what you probably wanted: $10^{10}$. Use curly braces to delimit a formula to which a superscript or subscript applies.

> [!EXAMPLE]+ Examples
> `x^5^6` → error
> `{x^y}^z` → ${x^y}^z$
> `x^{y^z}` → $x^{y^z}$
> `x_i^2` → $x_i^2$
> `x_{i^2}` → $x_{i^2}$
> `{x_i}^2` → ${x_i}^2$

## Parentheses
Ordinary symbols `()[]` make parentheses and brackets $(2+3)[4+4]$. 
Use `\{` and `\}` for curly braces $\{\}$.

### Scaling Parentheses - `\left(` and `\right)`
Normal parentheses do *not* scale with the formula in between, so if you write 
`(\frac{\sqrt x}{y^3})` the parentheses will be too small: $(\frac{\sqrt x}{y^3})$. Using 
`\left(`…`\right)` will make the sizes adjust automatically to the formula they enclose.

> [!EXAMPLE]+ Example
> `\left(\frac{\sqrt x}{y^3}\right)` 
> 
> $\left(\frac{\sqrt x}{y^3}\right)$

`\left` and`\right` apply to all the following sorts of parentheses: 
- `(` and `)` $(x)$
- `[` and `]` $[x]$
- `\{` and `\}` $\{ x \}$
- `|` $|x|$$|x|$, `\vert` $\vert x \vert$, `\Vert` $\Vert x \Vert$
- `\langle` and `\rangle` $\langle x \rangle$
- `\lceil` and `\rceil` $\lceil x \rceil$, and `\lfloor` and `\rfloor` $\lfloor x \rfloor$. `\middle` can be used to add additional dividers. 

### Invisible parentheses - `.`

> [!EXAMPLE]+ Example:
> `\left.x^2\right\rvert_3^5 = 5^2-3^2`
> 
> $\left.x^2\right\rvert_3^5 = 5^2-3^2$

## Sums and Integrals
**Sums and integrals** `\sum` and `\int`; the subscript is the lower limit and the superscript is the upper limit, so for example `\sum_1^n` $\sum_1^n$$\sum_1^n$. Don't forget `{`…`}` if the limits are more than a single symbol. For example, `\sum_{i=0}^\infty i^2` is $\sum_{i=0}^\infty i^2$$\sum_{i=0}^\infty i^2$. Similarly, `\prod` $\prod$$\prod$, `\int` $\int$$\int$, `\bigcup` $\bigcup$$\bigcup$, `\bigcap` $\bigcap$$\bigcap$, `\iint` $\iint$$\iint$, `\iiint` $\iiint$$\iiint$, `\idotsint` $\idotsint$$\idotsint$.

## Fractions
**Fractions** There are [three ways to make these](https://math.meta.stackexchange.com/questions/12978/should-dfrac-be-edited-in). `\frac ab` applies to the next two groups, and produces $\frac ab$$\frac ab$; for more complicated numerators and denominators use `{`…`}`: `\frac{a+1}{b+1}` is $\frac{a+1}{b+1}$$\frac{a+1}{b+1}$. If the numerator and denominator are complicated, you may prefer `\over`, which splits up the group that it is in: `{a+1\over b+1}` is ${a+1\over b+1}$${a+1\over b+1}$. For continued fractions, [use `\cfrac` instead of `\frac`](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5058#5058).

## Fonts
-   Use `\mathbb` or `\Bbb` for "blackboard bold": $\mathbb{CHNQRZ}$$\mathbb{CHNQRZ}$.
-   Use `\mathbf` for boldface: $\mathbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathbf{abcdefghijklmnopqrstuvwxyz}$$\mathbf{abcdefghijklmnopqrstuvwxyz}$.
-   For expression based characters, use `\boldsymbol` instead: $\boldsymbol{\alpha}$$\boldsymbol{\alpha}$
-   Use `\mathit` for italics: $\mathit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathit{abcdefghijklmnopqrstuvwxyz}$$\mathit{abcdefghijklmnopqrstuvwxyz}$.
-   Use `\pmb` for boldfaced italics: $\pmb{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\pmb{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\pmb{abcdefghijklmnopqrstuvwxyz}$$\pmb{abcdefghijklmnopqrstuvwxyz}$.
-   Use `\mathtt` for "typewriter" font: $\mathtt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathtt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathtt{abcdefghijklmnopqrstuvwxyz}$$\mathtt{abcdefghijklmnopqrstuvwxyz}$.
-   Use `\mathrm` for roman font: $\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathrm{abcdefghijklmnopqrstuvwxyz}$$\mathrm{abcdefghijklmnopqrstuvwxyz}$.
-   Use `\mathsf` for sans-serif font: $\mathsf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathsf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathsf{abcdefghijklmnopqrstuvwxyz}$$\mathsf{abcdefghijklmnopqrstuvwxyz}$.
-   Use `\mathcal` for "calligraphic" letters: $\mathcal{ ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathcal{ ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ (Uppercase only.)
-   Use `\mathscr` for script letters: $\mathscr{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathscr{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathscr{abcdefghijklmnopqrstuvwxyz}$$\mathscr{abcdefghijklmnopqrstuvwxyz}$
-   Use `\mathfrak` for "Fraktur" (old German style) letters: $\mathfrak{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathfrak{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ $\mathfrak{abcdefghijklmnopqrstuvwxyz}$$\mathfrak{abcdefghijklmnopqrstuvwxyz}$.

## Radical Signs / Roots
 **Radical signs / roots** Use `sqrt`, which adjusts to the size of its argument: `\sqrt{x^3}` $\sqrt{x^3}$$\sqrt{x^3}$; `\sqrt[3]{\frac xy}` $\sqrt[3]{\frac xy}$$\sqrt[3]{\frac xy}$. For complicated expressions, consider using `{...}^{1/2}` instead.

## Lim, Sin, Max, Ln
Some **special functions** such as "lim", "sin", "max", "ln", and so on are normally set in roman font instead of italic font. Use `\lim`, `\sin`, etc. to make these: `\sin x` $\sin x$$\sin x$, not `sin x` $sin x$$sin x$. Use subscripts to attach a notation to `\lim`: `\lim_{x\to 0}`

$$
\lim_{x\to 0}
$$

Nonstandard function names can be set with `\operatorname{foo}(x)` $\operatorname{foo}(x)$$\operatorname{foo}(x)$.

## Special Symbols and Notations
There are a very large number of **special symbols and notations**, too many to list here; see the short listing [$\LaTeX$$\LaTeX$ and $\mathcal{A}_{\Large\mathcal{M}}\mathcal{S}$$\mathcal{A}_{\Large\mathcal{M}}\mathcal{S}$\-$\LaTeX$$\LaTeX$ Symbols](https://pic.plover.com/MISC/symbols.pdf) prepared by Dr. Emre Sermutlu, or the exhaustive listing [The Comprehensive $\LaTeX$$\LaTeX$ Symbol List](https://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf) by Scott Pakin. Some of the most common include:


-   `\lt \gt \le \ge \neq` $\lt$$\lt$, $\gt$$\gt$, $\le$$\le$, $\ge$$\ge$,$\neq$$\neq$. You can use `\not` to put a slash through almost anything: `\not\lt` $\not\lt$$\not\lt$ but it often looks bad.

-   `\times \div \pm \mp` $\times$$\times$, $\div$$\div$, $\pm$$\pm$, $\mp$$\mp$. `\cdot` is a centered dot: $x\cdot y$$x\cdot y$

-   `\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing` $\cup$$\cup$, $\cap$$\cap$, $\setminus$$\setminus$, $\subset$$\subset$, $\subseteq$$\subseteq$, $\subsetneq$$\subsetneq$, $\supset$$\supset$, $\in$$\in$, $\notin$$\notin$, $\emptyset$$\emptyset$, $\varnothing$$\varnothing$

-   `{n+1 \choose 2k}` or `\binom{n+1}{2k}` ${n+1 \choose 2k}$${n+1 \choose 2k}$

-   `\to \gets \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto \implies \iff` $\to$$\to$, $\gets$$\gets$, $\rightarrow$$\rightarrow$, $\leftarrow$$\leftarrow$, $\Rightarrow$$\Rightarrow$, $\Leftarrow$$\Leftarrow$, $\mapsto$$\mapsto$, $\implies$$\implies$, $\iff$$\iff$

-   `\land \lor \lnot \forall \exists \top \bot \vdash \vDash` $\land$$\land$, $\lor$$\lor$, $\lnot$$\lnot$, $\forall$$\forall$, $\exists$$\exists$, $\top$$\top$, $\bot$$\bot$, $\vdash$$\vdash$, $\vDash$$\vDash$

-   `\star \ast \oplus \circ \bullet` $\star$$\star$, $\ast$$\ast$, $\oplus$$\oplus$, $\circ$$\circ$, $\bullet$$\bullet$

-   `\approx \sim \simeq \cong \equiv \prec \lhd` $\approx$$\approx$, $\sim$$\sim$ , $\simeq$$\simeq$, $\cong$$\cong$, $\equiv$$\equiv$, $\prec$$\prec$, $\lhd$$\lhd$

-   `\infty \aleph_0` $\infty\, \aleph_0$$\infty\, \aleph_0$ `\nabla \partial` $\nabla$$\nabla$, $\partial$$\partial$ `\Im \Re` $\Im$$\Im$, $\Re$$\Re$

-   For modular equivalence, use `\pmod` like this: `a\equiv b\pmod n` $a\equiv b\pmod n$$a\equiv b\pmod n$. For the binary mod operator, use `\bmod` like this: `a\bmod 17` $a\bmod 17$$a\bmod 17$.

-   Use `\dots` for the triple dots in $a_1, a_2, \dots, a_n$$a_1, a_2, \dots, a_n$ and $a_1+a_2+\dots+a_n$$a_1+a_2+\dots+a_n$

-   Script lowercase l is `\ell` $\ell$$\ell$.

[Detexify](https://detexify.kirelabs.org/classify.html) lets you draw a symbol on a web page and then lists the $\TeX$$\TeX$ symbols that seem to resemble it. These are not guaranteed to work in MathJax, but it's a good place to start. To check that a command is supported, note that MathJax.org maintains a [list of currently supported $\LaTeX$$\LaTeX$ commands](https://docs.mathjax.org/en/latest/input/tex/macros/index.html), and one can also check Dr. Carol JVF Burns's page of [$\TeX$$\TeX$ Commands Available in MathJax](https://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm).

## Spaces
**Spaces** MathJax usually decides for itself how to space formulas, using a complex set of rules. Putting extra literal spaces into formulas will not change the amount of space MathJax puts in: `a␣b` and `a␣␣␣␣b` are both $a    b$$a    b$. To add more space, use `\,` for a thin space $a\,b$$a\,b$; `\;` for a wider space $a\;b$$a\;b$. `\quad` and `\qquad` are large spaces: $a\quad b$$a\quad b$, $a\qquad b$$a\qquad b$.

To set plain text, use `\text{…}`: $\{x\in s\mid x\text{ is extra large}\}$$\{x\in s\mid x\text{ is extra large}\}$. You can nest `$…$` inside of `\text{…}`, for example to access spaces.

## Accents and Diacritical Marks
**Accents and diacritical marks** Use `\hat` for a single symbol $\hat x$$\hat x$, `\widehat` for a larger formula $\widehat{xy}$$\widehat{xy}$. If you make it too wide, it will look silly. Similarly, there are `\bar` $\bar x$$\bar x$ and `\overline` $\overline{xyz}$$\overline{xyz}$, and `\vec` $\vec x$$\vec x$ and `\overrightarrow` $\overrightarrow{xy}$$\overrightarrow{xy}$ and `\overleftrightarrow` $\overleftrightarrow{xy}$$\overleftrightarrow{xy}$. For dots, as in $\frac d{dx}x\dot x =  \dot x^2 +  x\ddot x$$\frac d{dx}x\dot x =  \dot x^2 +  x\ddot x$, use `\dot` and `\ddot`.

## Escaping Special Characters
Special characters used for MathJax interpreting can be escaped using the `\` character: \\$ $\$$$\$$, `\{` $\{$$\{$, `\}` $\}$$\}$, `\_` $\_$$\_$, `\#` $\#$$\#$, `\&` $\&$$\&$. If you want `\` itself, you should use `\backslash` (symbol) or `\setminus` ([binary operation](https://tex.stackexchange.com/questions/511328/difference-between-commands-setminus-and-backslash/511332#511332)) for $\backslash$$\backslash$, because `\\` is for a new line.
