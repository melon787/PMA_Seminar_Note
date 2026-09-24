# PMA Exercises

Exercise statements and solutions based on Walter Rudin's *Principles of Mathematical Analysis*.

## Files

- `main.tex`: Main exercise document.
- `chapters/`: Add exercises and solutions to the corresponding chapter file.
- `preamble.tex`: Packages, theorem environments, and custom commands.
- `build/main.pdf`: Compiled exercise document.

The concept notes are archived separately in `../LaTeX/PMA_Notes/`. This project compiles independently of that folder.

## Build

Use the existing editor workflow, or run from this directory:

```sh
latexmk -pdf -synctex=1 -outdir=build main.tex
```

[View the exercise PDF](build/main.pdf)

## Adding exercises

Continue editing the files in `chapters/`. To add another chapter, create its TeX file there and add its `\input` to `main.tex`.

Enter the book's exercise number directly in the environment. For example, inside Chapter 2:

```tex
\begin{exercise}{20}
Exercise statement.
\end{exercise}

\begin{proof}
Solution.
\end{proof}
```

This displays **Exercise 2.20.** The chapter number comes from the current section. No separate numbering command is needed.

Theorem citations use the manually entered book numbers. Equation and footnote numbers start at 1 and are assigned automatically within this document; use `\label` and `\eqref` for equation references.
