* https://github.com/hpcaitech/ColossalAI
* https://docs.broadcom.com/doc/aiops-essentials-of-root-cause-analytics
* https://cloudfabrix.com/blog/aiops/what-is-aiops-top-10-common-use-cases/

LLM

* https://github.com/databrickslabs/dolly

| 模型	| 时间 | 机构| 	类型	| 大小(B) |	链接 |
|---   | --- | --- | ---   | ---     | --- |
MOSS	2023	FudanNLP	Decoder-only	16(双语)	https://github.com/OpenLMLab/MOSS
Phoenix	2023	CUHK	Decoder-only	7 (多语)	
BLOOMZ + 微调		FreedomIntelligence			https://github.com/FreedomIntelligence/LLMZoo
ChatPLUG	2023	Alibaba	Encoder-Decoder	3.7	https://github.com/X-PLUG/ChatPLUG
Chinese-LLaMA-Alpaca	2023	ymcui	Decoder-only	7/13	
LLaMA + 中文pretrain		ymcui			https://github.com/ymcui/Chinese-LLaMA-Alpaca
ChatGLM	2023	Tsinghua	Decoder-only	6	https://github.com/THUDM/ChatGLM-6B
GLM	2022	Tsinghua	Decoder-only	10/130	https://github.com/THUDM/GLM
BLOOMZ	2022	BigScience	Decoder-only	BLOOM + 多任务微调	https://github.com/bigscience-workshop/xmtf
BLOOM	2022	BigScience	Decoder-only	1/3/7/176(多语)	https://huggingface.co/bigscience
CPM-Ant+	2022	OpenBMB	Decoder-only(UniLM)	10(双语)	https://github.com/OpenBMB/CPM-Live/tree/cpm-ant-plus/cpm-live
CPM-Ant	2022	OpenBMB	Decoder-only(UniLM)	1/3/7/10	https://github.com/OpenBMB/CPM-Live/tree/cpm-ant/cpm-live
PanGu-α	2022	PengCheng	Decoder-only	2.6/13	https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha
PLUG	2022	Alibaba	Encoder-Decoder	27	https://github.com/alibaba/AliceMind/tree/main/PLUG
OPD(对话)	2022	Tsinghua	Decoder-only(UniLM)	6.3	https://github.com/thu-coai/OPD
封神 系列	2022	IDEA			https://github.com/IDEA-CCNL/Fengshenbang-LM
CPM-2	2021	Tsinghua	Encoder-Decoder	11/198	https://github.com/TsinghuaAI/CPM-2-Finetune
CPM-1	2021	Tsinghua	Decoder-only	2.6	https://github.com/TsinghuaAI/CPM-1-Finetune
Chinese-Transformer-XL	2021	Tsinghua	Decoder-only	2.9	https://github.com/THUDM/Chinese-Transformer-XL
mT5	2020	Google	Encoder-Decoder	1.2/3.7/13	https://github.com/google-resea


GPT-2: 由OpenAI开发的基于Transformer的语言模型，可用于生成文本、回答问题等任务。GitHub链接
GPT-3: 由OpenAI开发的基于Transformer的语言模型，具有极高的生成能力和通用性。GitHub链接
BERT: 由Google开发的基于Transformer的预训练语言模型，可用于文本分类、命名实体识别等任务。GitHub链接
RoBERTa: 由Facebook AI Research开发的基于Transformer的预训练语言模型，具有比BERT更高的性能。GitHub链接
XLNet: 由CMU和Google Brain开发的基于Transformer的预训练语言模型，采用了permutation-based自回归和自编码机制，具有比BERT更高的性能。GitHub链接
T5: 由Google开发的基于Transformer的预训练语言模型，可用于生成文本、翻译等任务。GitHub链接
ALBERT: 由Google开发的基于Transformer的预训练语言模型，采用了参数共享和跨层参数共享机制，具有比BERT更高的效率和性能。GitHub链接
ELECTRA: 由Google开发的基于Transformer的预训练语言模型，采用了对抗训练机制，具有比BERT更高的性能和训练效率。GitHub链接
GShard: 由Google开发的基于Transformer的分布式预训练语言模型，可用于处理超大规模数据。GitHub链接
Megatron-LM: 由NVIDIA开发的基于Transformer的分布式预训练语言模型，可用于处理超大规模数据。GitHub链接
这些语言模型在GitHub上都有开源代码和预训练模型可供使用。


模型名称	开发语言	参数数量	最小规模训练所需耗时
GPT-2	Python	1.5亿	1天
GPT-3	Python	1.75万亿	355年
BERT	Python	1.1亿	4天
RoBERTa	Python	1.5亿	4天
XLNet	Python	3亿	2天
T5	Python	11亿	1天
ALBERT	Python	8千万	4天
ELECTRA	Python	1.1亿	4天
GShard	C++	6亿	3天
Megatron-LM	Python	8亿	1天

训练这些语言模型需要大量的计算资源，因此需要使用高性能的GPU卡。具体来说，需要什么样级别的GPU卡取决于模型的大小和训练数据的规模，以及训练所需的时间和预算等因素。一般来说，越大的模型和训练数据需要的GPU卡就越高级别。以下是一些常用的GPU卡及其适用的模型规模：

NVIDIA GeForce RTX 3090：适用于最大规模的语言模型，如GPT-3等。
NVIDIA GeForce RTX 3080 Ti：适用于大规模的语言模型，如RoBERTa、T5等。
NVIDIA GeForce RTX 3080：适用于中等规模的语言模型，如BERT、XLNet等。
NVIDIA GeForce RTX 3070：适用于较小规模的语言模型，如ALBERT、ELECTRA等。
需要注意的是，GPU卡的选择不仅受到模型规模的影响，还受到训练数据的规模、训练算法的复杂度、训练的批次大小等因素的影响。因此，在选择GPU卡时，需要综合考虑以上因素，并根据自己的具体情况做出合理的选择。

You:
最小规模数据量 和 最小训练资源需求

ChatGPT:
最小规模数据量和最小训练资源需求取决于所使用的语言模型和训练任务的复杂度。以下是一些常见的语言模型和对应的最小规模数据量和最小训练资源需求：

BERT：建议使用至少10万到100万条文本数据进行训练，需要至少16GB的GPU显存，训练时间为数天到数周。
GPT-2：建议使用至少几百万条文本数据进行训练，需要至少32GB的GPU显存，训练时间为数周到数月。
GPT-3：建议使用数十亿到数万亿条文本数据进行训练，需要至少250GB的GPU显存，训练时间为数月到数年。
需要注意的是，以上数据量和资源需求仅供参考，实际情况可能因训练任务的复杂度、训练算法的优化程度、硬件设备的性能等因素而有所不同。在实际训练中，建议根据具体情况进行调整和优化，以达到最佳的训练效果。

