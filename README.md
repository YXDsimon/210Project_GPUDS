# 210Project_GPUDS
Project link:<br />
http://eecs.uci.edu/~doemer/f22_ecps210/P16_GPUdirect_Dutt.pdf<br />
References have to read:<br />
[1] NVIDIA GPUDirect Storage. https://docs.nvidia.com/gpudirect-storage/overview- guide/index.html#dev-benefits<br />
[2]Brokhman, Tanya, Pavel Lifshits, and Mark Silberstein. "{GAIA}: An {OS} page cache for
 heterogeneous systems." 2019 USENIX Annual Technical Conference (USENIX ATC 19). 2019.<br />
[3] Qureshi, Zaid, et al. "BaM: A Case for Enabling Fine-grain High Throughput GPU-Orchestrated
 Access to Storage." arXiv preprint arXiv:2203.04910 (2022).
 # Flash Kernel
 已完成。成功在Xavier板子上flash了英伟达提供的Ubuntu特殊版本<br />
 登陆板子需要使用UCI VPN<br />
 ssh simon@128.195.55.217<br />
 密码：nvidia<br />
 待办事项：创建三个不同账号，以免同时登陆发生冲突
 # BCC:
 当前任务：把源码pull下来build，然后熟悉基本操作（见Tutorial）
 ### Background Knowledge:
 https://netflixtechblog.com/linux-performance-analysis-in-60-000-milliseconds-accc10403c55
 ### Tutorial(着重看):
 https://github.com/YXDsimon/bcc/blob/master/docs/tutorial.md
 
 
 ### OCT 31:BCC已成功运行，开始做Darknet
