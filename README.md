# proj181-xiaomi-vela-posix-wasm-runtime

## 基于Vela平台的POSIX和Wasm的多语言运行时

### 赛题要点/解析

#### 项目介绍

##### 平台介绍

**关于Vela**：[Vela](https://iot.mi.com/vela)是小米公司基于开源实时操作系统NuttX打造的物联网嵌入式软件平台，Vela在各种物联网硬件平台上提供统一的软件服务，支持丰富的组件和易用的框架，用于打通碎片化的物联网应用场景。

**关于NuttX**：[NuttX](https://nuttx.apache.org/docs/latest/)是一个在IoT、分布式嵌入式系统、无人机系统中广泛使用的RTOS，第一个版本由 Gregory Nutt 于 2007 年发布。NuttX 可以支持 8 位到64位的处理器，支持risc-v，arm，mips，x86等主流芯片平台，按照POSIX和 ANSI 标准进行设计，支持MMU和MPU，支持多线程和进程。2019年NuttX在小米的推动下正式进入Apache基金会，小米多位资深工程师参与了 [NuttX社区](https://github.com/apache/incubator-nuttx) 的开发和架构设计。经过多年的不懈努力，NuttX功能丰富，性能稳定，商业化成熟度高，在各种物联网产品上得到了广泛的应用。

##### 项目意义

WebAssembly（以下简称Wasm）技术对于没有MMU的小型嵌入式操作系统是一个很好的补充，它具备高性能并且让应用和系统之间能够隔离开，Wasm生态目前也在逐步完善中，类似C、C++、Go、Rust、Assembly Script等流行语言都支持编译到Wasm，创建一个统一的多语言运行时具备丰富嵌入式应用开发生态、提升应用开发效率和安全性的意义。

#### 功能点

注：所有功能点应能在K210板卡上运行并演示

• 以Vela平台为基础，使用NuttX作为目标OS，使用WAMR作为Wasm虚拟机

• 提供NuttX端的bottom half库和WAMR/语言端的upper half库

• 支持C、C++、Rust和Assembly Script

### 项目导师

• 黄齐，Bytecode Alliance RC / WAMR TSC Member , huangqi3@xiaomi.com

• 小米公司Vela研发团队（含NuttX社区主要代码提交人）

#### 难度

中等

#### 参考资料

• [https://nuttx.apache.org/docs/latest/](https://github.com/acoinfo/sylixos_oscomp_2021/tree/master/Dual-OS-OpenAMP)

• https://github.com/apache/incubator-nuttx/tree/master/boards/risc-v/k210/maix-bit

• https://rustwasm.github.io/docs/book/

• https://github.com/WebAssembly/wasi-sdk

• https://www.assemblyscript.org

• https://github.com/bytecodealliance/wasm-micro-runtime

• https://nuttx.apache.org

#### 预期目标

注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

• 完整且独立的开发SDK和C/C++/Rust/Assembly Script支持

• 配套的NuttX/WAMR端支持库

### 对参赛队提供的支持

• NuttX在Wasm支持方面的现状及改进方向

• WAMR在多语言支持方面的现状及改进方向

• 针对NuttX实时操作系统和Vela平台业界最专业权威的技术支持和指导
