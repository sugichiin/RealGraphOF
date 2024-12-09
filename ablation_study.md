# EQ1. Ablation study.

We (1) verify the effectiveness of our optimization strategies employed in RealGraphOF (i.e., local storage caching (`LSC`) and U-IO/A-IO (`UA`)) and (2) show the superiority of RealGraphOF (`RGOF`, in short) over naive-RealGraphOF (`naive-RGOF`, in short) in terms of IO-BW and execution time.
We use U-IO and A-IO simultaneously because they are implemented together by using SPDK and POS.
We perform graph algorithms and measure their IO-BW and execution time on the Yahoo dataset with four versions of `RGOF`: `RGOF` with no strategies (`naive-RGOF`), LSC only (`RGOF-LSC`), UA only (`RGOF-UA`), and all of them (`RGOF-All`).

Figure below shows the results.
Compared to `naive-RGOF`, UA improves the performance about 169\%/153\% in IO-BW/execution time.
This is because (1) U-IO eliminates the overhead of context switching when issuing IO requests and (2) A-IO eliminates the time for the thread to wait in an idle state after issuing an IO request.
Also, LSC improves the performance about \textcolor{red}{7.17\%/7.17\%} in IO-BW/execution time.
This is because local storage caching reduces the number of remote IOs along with network transfer.
We can summarize our findings as follows: both of our optimization strategies are indeed effective in increasing the IO-BW, thereby reducing the execution time; `RGOF` equipped with both strategies is the most effective, improving the overall performance of by 223\%/206\% in IO-BW/execution time, compared to `naive-RGOF`.

# EQ2. Comparison of the RealGraph family.

We compare the final performances (i.e., execution times) of three versions of RealGraph: original RealGraph (`orgRG`, in short), `naive-RGOF`, and `RGOF`.
We conducted experiments with graph algorithms and datasets mentioned in Section 4.
Figure below shows the results.
We observe the execution times of `RGOF` are much smaller than those of the others in all cases.
Specifically, `RGOF` provides performance about 138\% on average and up to 330\% higher than `naive-RGOF` which is comparable to that of `orgRG`.
Note that `RGOF` can process the large graph data that `orgRG` could not process due to out-of-storage (i.e., `O.O.S`), by employing NVMe-oF;
