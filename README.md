# bamboofilters

We propose a novel approximate membership query data structure called bamboo filter. Bamboo filters implement insertion, lookup, and deletion operations with a constant-time cost, and support expanding and compressing the hash table in a fine-grained way. 

## Build and run

```
mkdir build
cd build
cmake ..
cd test
make
./example
```

## Evaluation

|Algorithm| Description|
|:----:|----|
|DBF|D. Guo, J. Wu, H. Chen, Y. Yuan, and X. Luo, “The Dynamic Bloom Filters,” IEEE Transactions on Knowledge and Data Engineering, vol. 22, no. 1, pp. 120–133, 2009. Implementation: https://github.com/CGCL-codes/DCF/tree/master/src_DBF|
|EBF|Y. Wu, J. He, S. Yan, J. Wu, T. Yang, O. Ruas, G. Zhang, and B. Cui, “Elastic Bloom Filter: Deletable and ExpandableFilter Using Elastic Fingerprints,” IEEE Transactions on Computers, vol. 1, no. 1, pp. 1–8, 2021. Implementation: https://github.com/Dustin-He/ElasticBloomFilter/blob/master/bloom.h|
|SBF|K. Xie, Y. Min, D. Zhang, J. Wen, and G. Xie, “A Scalable Bloom Filter for Membership Queries,” in Proceedings of the Global Communications Conference. IEEE, 2007, pp. 543–547. Implementation: https://github.com/Dustin-He/ElasticBloomFilter/blob/master/ScalableBF.h|
|DCF|H. Chen, L. Liao, H. Jin, and J. Wu, “The Dynamic Cuckoo Filter,” in Proceedings of International Conference on Network Protocols. IEEE, 2017, pp. 1–10. Implementation: https://github.com/CGCL-codes/DCF|
|SuRF|H. Zhang, H. Lim, V. Leis, D. G. Andersen, M. Kaminsky, K. Keeton, and A. Pavlo, “SuRF: Practical Range Query Filtering with Fast Succinct Tries,” in Proceedings of International Conference on Management of Data. ACM, 2018, pp. 323–336. Implementation: https://github.com/efficient/SuRF|
|E2CF|S. Yu, S. Wu, H. Chen, and H. Jin, “The entry-extensible cuckoo filter,” in Proceedings of International Federation for Information Processing. Springer, 2020, pp. 373–385. Implementation: https://github.com/CGCL-codes/E2CF|
|TCF|J. Apple, “Stretching your data with taffy filters,” arXiv preprint arXiv:2109.01947v4, 2022. Implementation: https://github.com/jbapple/libfilter|
|LDCF|F. Zhang, H. Chen, H. Jin, and Pedro Reviriego, “The logarithmic dynamic cuckoo filter,” in Proceedings of IEEE International Conference on Data Engineering. IEEE, 2021, pp. 948-959. Implementation: https://github.com/BigDataProcessing/LDCF|


## Results

Our results show that bamboo filters have the highest insertion throughput, positive lookup throughput, and deletion throughput even after multiple resizing operations. Moreover, bamboo filters have the lowest positive/negative lookup and deletion throughput decline rate.