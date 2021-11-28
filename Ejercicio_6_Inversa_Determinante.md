# Ejercicio 6. Inversa Determinante 

Sea la siguiente matriz:
<img src="https://render.githubusercontent.com/render/math?math=A=\begin{bmatrix}1& 4&-2& 0\\
-3&-2& 0& 1\\
 3& 2& 1&-1\\
 2&-2& 3& 4
\end{bmatrix}">

Obtener 
\begin{itemize}
    \item Matriz de menores
    \item Matriz de cofactores
    \item Determinante
    \item Matriz Adjunta
    \item Matriz inversa
\end{itemize}

\newpage
\tableofcontents
\newpage

\section{Matriz de Menores}
$$
\begin{bmatrix}
-6 & -14 & 0 & -10\\
40 &  35 &-50&   0\\
-24& -31 & 50&  10\\
-4 &  -1 &  0&  10
\end{bmatrix}
$$
\section{Matriz de Cofactores}
$$
cof(A)=
\begin{bmatrix}
-6 & 14 & 0 & 10\\
-40& 35 & 50&  0\\
-24& 31 & 50&-10\\
 4 & -1 &  0& 10
\end{bmatrix}
$$

\section{Determinante}
$$|A|=
\begin{vmatrix}
 1& 4&-2& 0\\
-3&-2& 0& 1\\
 3& 2& 1&-1\\
 2&-2& 3& 4
\end{vmatrix}
= 50$$

\section{Matriz Adjunta}
$$
adj(A)=
\begin{bmatrix}
-6 & -40 & -24 &  4\\
14 &  35 &  31 & -1\\
 0 &  50 &  50 &  0\\
10 &   0 & -10 & 10
\end{bmatrix}
$$
\section{Matriz inversa}
$$
A^{-1} = \frac{1}{50} *
\begin{bmatrix}
-6 & -40 & -24 &  4\\
14 &  35 &  31 & -1\\
 0 &  50 &  50 &  0\\
10 &   0 & -10 & 10
\end{bmatrix} =
\begin{bmatrix}
-\frac{3}{25} & -\frac{4}{5} & -\frac{12}{25} &  \frac{2}{25}\\
\frac{7}{25} &  \frac{7}{10} &  \frac{31}{50} & -\frac{1}{50}\\
 0 &  1 &  1 &  0\\
\frac{1}{5} &   0 & -\frac{1}{5} & \frac{1}{5}
\end{bmatrix}
$$
