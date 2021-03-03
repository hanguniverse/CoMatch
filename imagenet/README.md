### Semi-supervised learning on ImageNet with 1% or 10% labels:

This implementation only supports multi-gpu, DistributedDataParallel training, which is faster and simpler.

To train CoMatch with 1% labels, run:
<pre>python Train_CoMatch.py --percent 1 --thr 0.6 --contrast-th 0.3 --lam-c 10 [Imagenet dataset folder]</pre>

To train CoMatch with 10% labels, run:
<pre>python Train_CoMatch.py --percent 10 --thr 0.5 --contrast-th 0.2 --lam-c 2 [Imagenet dataset folder]</pre>


### Download CoMatch pre-trained ResNet-50 models
<a href="https://storage.googleapis.com/sfr-pcl-data-research/CoMatch_checkpoint/CoMatch_1percent.pth.tar">1% labels</a>| <a href="https://storage.googleapis.com/sfr-pcl-data-research/CoMatch_checkpoint/CoMatch_10percent.pth.tar">10% labels</a>
------ | ------


### Semi-supervised learning results with CoMatch

num. labels | top-1 acc. | top-5 acc
--- | --- | --- 
1%  | 66.0% | 86.4% 
10%  | 73.6% | 91.6%