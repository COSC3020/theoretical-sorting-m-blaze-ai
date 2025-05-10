# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

To verify that the sorting algorithm sorts in $O(n)$ time based on comparisons, I would start by testing the algorithm empirically. Since the algorithm is a black box and cannot be inspected directly, I can still test its performance. To do so, I would run the algorithm on arrays of varying sized and compare its runtime to known algorithms. If the algorithm is $O(n)$, it would be expected that its runtime would grow lineraly with the input size. Additionally, I would test the algorithm on different input patterns to check for consistent performance across various input cases. Lastly, I would also count the number of comparisons made during sorting and check if the algorithm performs fewer than (nlogn) comparisons, which would provide strong evidence that the claim might be true.

From a theoretical standpoint, we know that for algorithms that compare pairs of elements, the number of comparisons needed to sort n elements must be at least Ω (n log n). This is because there are (n!) possible ways to order (n) elements. As such, any sorting algorithm must distinguish between all these options, requiring at least log_2(n!) comparisons. Since Log_2(n!)∈Θ(nlogn),, no algorithm that is comparison based can perform better than $O(nlogn)$ which makes this proposed algorithm theoretically impossible. 
