single-machine-based graph engines}\label{sec:eval-single_all}
We compare {\m} with five single-machine-based graph engines: GraphChi~\cite{Kyr12}, X-Stream~\cite{Roy13}, TurboGraph~\cite{Han13}, GridGraph~\cite{Zhu15}, and FlashGraph~\cite{Zhe15}.
We run BFS, PR, and WCC, which are commonly provided by all graph engines, by executing each graph engine with 8 CPU threads on each of the PC system with the same specifications, since they require different operating systems (i.e., Windows OS for TurboGraph and Linux OS for the other graph engines).
Figure~\ref{fig:single_all} shows the result where "O.O.M" and "O.O.T" denote the out-of-memory and out-of-time indicating the case exceeding 24 hours, respectively.
We note that TurboGraph does not perform WCC on the Wiki and UK datasets (i.e., infeasible).
We observe that {\m} provides the performance much better than the existing graph engines, especially, by up to 69$\times$ better than TurboGraph, the best performer among existing graph engines.


\textbf{EQ2. Comparison of the RealGraph family.}
We compare the final performances (i.e., execution times) of three versions of RealGraph: {\rgf}, naive-{\mf}, and {\mf}.
We conducted experiments with graph algorithms and datasets mentioned in Section~\ref{sec:eval_setup}.
Figure~\ref{fig:perf_vs_RealGraph} shows the results with BFS and PR due to space limitations.
We observe the execution times of {\mf} are much smaller than those of the others in all cases.
Specifically, {\mf} provides performance about 138\% on average and up to 330\% higher than naive-{\mf} which is comparable to that of {\rgf}.
%109.4\% 137.62\% and 202.72\% 329.52\%
Note that {\mf} can process the large graph data that {\rgf} could not process due to out-of-storage (i.e., O.O.S), by employing NVMe-oF;
