---
{"dg-publish":true,"permalink":"/misc-research/math-jax-quick-reference/","title":"MathJax Quick Reference (Concise and Clean Edition)","tags":["clips","mathjax","guides","obsidian"],"dgShowInlineTitle":false,"noteIcon":""}
---


# MathJax Quick Reference (Concise and Clean Edition)
2023-02-28
[Source](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)

## FoliathR's Notes
A.k.a _"I-am-probably-too-particular-about-things-that-people-don't-really-care-about Edition"_

In summary, formatting is cleaned up for human reading instead of messy point form. Language has been simplified and made consistent to easily find what is needed.

> [!NOTE]- Changes
> - Each section has a header instead of being points
> - Moved code to start of sentences
> - Removed unnecessary words that extend sentences unnecessarily (eg "To use xxx, use `xxx`" → "xxx: `xxx`")
> - Examples in callouts for easier reading
> - Removed commas around MathJax Examples as they make them much more confusing to read
> - Fixed many formatting inconsistencies and missing formatting
> - New line for each code introduced in each section
> - Smaller clean-up (eg removing spaces between points and text - why even??)

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
`\sum` and `\int`

The subscript is the lower limit and the superscript is the upper limit, so for example `\sum_1^n` $\sum_1^n$. Don't forget `{`…`}` if the limits are more than a single symbol.

> [!EXAMPLE]+ Examples
> `\sum_{i=0}^\infty i^2` is $\sum_{i=0}^\infty i^2$
> `\prod` $\prod$
> `\int` $\int$
> `\bigcup` $\bigcup$
> `\bigcap` $\bigcap$
> `\iint` $\iint$
> `\iiint` $\iiint$
> `\idotsint` $\idotsint$

## Fractions
There are [three ways to make these](https://math.meta.stackexchange.com/questions/12978/should-dfrac-be-edited-in).

1. `\frac ab` applies to the next two groups, and produces $\frac ab$;
2. for more complicated numerators and denominators use `{`…`}`: `\frac{a+1}{b+1}` is $\frac{a+1}{b+1}$. If the numerator and denominator are complicated, you may prefer `\over`, which splits up the group that it is in: `{a+1\over b+1}` is ${a+1\over b+1}$.
3. For continued fractions, [use `\cfrac` instead of `\frac`](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5058#5058).

## Fonts
- "blackboard bold": `\mathbb` or `\Bbb` $\mathbb{CHNQRZ}$.
- boldface: `\mathbf` $\mathbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathbf{abcdefghijklmnopqrstuvwxyz}$
- For expression based characters, use `\boldsymbol` instead: $\boldsymbol{\alpha}$
- Italics: `\mathit` $\mathit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathit{abcdefghijklmnopqrstuvwxyz}$
- Boldfaced italics: `\pmb` $\pmb{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\pmb{abcdefghijklmnopqrstuvwxyz}$
- Typewriter: `\mathtt`$\mathtt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathtt{abcdefghijklmnopqrstuvwxyz}$
- Roman font: `\mathrm` $\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathrm{abcdefghijklmnopqrstuvwxyz}$
- Sans-serif font: `\mathsf` $\mathsf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathsf{abcdefghijklmnopqrstuvwxyz}$
- "calligraphic" letters: `\mathcal` $\mathcal{ ABCDEFGHIJKLMNOPQRSTUVWXYZ}$ (Uppercase only.)
- Script letters: `\mathscr` $\mathscr{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathscr{abcdefghijklmnopqrstuvwxyz}$
- "Fraktur" (old German style) letters: `\mathfrak` $\mathfrak{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\mathfrak{abcdefghijklmnopqrstuvwxyz}$

## Radical Signs / Roots
`sqrt`

Adjusts to the size of its argument.

> [!EXAMPLE]+ Example
> `\sqrt{x^3}` $\sqrt{x^3}$
> `\sqrt[3]{\frac xy}` $\sqrt[3]{\frac xy}$
> For complicated expressions, consider using `{...}^{1/2}` instead.

## Lim, Sin, Max, Ln
Some **special functions** such as "lim", "sin", "max", "ln", and so on are normally set in roman font instead of italic font. Use `\lim`, `\sin`, etc. to make these:
- `\sin x` $\sin x$ (not `sin x` $sin x$)
Use subscripts to attach a notation to `\lim`: `\lim_{x\to 0}`
$$
\lim_{x\to 0}
$$

Nonstandard function names can be set with `\operatorname{foo}(x)` $\operatorname{foo}(x)$.

## Special Symbols and Notations
There are a very large number of **special symbols and notations**, too many to list here; see:
- the short listing [LaTeX and mathcal{A}_{Largemathcal{M}}mathcal{S}-LaTeX Symbols](https://pic.plover.com/MISC/symbols.pdf) prepared by Dr. Emre Sermutlu
- the exhaustive listing [The Comprehensive LaTeX Symbol List](https://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf) by Scott Pakin.

> [!EXAMPE]+ Some common examples
> - `\lt \gt \le \ge \neq`
>   $\lt$, $\gt$, $\le$, $\ge$,$\neq$.
> - `\not` to put a slash through almost anything: `\not\lt` $\not\lt$ but it often looks bad.
>
> - `\times \div \pm \mp`
>   $\times$, $\div$, $\pm$, $\mp$.
> - `\cdot` is a centered dot: $x\cdot y$$x\cdot y$
>
> - `\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing`
>   $\cup$, $\cap$, $\setminus$, $\subset$, $\subseteq$, $\subsetneq$, $\supset$, $\in$, $\notin$, $\emptyset$, $\varnothing$
>
> - `{n+1 \choose 2k}` or `\binom{n+1}{2k}`
>    ${n+1 \choose 2k}$
>
> - `\to \gets \rightarrow \leftarrow \Rightarrow \Leftarrow \mapsto \implies \iff`
>   $\to$, $\gets$, $\rightarrow$, $\leftarrow$, $\Rightarrow$, $\Leftarrow$, $\mapsto$, $\implies$, $\iff$
>
> - `\land \lor \lnot \forall \exists \top \bot \vdash \vDash`
>   $\land$, $\lor$, $\lnot$, $\forall$, $\exists$, $\top$, $\bot$, $\vdash$, $\vDash$
>
> - `\star \ast \oplus \circ \bullet`
>   $\star$, $\ast$, $\oplus$, $\circ$, $\bullet$
>
> - `\approx \sim \simeq \cong \equiv \prec \lhd`
>   $\approx$, $\sim$ , $\simeq$, $\cong$, $\equiv$, $\prec$, $\lhd$
>
> - `\infty \aleph_0`
>   $\infty\, \aleph_0$
>   `\nabla \partial`
>   $\nabla$, $\partial$
>   `\Im \Re`
>   $\Im$, $\Re$
>
> - For modular equivalence, use `\pmod` like this: `a\equiv b\pmod n` $a\equiv b\pmod n$. For the binary mod operator, use `\bmod` like this: `a\bmod 17` $a\bmod 17$.
>
> - Use `\dots` for the triple dots in $a_1, a_2, \dots, a_n$ and $a_1+a_2+\dots+a_n$
>
> - Script lowercase l is `\ell` $\ell$.

## Spaces
MathJax usually decides for itself how to space formulas, using a complex set of rules. Putting extra literal spaces into formulas will not change the amount of space MathJax puts in: `a␣b` and `a␣␣␣␣b` are both $a    b$.

To add more space:
- `\,` for a thin space
  $a\,b$
- `\;` for a wider space
  $a\;b$
- `\quad` and `\qquad` are large spaces:
  $a\quad b$
  $a\qquad b$.

Plain text: `\text{…}`: $\{x\in s\mid x\text{ is extra large}\}$. You can nest `$…$` inside of `\text{…}`, for example to access spaces.

## Accents and Diacritical Marks
`\hat` for a single symbol $\hat x$
`\widehat` for a larger formula $\widehat{xy}$. If you make it too wide, it will look silly.

Similarly, there are:
- `\bar` $\bar x$ and `\overline` $\overline{xyz}$
- `\vec` $\vec x$
- `\overrightarrow` $\overrightarrow{xy}$ and `\overleftrightarrow` $\overleftrightarrow{xy}$.
- Dots: `\dot` and `\ddot` in $\frac d{dx}x\dot x =  \dot x^2 +  x\ddot x$

## Escaping Special Characters
Special characters used for MathJax interpreting can be escaped using the `\` character:
- `\$` $\$$
- `\{` $\{$
- `\}` $\}$
- `\_` $\_$
- `\#` $\#$
- `\&` $\&$

If you want `\` itself, you should use `\backslash` (symbol) or `\setminus` ([binary operation](https://tex.stackexchange.com/questions/511328/difference-between-commands-setminus-and-backslash/511332#511332)) for $\backslash$, because `\\` is for a new line.

# Tool to identify drawn symbol → TeX
[Detexify](https://detexify.kirelabs.org/classify.html) lets you draw a symbol on a web page and then lists the $\TeX$ symbols that seem to resemble it.

These are not guaranteed to work in MathJax, but it's a good place to start. To check that a command is supported, note that MathJax.org maintains a [list of currently supported LaTeX commands](https://docs.mathjax.org/en/latest/input/tex/macros/index.html), and one can also check Dr. Carol JVF Burns's page of [TeX Commands Available in MathJax](https://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm).
