# Deploying LLM to Mobile

To deploy LLM to mobile, we need a quantized model in GGUF format for CPU inference. 

## Selected Model

* [bigcode/starcoderbase-3b](https://huggingface.co/bigcode/starcoderbase-3b)
* [bigcode/starcoderbase-1b](https://huggingface.co/bigcode/starcoderbase-1b)

## Local deployment steps on ios

[llama.cpp](https://github.com/ggerganov/llama.cpp) has developed a barebone ios app using swiftui. You can find the example [here](https://github.com/ggerganov/llama.cpp/tree/master/examples/llama.swiftui). You can also find a lengthy discussion on `Performance of llama.cpp on Apple Silicon A-series` where some models have been benchmarked and also instruction is given how you can benchmark as well.

The general steps to follow to run the app in simulator: 

### Clone the repo

```
git clone https://github.com/ggerganov/llama.cpp
```

### Download xcode in mac

Download xcode in mac from app store. Don't forget to install ios stimulator as well. You will be prompted to install during xcode installation.

### Open the `examples/llama.swiftui` with Xcode

In your terminal where you have cloned the repo, type

```
cd llama.cpp/examples/llama.swiftui
xed .
```

This will open `llama.swiftui` in xcode.

### Select the simulator

Select the ios simulator from top (iphone 15 pro max in my case)

### Click on Run

Click on `run` icon to build and start the ios simulator.

## Tested models

### cosmo3769/starcoderbase-1b-GGUF

I have downloaded and loaded [bigcode/starcoderbase-1b](https://huggingface.co/bigcode/starcoderbase-1b) in GGUF format which I have quantized. Here is the download link for the [GGUF format cosmo3769/starcoderbase-1b-GGUF](https://huggingface.co/cosmo3769/starcoderbase-1b-GGUF/resolve/main/starcoderbase-1b.Q4_K_M.gguf?download=true).

![Simulator Screenshot - iPhone 15 Pro Max - 2024-03-14 at 15 34 01](https://github.com/cosmo3769/Quantized-LLMs/assets/53268607/0edf6eeb-24f3-4a4b-b8e1-2d53f149dc27)

![Simulator Screenshot - iPhone 15 Pro Max - 2024-03-14 at 15 35 33](https://github.com/cosmo3769/Quantized-LLMs/assets/53268607/d8fa5e4d-c9a9-43cf-8fde-20c1265ff33e)

![Simulator Screenshot - iPhone 15 Pro Max - 2024-03-14 at 15 36 17](https://github.com/cosmo3769/Quantized-LLMs/assets/53268607/3cf19c60-a069-4ebd-a8ee-24aa5c60e2e1)

### cosmo3769/starcoderbase-3b-GGUF

I have downloaded and loaded [bigcode/starcoderbase-3b](https://huggingface.co/bigcode/starcoderbase-3b) in GGUF format which I have quantized. Here is the download link for the [GGUF format cosmo3769/starcoderbase-3b-GGUF](https://huggingface.co/cosmo3769/starcoderbase-3b-GGUF/resolve/main/starcoderbase-3b.Q4_K_M.gguf?download=true).

![Simulator Screenshot - iPhone 15 Pro Max - 2024-03-15 at 13 09 27](https://github.com/cosmo3769/Quantized-LLMs/assets/53268607/7f46e105-dbfb-4bed-b620-ecea37f9912c)

![Simulator Screenshot - iPhone 15 Pro Max - 2024-03-15 at 13 16 46](https://github.com/cosmo3769/Quantized-LLMs/assets/53268607/d039ef82-d4c2-4d97-8199-7725c64c81ea)
