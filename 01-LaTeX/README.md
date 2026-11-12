
# 01 | LaTeX

> **The art of creating beautifully structured documents.**

---

## 01. First, What Is LaTeX?

LaTeX (pronounced *LAY-tech*) is a document preparation system used to create professional documents with consistent formatting.

Unlike a word processor, where you directly format text, LaTeX uses commands to define the structure and appearance of a document.

**Where is it used?**

- Academic reports and research papers
- Mathematical and scientific documents
- Books, articles and technical manuals
- Assignments and project reports

## 02. How Does It Work?

A LaTeX document is written in a `.tex` file. A compiler processes the source and generates a formatted document, usually a PDF.

```text
Write LaTeX code (.tex)
          |
          v
   LaTeX Compiler
          |
          v
   Formatted PDF
```

## 🧭 How LaTeX Works

LaTeX follows a simple process to turn your written content into a professionally formatted document.

1. **Write your content:** Create a `.tex` file and add your text.
2. **Add commands and formatting:** Use LaTeX commands to structure headings, format text, insert images, and write equations.
3. **Compile the file:** Process your `.tex` file using a LaTeX compiler such as `pdflatex`.
4. **Generate the PDF:** The compiler converts your source code into a formatted PDF document.
5. **View and share:** Open the final PDF, review the output, and share your document.

## 03. Anatomy of a LaTeX Document

A basic LaTeX document has two main parts:

- **Preamble:** Document class, packages, title and other settings.
- **Document body:** The actual content of the document.

### Your First LaTeX Document

```latex
\documentclass{article}
\usepackage{amsmath}

\title{My First LaTeX Document}
\author{Student}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}

Welcome to the world of LaTeX!

\section{Mathematics}

\[
E = mc^2
\]

\end{document}
```

## 04. Essential Commands

| Command | Purpose |
|---|---|
| `\documentclass{article}` | Defines document type |
| `\usepackage{...}` | Loads a package |
| `\begin{document}` | Starts document body |
| `\end{document}` | Ends document body |
| `\title{...}` | Defines title |
| `\author{...}` | Defines author |
| `\maketitle` | Displays title |
| `\section{...}` | Creates a section |
| `\subsection{...}` | Creates a subsection |
| `\textbf{...}` | Makes text bold |
| `\textit{...}` | Makes text italic |
| `\underline{...}` | Underlines text |

## 05. Formatting and Lists

**Text formatting**

```latex
\textbf{Bold text}

\textit{Italic text}

\underline{Underlined text}
```

**Bulleted list**

```latex
\begin{itemize}
    \item First point
    \item Second point
    \item Third point
\end{itemize}
```

**Numbered list**

```latex
\begin{enumerate}
    \item First step
    \item Second step
    \item Third step
\end{enumerate}
```

## 06. Mathematical Expressions

Mathematical typesetting is one of LaTeX's strongest features.

| Expression | LaTeX syntax |
|---|---|
| \(a^2\) | `a^2` |
| \(\frac{a}{b}\) | `\frac{a}{b}` |
| \(\sqrt{x}\) | `\sqrt{x}` |
| \(\sum_{i=1}^{n}i\) | `\sum_{i=1}^{n}i` |
| \(\alpha,\beta,\gamma\) | `\alpha,\beta,\gamma` |

**Example: Quadratic formula**

```latex
\[
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
\]
```

Inline mathematics uses `$...$`, while displayed mathematics can use `\[...\]`.

## 07. Creating Tables

```latex
\begin{center}
\begin{tabular}{|c|c|}
\hline
Subject & Marks \\
\hline
Mathematics & 90 \\
Physics & 85 \\
Computer Science & 95 \\
\hline
\end{tabular}
\end{center}
```

| Symbol | Meaning |
|---|---|
| `c` | Center alignment |
| `l` | Left alignment |
| `r` | Right alignment |
| `&` | Separates columns |
| `\\` | Ends a row |
| `\hline` | Adds a horizontal line |

## 08. Packages: Extending LaTeX

Packages provide additional functionality.

| Package | Use |
|---|---|
| `amsmath` | Advanced mathematical expressions |
| `graphicx` | Inserting images |
| `geometry` | Adjusting page margins |
| `hyperref` | Adding clickable links |
| `xcolor` | Adding colours |

Example:

```latex
\usepackage{graphicx}
\usepackage[margin=1in]{geometry}
```

## 09. Working with Colours in LaTeX

LaTeX allows you to add colours to text, headings, backgrounds, and other elements using the `xcolor` package.

### Import the Package

Add this command in the preamble:

```latex
\usepackage{xcolor}
```

### Basic Colour Commands

| Command | Purpose |
|---|---|
| `\textcolor{red}{Text}` | Changes the colour of specific text. |
| `\color{blue}` | Changes the colour of subsequent text. |
| `\colorbox{yellow}{Text}` | Adds a coloured background behind text. |
| `\pagecolor{gray}` | Changes the page background colour. |
| `\fcolorbox{red}{yellow}{Text}` | Adds a coloured border and background. |

### Using Custom Colours

You can define your own colours using RGB values.

```latex
\definecolor{myblue}{RGB}{23,35,59}
\definecolor{mylavender}{RGB}{117,103,181}
\definecolor{mygold}{RGB}{181,139,73}
```

Use your custom colours like this:

```latex
\textcolor{myblue}{Technical Writing}

\textcolor{mylavender}{Beautiful Documents}

\colorbox{mygold}{Important Note}
```

### Complete Example

```latex
\documentclass{article}
\usepackage{xcolor}

\definecolor{myblue}{RGB}{23,35,59}
\definecolor{mylavender}{RGB}{117,103,181}

\begin{document}

\textcolor{myblue}{\Huge Technical Writing}

\textcolor{mylavender}{Learning LaTeX}

\colorbox{yellow}{Important Information}

\end{document}
```

**Tip:** Use colours consistently to highlight important information and make documents visually appealing.


## 10. Adding Pictures and Graphics in LaTeX

LaTeX allows you to insert images, diagrams, charts, and other graphical elements into your documents. The `graphicx` package is commonly used for adding external images.

### Import the Package

Add this command in the preamble:

```latex
\usepackage{graphicx}
```

### Basic Image Insertion

Use the `\includegraphics` command:

```latex
\includegraphics{image.png}
```

Make sure the image is stored in the same folder as your `.tex` file, or provide its relative path.

### Adjusting Image Size

You can control the appearance of an image using different options:

| Command | Purpose |
|---|---|
| `width=0.5\textwidth` | Sets image width to half the text width. |
| `height=5cm` | Sets image height to 5 cm. |
| `scale=0.5` | Reduces image size to half. |
| `angle=45` | Rotates the image by 45 degrees. |
| `keepaspectratio` | Maintains the original image proportions. |

### Adding an Image with a Caption and Label

Use the `figure` environment to insert an image with a caption and reference label.

```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\textwidth]{image.png}
    \caption{Example of an inserted image}
    \label{fig:example}
\end{figure}
```

- `\centering` aligns the image in the centre.
- `\caption{}` adds a caption below the image.
- `\label{}` assigns a reference name to the figure.

### Referencing an Image

You can refer to the image anywhere in your document using:

```latex
As shown in Figure~\ref{fig:example}, the image illustrates the concept.
```

LaTeX automatically manages figure numbering.

### Example with Two Images

```latex
\begin{figure}[h]
    \centering

    \includegraphics[width=0.4\textwidth]{image1.png}
    \hspace{0.5cm}
    \includegraphics[width=0.4\textwidth]{image2.png}

    \caption{Comparison of two images}
\end{figure}
```

**Tip:** Use clear, high-quality images and suitable dimensions so that graphics fit naturally into your document.


## 11. Common Errors

| Error | Likely cause |
|---|---|
| Undefined control sequence | Incorrect command or missing package |
| Missing `$` | Unclosed math mode |
| Missing `\end{...}` | Environment not closed |
| Missing brace | Unmatched `{` or `}` |
| Image not found | Incorrect image path |


## Quick Revision

- `.tex` is the LaTeX source file.
- The preamble defines document settings.
- The document body contains the content.
- Packages extend functionality.
- LaTeX is especially useful for technical and mathematical documents.

---

## 📸 See It in Action

Here is an example of a LaTeX document being written
and compiled into a PDF.

![LaTeX source code and compiled PDF](../assets/images/latex/latex-source.png)

![Formatted LaTeX Document](../assets/images/latex/formatted-document.png)


### Final PDF Output

![LaTeX PDF Output](../assets/images/latex/latex-output.png)

*From source code to a formatted document.*


[← Portfolio Home](../README.md) | [Next: Beamer →](../02-Beamer/README.md)

