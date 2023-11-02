https://huggingface.co/docs/transformers/main/llm_tutorial


https://github.com/mrbig0503/AI_Search/assets/14293811/29f22750-06f1-4b35-bfcb-fedb7a2799df


https://github.com/mrbig0503/AI_Search/assets/14293811/7c2cd5ca-8aaa-4810-b19a-6e7d7e95547e


Profiling 方法有兩種
1. 統計法 (Profiling）：
   a. 計算量：OP 的 MAC (multiply-accumulate count) 加總
   b. 記憶體量：Param_Size + OP_Need_Size
   c. 頻寬：(Param_Size + 2 x OP_Need_Size) / Exe_Time 
3. 量測法（Perf tool)：
   a. 計算量：系統執行的Cycle數
   b. 記憶體量：Param_Size + OP_Alloc_Size
   c. 頻寬：(Param_Size + 2 x OP_Alloc_Size) / Exe_Time 


LLM 目前還沒有統計法的數據，只能用公開資料來推測
StableDIffusion 有統計法取得資訊
LLM & StableDiffusion 都有量測法可以推測記憶體量與頻寬


1. 假設model是在記憶體上，硬體只有 read，所以是 1x Param Size 頻寬
2. Operator計算結果的暫存空間也在記憶體上，預期是 write & read Allocate 出來的空間
   所以是 2x Operator required mem
3. LLM 統一用 每秒20個 token 來評估計算量與頻寬 INT8
4. Stable Diffusion 統一用 10seconds/frame 來評估計算量與頻寬 INT8
