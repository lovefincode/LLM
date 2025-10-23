## 名词

|名词|全称|含义|备注|
|--|--|--|--|
|V2||||
|V3||||
|R1-Zero||||
|R1||||
|MoE||||
|MLA|Multi-Head Latent Attention||QMLA（量化MLA）或者CMLA（压缩MLA）|
|CoT|Chain of Thought|思维链||
|RL|Reinforcement Learning|强化学习||
|SFT|Supervised Fine-Tuning|监督微调||
|RoPE|Rotary Position Embedding|旋转位置编码||
|Reasoning||推理||
|HAI-LLM||||
|TP|Tensor Parallelism|张量并行|将模型层放置在并行执行计算的多个设备（计算芯片）上，包括逐行和逐列并行|
|PP|Pipeline Parallelism|流水线并行|每个设备（计算芯片）都包含一部分模型层，每个训练批次分为串行的小批次以进行流水线执行|
|FSDP|Fully Sharded Data Parallel|全共享数据并行|基于ZeRO Stage 3算法，对模型的参数、优化器状态和梯度分布到不同的设备（计算芯片）上。在正向传播期间，FSDP执行 allgather作来组装完整的参数，并正向传播完成后释放；反向传播期间，FSDP执行allgather获取完整参数，并进行反向梯度计算，然后执行reduce-scatter以同步所有设备之间的梯度，每个设备只保留部分梯度、参数和优化器更新|
|DP|Data Parallelism|数据并行 |模型和优化器的状态在多个设备（计算芯片）之间复制，数据均匀分布给所有设备进行并行计算|
|EP|Expert Parallelism|专家并行|在MoE 训练期间，MoE 模型的不同专家分布在不同的设备（计算芯片）上，由门控单元将输入的Token分配给不同的专家|
|DualPipe算法||||
