Also note:  
Einsum vs matmul: [https://discuss.pytorch.org/t/gpu-speed-and-memory-difference-between-einsum-and-matmul/164493/2](https://discuss.pytorch.org/t/gpu-speed-and-memory-difference-between-einsum-and-matmul/164493/2)￼
 
nnConv2d = unfold + matmul + fold  
[https://github.com/pytorch/pytorch/issues/47990](https://github.com/pytorch/pytorch/issues/47990)  
[https://stackoverflow.com/questions/53972159/how-does-pytorchs-fold-and-unfold-work](https://stackoverflow.com/questions/53972159/how-does-pytorchs-fold-and-unfold-work)
 
Take a look into why similarity can squeeze -2
 
MatMul Efficiency
 
[https://discuss.pytorch.org/t/many-weird-phenomena-about-torch-matmul-operation/158208](https://discuss.pytorch.org/t/many-weird-phenomena-about-torch-matmul-operation/158208)
 
[https://stackoverflow.com/questions/67496315/how-to-efficiently-multiply-by-torch-tensor-with-repeated-rows-without-storing-a](https://stackoverflow.com/questions/67496315/how-to-efficiently-multiply-by-torch-tensor-with-repeated-rows-without-storing-a)
 
[https://discuss.pytorch.org/t/memory-efficient-way-to-implement-masked-matrix-multiplication/127543/4](https://discuss.pytorch.org/t/memory-efficient-way-to-implement-masked-matrix-multiplication/127543/4)
 
[https://discuss.pytorch.org/t/cuda-memory-use-batched-matrix-multiplication/164131/4](https://discuss.pytorch.org/t/cuda-memory-use-batched-matrix-multiplication/164131/4)
 
[https://discuss.pytorch.org/t/unexpected-huge-memory-cost-of-matmul/41642](https://discuss.pytorch.org/t/unexpected-huge-memory-cost-of-matmul/41642)
 
[https://stackoverflow.com/questions/73924697/whats-the-difference-between-torch-mm-torch-matmul-and-torch-mul](https://stackoverflow.com/questions/73924697/whats-the-difference-between-torch-mm-torch-matmul-and-torch-mul)
 
[https://pytorch.org/docs/stable/generated/torch.bmm.html](https://pytorch.org/docs/stable/generated/torch.bmm.html)
 
[https://www.geeksforgeeks.org/performing-batch-multiplication-in-pytorch-without-using-torchbmm/](https://www.geeksforgeeks.org/performing-batch-multiplication-in-pytorch-without-using-torchbmm/)
 
While torch.matmul, torch.einsum, and for-loops provide alternatives to torch.bmm, it’s essential to consider performance implications.  
torch.bmm is optimized for batch matrix multiplication and is generally more efficient than other methods, especially for large-scale operations. **For most use cases, torch.matmul and torch.einsum should be sufficient, but for highly optimized performance, sticking with torch.bmm might be preferable.**  
When choosing an alternative to torch.bmm, it’s important to consider the performance implications:

- **Hardware**: The performance of different methods can vary significantly depending on the hardware (CPU vs. GPU) and specific configurations.
- **Batch Size:** For large batch sizes, methods that avoid explicit loops, such as torch.matmul, may offer better performance.
- **Precision:** Using lower precision (e.g., float16) can help reduce memory usage and potentially increase speed but may affect numerical stability.
 \> From \<[https://www.geeksforgeeks.org/performing-batch-multiplication-in-pytorch-without-using-torchbmm/](https://www.geeksforgeeks.org/performing-batch-multiplication-in-pytorch-without-using-torchbmm/)\>      
[https://www.kernel-operations.io/keops/index.html](https://www.kernel-operations.io/keops/index.html)