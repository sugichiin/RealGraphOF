
Finally, we compare {\m} on the PC system with four distributed-system based graph engines: PowerGraph~\cite{Gon12}, GraphLab~\cite{Low12}, GraphX~\cite{Gon14}, and Giraph~\cite{Ave11}.
We quote their results for comparison since it is not feasible to construct the identical distributed systems with them.
Note that we use WCC and PR as graph algorithms for comparison since they are the only graph algorithms whose performances on the four distributed-system based graph engines are commonly reported~\cite{Gon12,Gon14}) for the Twitter dataset.
Table~\ref{tab:distributed_all} presents the performance of each graph engine and its system environment where Machine indicates the number and type of machines; for each machine, \#Cores, Mem.Size, and Storage indicate the number of cores, the size of memory, and the type of storage, respectively.
The hyphen (-) means that no result is available in the respective papers.
We note that the distributed-system-based graph engines use hundreds of cores within dozens of machines, which have much more computing power than our single machine employed by our {\m}.
Nevertheless, the result shows that {\m} performs better than distributed-system based engines, even better than PowerGraph, the best performer among them.

In summary, we conclude {\m} achieves significantly better performance than {\real} as well as other existing graph engines by increasing its IO-BW on high-performance storage such as NVMe SSD, using much smaller computing resources in a single machine.



\textbf{EQ4. Comparison with distributed-system-based graph engines.}
Finally, we compare {\mf} with four distributed-system-based graph engines, PowerGraph~\cite{Gon12}, GraphLab~\cite{Low12}, GraphX~\cite{Gon14}, and Giraph~\cite{Ave11}.
We quote the results from their original papers for this comparison.
Following~\cite{Gon12,Low12}, we ran WCC and PR, which are the only graph algorithms whose performances on the four graph engines are commonly reported~\cite{Gon12,Low12} on the Twitter dataset.
%Table 2 shows the result.
Despite storage IOs along with network transfer, {\mf} outperforms \textit{all} of them by up to \textcolor{red}{$7\times$} compared to PowerGraph~\cite{Gon12}, the best performer among them, running \textit{on 64 machines}.
%We note that the four competitors are equipped with much higher computing power as shown in Table ??.
%However, we observe that {\mf} provides the performance better than existing graph engines (by up to y× better than PowerGraph, the best performer among them).
Due to space limitations, these results are provided outside via an external link\footnote{https://github.com/sugichiin/RealGraphOF/blob/main/distributedsystem\_compare.md}.
