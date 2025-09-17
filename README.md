# latex-code
code main 



Mon code main ------------



% ================================
% Type de document
\documentclass[12pt,a4paper,twoside]{report}

% ================================
% Préambule
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[french]{babel}

% Gestion des marges
\usepackage[top=2cm, bottom=1.5cm, left=1.5cm, right=1.5cm, headheight=14pt]{geometry}

% Graphiques et PDF
\usepackage[pdftex]{graphicx}
\usepackage[final]{pdfpages}

% Liens hypertexte
\usepackage[colorlinks=false]{hyperref}

% Autres packages utiles
\usepackage{ragged2e} % Alignement justifié ou centré
\usepackage{float}
\usepackage{pslatex} % Times New Roman
\usepackage{array}
\usepackage{setspace}
\usepackage{enumerate}
\usepackage{enumitem}
\usepackage{longtable}
\usepackage{titlesec} 
\usepackage{multirow}
\usepackage[font=small,labelfont=bf]{caption}
\onehalfspacing

\setlength{\parskip}{5pt}
\setlength{\parindent}{0pt}

% Table des matières par chapitre
\usepackage[french]{minitoc}
\dominitoc  % active les mini-tables

% Style des chapitres
\usepackage[Glenn]{fncychap}

% Code source
\usepackage{listings}
\usepackage{xcolor}
\lstset{
    backgroundcolor=\color{gray!10},
    keywordstyle=\color{blue}\bfseries,
    commentstyle=\color{green!40!black},
    stringstyle=\color{red!60!black},
    basicstyle=\ttfamily\footnotesize,
    breaklines=true,
    frame=single,
    rulecolor=\color{black!30},
    showstringspaces=false
}

% ================================
% Début du document
\begin{document}


%\includepdf{pagedegarde.pdf}
%\input{Projet/Remerceiment/Remerciement.tex}

% ================================
% Pages préliminaires (numérotation romaine)

\cleardoublepage
\pagestyle{empty} 
\pagenumbering{gobble}

%\pagenumbering{roman} 
\tableofcontents
\listoffigures
\listoftables
\mtcaddchapter

\pagestyle{plain}


\input{Projet/Remerceiment/Dedicace}
\input{Projet/Remerceiment/Remerceiment}

\clearpage

% ================================
% Corps du document (numérotation arabe)
\pagenumbering{arabic}
\setcounter{page}{1} % commence à 1

\input{Projet/introduction}           % Chapitre 1
\input{Cadre générale du projet}      % Chapitre 2
% Ajouter les autres chapitres ici, par exemple :
% \input{Chapitre3}
% \input{Chapitre4}

\end{document}
