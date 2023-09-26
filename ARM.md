# RISCV
https://www.techbang.com/posts/109691-can-risc-v-compete-with-x86
-> 進軍伺服器的RISC-V能否與 x86一戰？

# ARM
https://www.exxactcorp.com/blog/hpc/why-arm-is-becoming-more-popular-in-hpc

文章概要：ARM处理器在高性能计算（HPC）领域越来越受欢迎，原因在于其更高的效率、密度、可伸缩性以及与云计算的兼容性，以便管理物联网设备。本文解释了ARM处理器的优势，以及它们为什么正在改变数据中心和HPC行业。

ARM处理器的兴起

ARM处理器在服务器解决方案领域逐渐崭露头角，尤其是在数据中心和HPC中。
世界上最快的超级计算机之一Fugaku使用基于ARM架构的处理器。
ARM架构介绍

ARM（Advanced RISC Machines）是一种处理器架构，最初由Acorn于1994年开发，以低功耗和高效设计著称。
与传统的x86处理器相比，ARM处理器采用精简指令集计算（RISC）架构，能够更快、更高效地执行任务，同时具有低功耗特性。
ARM vs x86处理器

ARM处理器在性能每瓦特方面表现优异，功耗较低，因此在数据中心和HPC领域具有吸引力。
ARM处理器由于采用简单指令集，执行任务时需要的指令较少，能够提供更好的性能每瓦特比例。
较低的热量产生使ARM处理器在数据中心中更加节能，有助于性能和稳定性。
云本地高密度计算

Ampere推出的Altra和Altra Max处理器针对超大规模云服务提供商，具有高达128个核心。
云提供商可以有效地开发适应核心数量而不是每个核心性能的软件，从而降低能源消耗和总成本。
采用ARM的挑战

软件兼容性是采用ARM处理器的主要挑战，大多数应用程序设计用于x86处理器，需要重新编译才能在ARM处理器上运行。
ARM处理器目前更适用于较简单的应用和用例，需要更多的开发支持才能应对复杂的工作负载。
ARM的未来

ARM处理器在消费市场和云计算中表现出色，将在数据中心领域继续增长。
云提供商如Microsoft Azure、Amazon AWS和Google正在采用ARM处理器以提高能源效率。
创业公司可以利用低成本运行这些系统，推动物联网等领域的新创新。
总结：ARM处理器因其能源效率、性能和云计算兼容性等优势，在HPC领域逐渐崭露头角，并在数据中心和云计算中取得越来越多的应用。尽管面临一些挑战，但ARM处理器有望在未来继续改变高性能计算领域的格局。




https://www.eettaiwan.com/20230314nt61-risc-v-have-a-chance-to-tackle-the-hpc-market/

RISC-V有機會搞定高效能市場嗎？

但對資料中心和超級運算而言，大量程式同時運作的平行吞吐才是最重要的——所以我們看到針對伺服器的處理器雖然核心數量超多，但核心頻率卻並不怎麼高。

一般超大規模資料中心或者雲端要回應大量的使用者請求，所以需要平行和吞吐。而具體到超級運算上，超級運算解決氣候預測、蛋白質折疊、量子運算、模擬模擬之類的問題，這些問題的任何一個都要拆解成需要大規模平行的細分問題。這樣的規模一旦大到一定程度，則不是一顆或者幾顆處理器、加速器晶片可以解決。

所謂的「集群」部署，是指大量處理器不僅需要跨晶片做通訊，還需要跨板、跨伺服器節點做通訊。這類系統的瓶頸可能在die與die、晶片與晶片、板與板、節點與節點之間的通訊延遲和頻寬方面——換句話說就是大量處理器同時工作時，協同的能力和效率。當然完成不同的任務，對核心與系統的需求也可能存在很大差異，但大方向就是如此。

某種程度上，x86在資料中心的某些細分領域，比如HPC AI領域顯現出頹勢，與其系統內部互連方式(如CPU與加速器的互連)、節點互連與通訊的效率有關係——尤其是AI追求的資料處理過程中的資料傳輸大吞吐。所以在Nvidia宣佈Arm架構的Grace CPU之際，NVLink 4作為CPU與GPU的的通訊頻寬相較於PCIe驚豔了很多人；還有後來的Grace-Hopper，die-to-die高速互連。





https://blogs.nvidia.com/blog/2023/03/21/grace-cpu-energy-efficiency/

Green Light: NVIDIA Grace CPU Paves Fast Lane to Energy-Efficient Computing for Every Data Center

The First Results Are In
NVIDIA engineers are running real data center workloads on Grace today.

They found that compared to the leading x86 CPUs in data centers using the same power footprint, Grace is:

2.3x faster for microservices,
2x faster in memory intensive data processing
and 1.9 x faster in computational fluid dynamics, used in many technical computing apps.
Data centers usually have to wait two or more CPU generations to get these benefits, summarized in the chart below.

Grace outperforms x86 CPUs

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/13a98688-e273-444a-80db-17311656e857)



https://technews.tw/2023/09/06/arm-neoverse-v2/

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/a3108b08-3079-446c-91e9-993e6919472d)

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/d7cfc35d-da17-49ab-9253-cc0ef1d164e6)

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/e83e9d1f-8e98-44d5-978a-603bd4e348f3)
這就是如假包換的頂上決戰：144 核心 Nvidia Grace CPU Superchip 對上兩顆 AMD EPYC 9654（總計 192 核心）和兩顆英特爾 Xeon 8480+（共 112 核心），相同功耗，吞吐量大致可達 AMD 兩倍，更不用講看來只是沙包的英特爾了。



https://developer.nvidia.com/blog/nvidia-grace-hopper-superchip-architecture-in-depth/

這篇有超多東西！！！

The NVIDIA Grace Hopper Superchip Architecture is the first true heterogeneous accelerated platform for high-performance computing (HPC) and AI workloads. It accelerates applications with the strengths of both GPUs and CPUs while providing the simplest and most productive distributed heterogeneous programming model to date. Scientists and engineers can focus on solving the world’s most important problems.

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/f2880ac1-c9d0-472a-adad-436a7c1699c9)


https://www.cloudthat.com/resources/blog/achieve-25-better-compute-performance-with-aws-graviton-processor-2

Achieve 25% Better Compute Performance with AWS Graviton Processor

![image](https://github.com/mrbig0503/AI_Search/assets/14293811/292414a6-7ced-430a-9caa-209e63472ea2)



https://www.eettaiwan.com/20210611nt61-between-arm-ang-x86-cpu/

