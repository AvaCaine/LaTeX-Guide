# 📄 LaTeX Quick Reference Guide

This guide summarizes the essential components needed to set up a modern LaTeX document and the most common commands for formatting text and structure.

-----

## 1\. Document Setup (The Preamble)

The Preamble is everything that comes before the `\begin{document}` command. It tells LaTeX how to process your entire file.

| Command | Category | Description |
| :--- | :--- | :--- |
| `\documentclass[11pt, a4paper]{article}` | **Mandatory Start** | Defines the document type. The most common are **`article`** (short papers/documents), **`report`** (long reports/theses), and **`book`**. |
| `\usepackage{fontspec}` | **Modern Fonts** | *Essential* for using the Noto font family and other system fonts. |
| `\usepackage[english]{babel}` | **Language** | Loads the Babel package to handle hyphenation and language-specific rules. Replace `english` with your main language if needed. |
| `\babelfont{rm}{Noto Sans}` | **Font Selection** | Sets the main document font. **`Noto Sans`** is a clean, modern, and highly legible choice. |
| `\usepackage{geometry}` | **Page Layout** | Allows you to easily control margins. |
| `\usepackage{amsmath}` | **Math** | Essential package for advanced mathematical environments and commands. |
| `\usepackage{booktabs}` | **Tables** | Required for professionally formatted, clean tables. |
| `\title{...}`, `\author{...}`, `\date{...}` | **Metadata** | Defines the title, author, and date for the document. |

-----

## 2\. Document Structure (The Flow)

These commands define the hierarchy and flow of your content.

| Command | Example | Description |
| :--- | :--- | :--- |
| **Document Body** | `\begin{document}` ... `\end{document}` | All content must be placed between these two commands. |
| **Title Generation** | `\maketitle` | Generates the title block using the metadata defined in the preamble. |
| **Abstract** | `\begin{abstract}` ... `\end{abstract}` | Creates a dedicated, formatted abstract section (often used in `article` class). |
| **Main Sections** | `\section{Overview}` | Creates a top-level heading. LaTeX automatically handles the numbering (1, 2, 3...). |
| **Subsections** | `\subsection{Details}` | Creates a second-level heading (e.g., 1.1, 1.2). |
| **Paragraph Break** | *Two blank lines* | You break a paragraph simply by leaving a blank line in your source code. |

-----

## 3\. Text and Formatting

These are the most frequent commands you'll use to emphasize text or include special elements.

| Command | Output / Purpose | Example |
| :--- | :--- | :--- |
| **Bold Text** | **Bold** | `\textbf{This is bold}` |
| **Italic Text** | *Italic* | `\textit{This is italic}` |
| **Monospace** | `Monospace` | `\texttt{This is code}` |
| **Line Break** | Forces a new line | `First line\\Second line` |
| **Footnote** | Adds a numbered footnote | `The claim is correct\footnote{See source A.}` |
| **Quotation** | Indented quotation block | `\begin{quote} ... \end{quote}` |

-----

## 4\. Lists

The two primary list environments are used for bullet points and numbered lists.

### Unordered (Bulleted) List

```latex
\begin{itemize}
    \item First point.
    \item Second point.
\end{itemize}
