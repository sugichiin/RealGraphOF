# EQ4. Comparison with distributed-system-based graph engines.

Finally, we compare `RGOF` with four distributed-system-based graph engines, `PowerGraph`, `GraphLab`, `GraphX`, and `Giraph`.
We quote the results from their original papers for this comparison.
Following their papers, we ran WCC and PR, which are the only graph algorithms whose performances on the four graph engines are commonly reported on the Twitter dataset.

Table below presents the performance of each graph engine and its system environment where Machine indicates the number and type of machines; for each machine, \#Cores, Mem.Size, and Storage indicate the number of cores, the size of memory, and the type of storage, respectively.
The hyphen (-) means that no result is available in the respective papers.
Despite storage IOs along with network transfer, `RGOF` outperforms all of them by up to \textcolor{red}{$7\times$} compared to `PowerGraph`, the best performer among them, running on 64 machines.

https://github.com/user-attachments/assets/796555ac-1274-4a88-97c6-46f6ab01a8ff
