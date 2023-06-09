# rbp-os

今年的study-2023计划中，包含了rust和Cortex-M处理器架构的学习。截止到目前为止RUST已经学的七七八八，偶然间找到了RUST编写简易操作系统的博客https://os.phil-opp.com/ 大为震撼。该博主基于x86架构的芯片使用rust编写了操作系统，里面包含了，中断异常处理、内存分配、还有任务管理的一些机制。受到该博主的启发，或许我们可以基于Cortex-M的同步进行开发。这样做的好处，我们既可以熟悉rust，又可以熟悉Cortex-M，又结合了操作系统的知识，可以说一举三得。我相信理论基础的学习也仅仅是第一步，自己动手编写和调试才能有很深刻的掌握。

我不打算把rbp-os作为一个要交付的“产品”，它不会是一个从顶层到底层的的设计方式。它更像是一种“乐高积木”，一个系统要素一个要素的去实现。在自定义的操作系统中，我们可以随意的增加自己的系统模块。我们按照博主的思路，先去做一个最小的内核，然后慢慢开发中断异常的处理，后续增加内存MMU管理，heap分配器，而这些机制可能一开始我们做一个能够“work”的最简单的实现方式，后续我们慢慢的增强，借鉴Linux内核的处理机制不断的去完善更复杂的场景。

我们开始吧！！！

-----

* [01_ARMv7m_Using_The_RUST_Cross_Compiler](https://github.com/carloscn/blog/issues/180) [2023-04-18]
