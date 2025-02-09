# **Inference Phi-3 in Android**

Let’s explore how you can perform inference with Phi-3-mini on Android devices. Phi-3-mini is a new series of models from Microsoft that enables deployment of Large Language Models (LLMs) on edge devices and IoT devices. 

## Semantic Kernel and Inference:
[Semantic Kernel](https://github.com/microsoft/semantic-kernel) is an application framework that allows you to create applications compatible with Azure OpenAI Service, OpenAI models, and even local models. If your new to Semantic Kernel we suggest you look at the [Semantic Kernel Cookbook](https://github.com/microsoft/SemanticKernelCookBook?WT.mc_id=aiml-138114-kinfeylo)

### To access Phi-3-mini using Semantic Kernel:
You can combine it with the Hugging face Connector in Semantic Kernel. [Sample Code](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/semantickernel?WT.mc_id=aiml-138114-kinfeylo)

By default, it corresponds to the model ID on Hugging face. However, you can also connect to a locally built Phi-3-mini model server.

### Calling Quantized Models with Ollama or LlamaEdge:

Many users prefer using quantized models to run models locally.
[Ollama](https://ollama.com/) and [LlamaEdge](https://llamaedge.com) allow individual users to call different quantized models:

**Ollama**

You can directly run ollama run Phi-3 or configure it offline by creating a Modelfile with the path to your gguf file.

```
FROM {Add your gguf file path}
TEMPLATE \"\"\"<|user|> {{.Prompt}}<|end|> <|assistant|>\"\"\"
PARAMETER stop <|end|>
PARAMETER num_ctx 4096

```
[Sample Code](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/ollama?WT.mc_id=aiml-138114-kinfeylo)

**LlamaEdge** 

If you want to use gguf in the cloud and edge devices simultaneously, LlamaEdge is a great choice.
[Sample code](https://github.com/Azure-Samples/Phi-3MiniSamples/tree/main/wasm?WT.mc_id=aiml-138114-kinfeylo)

### Install and Run on Android Phones:
Download the MLC Chat app (Free) for Android phones.
You’ll need to download the APK file (148MB) and install it.
Launch the MLC Chat app, and you’ll see a list of AI models, including Phi-3-mini.

In summary, Phi-3-mini opens up exciting possibilities for generative AI on edge devices, and you can start exploring its capabilities on Android.