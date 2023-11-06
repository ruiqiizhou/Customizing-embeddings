# Embeddings
How many embedding models Open AI provide now?

OpenAI offers a suite of embedding models accessible through its API. These models include ada, babbage, curie, and davinci, each optimized for different performance and cost considerations. For instance:

Ada: The fastest and least expensive model, suitable for quick processing and tasks where precision is less critical.

Babbage: Provides a balance between speed and cost, suitable for tasks of medium complexity.

Curie: More powerful than Babbage, suitable for more complex understanding and generation tasks.

Davinci: The most powerful model capable of handling the most complex tasks but also the most expensive.

All these models can generate embeddings for various applications such as text similarity analysis, classification, clustering, and more. OpenAI continually updates and improves their models to provide better performance and new features. If there are any new or custom-specific embedding models, they would typically be announced through OpenAI's official channels or API documentation.

# Q1: Which one is the best?

Model improvements:
Stronger performance. 'text-embedding-ada-002' outperforms all the old embedding models on text search, code search, and sentence similarity tasks and gets comparable performance on text classification. For each task category, they evaluate the models on the datasets used in old embeddings.



<img width="686" alt="Screenshot 2023-11-05 at 8 56 18 PM" src="https://github.com/ruiqiizhou/Customizing-embeddings/assets/101485360/5dd3746f-eeea-46b0-b792-3e3bee97522d">


<img width="688" alt="Screenshot 2023-11-05 at 8 56 33 PM" src="https://github.com/ruiqiizhou/Customizing-embeddings/assets/101485360/c1e04a28-aa76-4523-b806-8e90f21de02b">


<img width="681" alt="Screenshot 2023-11-05 at 8 56 46 PM" src="https://github.com/ruiqiizhou/Customizing-embeddings/assets/101485360/2fec3357-a760-4713-abec-0b650c54016b">


<img width="677" alt="Screenshot 2023-11-05 at 8 57 01 PM" src="https://github.com/ruiqiizhou/Customizing-embeddings/assets/101485360/48aed872-ca6e-432e-9a8b-057d87832911">


# Q2 Can we fine_tune OPENAI embedding models' weights?

No

# Why do we want to use Customizing-embeddings?
OpenAI's traditional embedding models, such as GPT-3 and earlier versions, have already excelled at handling language understanding tasks, particularly because they have been trained on massive datasets, enabling them to perform well on many general tasks. However, customized embeddings offer advantages that traditional embedding models may not achieve:

Specific Domain Accuracy: Traditional embedding models may not be precise enough for specialized terms and concepts in specific domains. Customized embeddings, trained on data specific to that domain, can better understand and represent nuances within that field.

Context Awareness: While models like GPT-3 are already advanced in capturing context, customized embeddings can provide a more refined understanding for complex or less common contextual usages.

Performance Optimization: In resource-constrained situations, such as when needing to run models on edge devices, customized embeddings can be optimized by reducing model size without sacrificing too much performance.

Data Privacy: When dealing with sensitive data, customized embeddings allow for local training, which means data does not need to be uploaded to the cloud, helping to enhance data privacy.

Multilingual and Cross-Cultural Capabilities: Although OpenAI's models support multiple languages, customized embeddings can offer deeper optimization for specific languages or dialects, especially those that might be underrepresented in pre-training data.

Noise and Anomaly Handling: For datasets that contain a lot of non-standard language, slang, or errors (such as social media data), customized embeddings can better adapt to these characteristics.

Therefore, although OpenAI's standard embedding models are already powerful, customized embeddings still provide significant value and performance improvements in certain specific application scenarios. This is why many businesses and research projects may choose to further optimize embedding vectors to cater to their unique needs.


# What is Customizing-embeddings?
we provide a method for customizing your embeddings using training data. The idea of the method is to train a custom matrix to multiply embedding vectors by in order to get new customized embeddings. With good training data, this custom matrix will help emphasize the features relevant to your training labels. You can equivalently consider the matrix multiplication as (a) a modification of the embeddings or (b) a modification of the distance function used to measure the distances between embeddings.
<img width="714" alt="Screenshot 2023-11-06 at 12 14 25 AM" src="https://github.com/ruiqiizhou/Customizing-embeddings/assets/101485360/8550b94c-8349-4731-94ec-85a514e3c983">



# How we use Customizing-embeddings?
https://colab.research.google.com/drive/1WGq7Czjp9UVP8OUxGjJRUT-kDTDsm0mc#scrollTo=PoTZWC1SpgkS

# Related resources from around the web
https://github.com/openai/openai-cookbook/blob/main/articles/related_resources.md

https://github.com/openai/openai-cookbook/blob/main/examples/Customizing_embeddings.ipynb

https://news.ycombinator.com/item?id=34904793

https://community.openai.com/t/customize-openai-embedding-model/224210

Self-Consistency Improves Chain of Thought Reasoning in Language Models (2022): Taking votes from multiple outputs improves accuracy even more. Voting across 40 outputs raises PaLM's score on math word problems further, from 57% to 74%, and code-davinci-002's from 60% to 78%.

Tree of Thoughts: Deliberate Problem Solving with Large Language Models (2023): Searching over trees of step by step reasoning helps even more than voting over chains of thought. It lifts GPT-4's scores on creative writing and crosswords.

Language Models are Zero-Shot Reasoners (2022): Telling instruction-following models to think step by step improves their reasoning. It lifts text-davinci-002's score on math word problems (GSM8K) from 13% to 41%.

Large Language Models Are Human-Level Prompt Engineers (2023): Automated searching over possible prompts found a prompt that lifts scores on math word problems (GSM8K) to 43%, 2 percentage points above the human-written prompt in Language Models are Zero-Shot Reasoners.

Reprompting: Automated Chain-of-Thought Prompt Inference Through Gibbs Sampling (2023): Automated searching over possible chain-of-thought prompts improved ChatGPT's scores on a few benchmarks by 0–20 percentage points.

Faithful Reasoning Using Large Language Models (2022): Reasoning can be improved by a system that combines: chains of thought generated by alternative selection and inference prompts, a halter model that chooses when to halt selection-inference loops, a value function to search over multiple reasoning paths, and sentence labels that help avoid hallucination.

