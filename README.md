# Quantized-LLMs

Visit the docs link for [Literature Review](https://docs.google.com/document/d/13AKlV_DhqfleW82-5kgPufhFQnpCeg1DgRHWcGOVBuI/edit?usp=sharing).

Visit the docs link for [Adaptations and Challenges](https://docs.google.com/document/d/1-e6h6b9d2pJtQexcfdRPrWh_9DbshzChpmhhVqY71pg/edit?usp=sharing).

## Selected Model

* [starcoderbase-3b](https://huggingface.co/bigcode/starcoderbase-3b)

## Quantized to GPTQ format

* [starcoderbase-3b-GPTQ](https://huggingface.co/cosmo3769/starcoderbase-3b-GPTQ)

[Quantization script](https://github.com/cosmo3769/Quantized-LLMs/blob/main/notebooks/quantize-starcodebase-3b-gptq.ipynb) 

## Quantized to GGUF format

* [starcoderbase-3b-GGUF](https://huggingface.co/cosmo3769/starcoderbase-3b-GGUF)

[Quantization script](https://github.com/cosmo3769/Quantized-LLMs/blob/main/notebooks/quantize_starcoderbase_3b_GGUF.ipynb)

## Benchmark 

[Benchmarking script](https://github.com/cosmo3769/Quantized-LLMs/blob/main/notebooks/llmbenchmark-starcodebase-3b-lm-eval-harness.ipynb)

### Baseline starcoderbase-3b model (non-quantized)

|         Tasks         |Version|Filter|n-shot|    Metric     |Value |   |Stderr|
|-----------------------|-------|------|------|---------------|-----:|---|-----:|
|codexglue_code2text    |N/A    |none  |None  |smoothed_bleu_4|1.3519|±  |0.3067|
| - code2text_go        |      1|none  |None  |smoothed_bleu_4|1.5781|±  |0.3734|
| - code2text_java      |      1|none  |None  |smoothed_bleu_4|1.2778|±  |0.1991|
| - code2text_javascript|      1|none  |None  |smoothed_bleu_4|1.1443|±  |0.1181|
| - code2text_php       |      1|none  |None  |smoothed_bleu_4|0.5171|±  |0.5171|
| - code2text_python    |      1|none  |None  |smoothed_bleu_4|2.8338|±  |1.5323|
| - code2text_ruby      |      3|none  |None  |smoothed_bleu_4|0.7601|±  |0.7601|

|      Groups       |Version|Filter|n-shot|    Metric     |Value |   |Stderr|
|-------------------|-------|------|------|---------------|-----:|---|-----:|
|codexglue_code2text|N/A    |none  |None  |smoothed_bleu_4|1.3519|±  |0.3067|

### Quantized starcoderbase-3b model to GPTQ format

|         Tasks         |Version|Filter|n-shot|    Metric     |Value |   |Stderr|
|-----------------------|-------|------|------|---------------|-----:|---|-----:|
|codexglue_code2text    |N/A    |none  |None  |smoothed_bleu_4|0.9254|±  |0.2109|
| - code2text_go        |      1|none  |None  |smoothed_bleu_4|1.4702|±  |0.4813|
| - code2text_java      |      1|none  |None  |smoothed_bleu_4|0.6907|±  |0.6907|
| - code2text_javascript|      1|none  |None  |smoothed_bleu_4|0.9469|±  |0.0339|
| - code2text_php       |      1|none  |None  |smoothed_bleu_4|0.5171|±  |0.5171|
| - code2text_python    |      1|none  |None  |smoothed_bleu_4|1.1676|±  |0.2156|
| - code2text_ruby      |      3|none  |None  |smoothed_bleu_4|0.7601|±  |0.7601|

|      Groups       |Version|Filter|n-shot|    Metric     |Value |   |Stderr|
|-------------------|-------|------|------|---------------|-----:|---|-----:|
|codexglue_code2text|N/A    |none  |None  |smoothed_bleu_4|0.9254|±  |0.2109|
