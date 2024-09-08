# Dead-Block Filter for Prefetcher Optimization

## Abstract
In cache prefetching using Deep Learning Models, **DeadBlocks** (i.e., prefetched addresses that remain unused and contribute to cache pollution) pose a significant issue. This project introduces a **DeadBlock Filter** to mitigate unnecessary cache pollution by filtering prefetched addresses, leading to improved **Instruction Per Cycle (IPC)** and a reduction in useless prefetches. The filter tracks block accesses to detect DeadBlocks efficiently and enhance prefetcher efficiency.

## Introduction
Cache prefetching is a technique used to enhance memory access latency by predicting future memory accesses. However, prefetchers often face **cache pollution** caused by **DeadBlocks**, i.e., prefetched blocks that remain unused. This project proposes a method to filter DeadBlocks to optimize cache utilization and reduce cache pollution.  

**Key Features**:
- Mitigates cache pollution by filtering DeadBlocks.
- Integrates DeadBlock prediction with prefetching strategies.
- Improves cache performance metrics like IPC and prefetch accuracy.

## Approach
The DeadBlock Filter was implemented using the **ChampSim simulator** on various trace files (bc-0, bc-5, pr-14, etc.). The filter uses an **unordered map** data structure to store DeadBlock information and filters out useless prefetches.

### Model Overview
The filter integrates with prefetchers to examine predicted prefetch addresses against identified DeadBlocks. This reduces unnecessary prefetches and improves prefetcher accuracy.

## Experimental Results
The approach significantly enhanced **cache performance** with improvements in the following areas:
1. **IPC Improvement**: Increased IPC, indicating better system performance.
2. **Reduction in Useless Prefetches**: Decreased cache pollution by reducing useless prefetches.
3. **Increase in Useful Prefetches**: More efficient and accurate prefetches were achieved.
4. **Overall Efficiency**: Optimized cache utilization and enhanced system efficiency.

## Conclusion
The DeadBlock Filter shows promising results in improving cache performance by integrating DeadBlock prediction mechanisms with prefetching strategies. Future work may focus on refining DeadBlock prediction for real-time scenarios and applying it to multi-level caches.

## Acknowledgments
Special thanks to **Dr. T.V. Kalyan** for his guidance and support, and to **Sourabh** and **Prathmesh** for their assistance during the project.
