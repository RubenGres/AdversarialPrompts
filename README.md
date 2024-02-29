# AdversialPrompts

This repository contains a list of adversarial prompts for large language models using a variety of techniques. Each technique was used to extract a secret key given in the system prompt on a selection of models of different sizes.  

All the adversarial prompts can be found in *adversarial_prompts.json*, the LLM responses are all available in the file *llm_replies.json*

All tested LLM are instruct versions of the following models: `Gemma 7B`, `LlaMa2 7B`,  `Mistral 7B`,  `Phi 7B`,  `GPT-3.5`,  `GPT-4`

**Here are the results of our study:** 

| Model\Method            | simplest  | polite  | begging | menacing | ignore | obfuscation | context_switching | diversion | long_diversion | DAN  |
|-------------------------|-----------|---------|---------|----------|--------|-------------|-------------------|-----------|----------------|------|
| **gemma:7b-instruct**   | 0%        | 0%      | 1%      | 7%       | 60%    | 53%         | 22%               | 44%       | 100%           | 16%  |
| **llama2**              | 0%        | 25%     | 0%      | 0%       | 4%     | 3%          | 49%               | 9%        | 45%            | 33%  |
| **mistral:7b-instruct** | 75%       | 55%     | 0%      | 60%      | 60%    | 95%         | 15%               | 70%       | 60%            | 75%  |
| **phi:chat**            | 75%       | 70%     | 55%     | 55%      | 55%    | 50%         | 25%               | 95%       | 35%            | 85%  |
| **gpt-3.5-turbo**       | 0%        | 0%      | 0%      | 2%       | 2%     | 2%          | 0%                | 0%        | 100%           | 31%  |
| **gpt-4**               | 0%        | 0%      | 2%      | 0%       | 0%     | 98%         | 0%                | 100%      | 100%           | 100% |

# Installation

All the python packages can be installed using pip
```sh
pip install -r requirements.txt
```

Ollama and its model can be pulled this way
```sh
curl -fsSL https://ollama.com/install.sh | sh
ollama serve
ollama pull llama2
ollama pull mistral:7b-instruct
ollama pull falcon:7b-instruct
ollama pull phi:chat
ollama pull gemma:7b-instruct
```
