一个token类似于一个单词卡片，它被记录在tokenizer的词表中，这个词表是在预训练之前就已经写好了的。tokenizer中包含 词表 和 分词算法。tokenizer负责对句子的拆分，模型只接收拆分后的token IDs

如：今天天气很好 
对于 ai大模型来说 这可能是由 "今天" "天气" "很" "好" 这四个token组合而成的。
又或者说这句话会被大模型绑定的tokenizer拆分为这4个token。

比如：unhappy
可能会被拆分为"un" "happy"这两个token。

至于为什么说是“可能会被拆分为”，这是因为拆分句子是通过tokenizer来进行拆分的，
而tokenizer是在预训练之前构建并与模型绑定，
不同模型绑定的tokenizer可能会不同，所以不同模型的tokenizer对句子的拆分就会不一样。
但可以确定的是同一个tokenizer对同一个句子的拆分，token一定是一致的。