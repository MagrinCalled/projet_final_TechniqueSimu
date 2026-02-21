On considère un porte-feuille de $N$ contrats d'assurance chacun associé à un motard.

On considère que la distribution d'un remboursement est proportionnelle à \begin{align*}
    f^{*}(x) = &\exp{\left(-\eta\ln{(\alpha + |x-x_0|)} \right)} \mathbb{1}_{x \in \R^{+}}\\ 
    &\eta>3,~x_0>0,~\alpha>0
\end{align*}

De plus, on considère que les conditions météorologiques ont un impact sur les risques encourus par les motards. La météo sera modélisée par une chaîne de Markov à trois états, \textit{Soleil, Nuages, Pluies}.
Avec pour probabilité de transition un vecteur $$\text{ptrans} = (p_{SN},~p_{NS},~p_{NP},~p_{PN})$$

Chaque motard a une probabilité $p_S$ (resp. $p_N$, resp. $p_P$) d'avoir un accident s'il se trouve dans l'état $S$ (resp. $N$, resp. $P$). Ces probabilités sont contenues dans le vecteur $$\text{pacc} = (p_S,~p_N,~p_P)$$

Nous allons nous placer dans deux cadres distincts.

\textbf{Cas A} Tous les motards ont la même météo.

\textbf{Cas B} Chaque motard a sa propre météo (\textit{i.e.} sa propre chaîne de Markov) et elles sont toutes indépendantes.

L'objectif sera d'estimer par Monte-Carlo la quantité \begin{equation}
    m(s):=\E[R-s~|~R>s]
\end{equation}
Où $R$ est le montant des remboursements totaux sur une année et $s > 0$ un seuil fixé à l'avance. Ceci dans le cas \textbf{A} comme le cas \textbf{B}.
