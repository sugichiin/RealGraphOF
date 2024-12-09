# EQ 3. Comparison with single-machine-based graph engines.

We compare RGOF with 5 state-of-the-art single-machine-based graph engines on remote storage, `GraphChi`, `X-Stream`, `GridGraph`, `TurboGraph`, and `FlashGraph`.
We employed BFS, PR, and WCC algorithms, which are commonly provided by all these graph engines.
Figure below shows the results on the real-world datasets, where `O.O.M` and `O.O.T` denote the cases of out-of-memory and out-of-time (i.e., exceeding 24 hours).
We note that TurboGraph does not perform WCC on the Wiki and UK datasets (i.e., infeasible).
We observe that RGOF dramatically outperforms all existing graph engines, by up to \textcolor{red}{$22.8\times$/$7.9\times$} better than TurboGraph/FlashGraph which are the best performers among competitors.
