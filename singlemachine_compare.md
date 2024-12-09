single-machine-based graph engines}\label{sec:eval-single_all}
We compare {\m} with five single-machine-based graph engines: GraphChi~\cite{Kyr12}, X-Stream~\cite{Roy13}, TurboGraph~\cite{Han13}, GridGraph~\cite{Zhu15}, and FlashGraph~\cite{Zhe15}.
We run BFS, PR, and WCC, which are commonly provided by all graph engines, by executing each graph engine with 8 CPU threads on each of the PC system with the same specifications, since they require different operating systems (i.e., Windows OS for TurboGraph and Linux OS for the other graph engines).
Figure~\ref{fig:single_all} shows the result where "O.O.M" and "O.O.T" denote the out-of-memory and out-of-time indicating the case exceeding 24 hours, respectively.
We note that TurboGraph does not perform WCC on the Wiki and UK datasets (i.e., infeasible).
We observe that {\m} provides the performance much better than the existing graph engines, especially, by up to 69$\times$ better than TurboGraph, the best performer among existing graph engines.


\textbf{EQ3. Comparison with single-machine-based graph engines.}
We compare {\mf} with 5 state-of-the-art single-machine-based graph engines on remote storage, GraphChi~\cite{Kyr12}, X-Stream~\cite{Roy13}, GridGraph~\cite{Zhu15}, TurboGraph~\cite{Han13}, and FlashGraph~\cite{Zhe15}.
%Here, we quote the results of TurboGraph with local storage from the previous paper~\cite{Jan23}, because we have the SMRC servers with Linux OS only while TurboGraph runs on Windows OS.
We employed BFS, PR, and WCC algorithms, which are \textit{commonly provided} by \textit{all} these graph engines.
Figure~\ref{fig:perf_vs_Others} shows the results on the Friend and Yahoo datasets, where "O.O.M" and "O.O.T" denote the cases of out-of-memory and out-of-time (i.e., exceeding 24 hours).
We observe that {\mf} dramatically outperforms all existing graph engines, by up to \textcolor{red}{$22.8\times$/$7.9\times$} better than TurboGraph/FlashGraph which are the best performers among competitors.
%This is because {\mf} substantially improves its IO processing while maintaining the excellent workload balancing capability of the original RealGraph, and two optimization strategies improved the performance successfully when using remote storage.
The results on other datasets (i.e., Wiki, UK, Twitter, SK) and another algorithm (i.e., PR) are provided outside via an external link\footnote{https://github.com/sugichiin/RealGraphOF/blob/main/singlemachine\_compare.md}.

