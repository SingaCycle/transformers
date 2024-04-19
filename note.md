# 项目文件组织
## 整个目录
![alt text](docs/image.png)
```
├── CITATION.cff
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── ISSUES.md
├── LICENSE
├── Makefile
├── README.md
├── README_de.md
├── README_es.md
├── README_fr.md
├── README_hd.md
├── README_ja.md
├── README_ko.md
├── README_pt-br.md
├── README_ru.md
├── README_te.md
├── README_vi.md
├── README_zh-hans.md
├── README_zh-hant.md
├── SECURITY.md
├── awesome-transformers.md
├── conftest.py
├── docker //docker容器
├── docs //文档
├── examples //使用示例
├── hubconf.py
├── model_cards //一个说明
├── notebooks //jupyter notebook形式的链接
├── pyproject.toml
├── scripts //脚本
├── setup.py
├── src //源码
├── templates
├── tests
└── utils
```
## src/transformers目录
```
.
├── benchmark
├── commands
├── data//数据读取和处理
├── generation//生成的采样策略
├── integrations//集成deepspeed或者peft等
├── kernels//一些手写的算子（cuda中没有）
├── models//所有的模型，最主要的文件
├── onnx//onnx推理框架
├── quantizers//量化方法
├── pipelines//任务框架的整合
├── sagemaker//适用于亚马逊训练平台
├── tools//agent，rag等大模型工具
├── utils//杂乱工具
├── __init__.py
├── activations.py//激活函数，torch版本
├── activations_tf.py
├── audio_utils.py
├── cache_utils.py
├── configuration_utils.py
├── convert_graph_to_onnx.py
├── convert_pytorch_checkpoint_to_tf2.py
├── convert_slow_tokenizer.py
├── convert_slow_tokenizers_checkpoints_to_fast.py
├── convert_tf_hub_seq_to_seq_bert_to_pytorch.py
├── debug_utils.py
├── deepspeed.py
├── dependency_versions_check.py
├── dependency_versions_table.py
├── dynamic_module_utils.py
├── feature_extraction_sequence_utils.py
├── feature_extraction_utils.py
├── file_utils.py
├── hf_argparser.py
├── hyperparameter_search.py
├── image_processing_utils.py
├── image_transforms.py
├── image_utils.py
├── keras_callbacks.py
├── modelcard.py
├── modeling_attn_mask_utils.py
├── modeling_flax_outputs.py
├── modeling_flax_pytorch_utils.py
├── modeling_flax_utils.py
├── modeling_outputs.py
├── modeling_tf_outputs.py
├── modeling_tf_pytorch_utils.py
├── modeling_tf_utils.py
├── modeling_utils.py
├── optimization.py
├── optimization_tf.py
├── processing_utils.py
├── pytorch_utils.py
├── safetensors_conversion.py
├── testing_utils.py
├── tf_utils.py
├── time_series_utils.py
├── tokenization_utils.py
├── tokenization_utils_base.py
├── tokenization_utils_fast.py
├── trainer.py//最重要的一个脚本，用于训练
├── trainer_callback.py//配合trainer.py的组件
├── trainer_pt_utils.py
├── trainer_seq2seq.py//继承trainer.py的
├── trainer_utils.py
├── training_args.py
├── training_args_seq2seq.py
└── training_args_tf.py
```
## 以llama为例
```
.
├── __init__.py
├── configuration_llama.py//配置文件
├── convert_llama_weights_to_hf.py//转为hf格式
├── modeling_flax_llama.py//
├── modeling_llama.py//以llama模型，torch版
├── tokenization_llama.py//token
└── tokenization_llama_fast.py
```