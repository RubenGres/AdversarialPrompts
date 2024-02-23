# AdversialPrompts

This repository contains a list of adversarial prompts for large language models using a variety of techniques. Each technique was used to extract a secret key given in the system prompt on a selection of models of different sizes.  

Extraction results are listed in the table below:

| Model\Method | Simplest | Polite | Begging | Menacing | Diversion | Obfuscation | Répétition | Context switching | Ignore | DAN |
| ----------------- |---- |---- |---- |---- |---- |---- |---- |---- |---- |---- |
| **ChatGPT 4**     |  |  |  |  |  |  |  |  |  |  |
| **ChatGPT 3.5**   |  |  |  |  |  |  |  |  |  |  |
| **Mixtral 8x7B**  |  |  |  |  |  |  |  |  |  |  |
| **LlaMa2 70B**    |  |  |  |  |  |  |  |  |  |  |
| **Gemini**        |  |  |  |  |  |  |  |  |  |  |
| **Mistral 7B**    | 80% | 20% |  0% | 60% | 90% | 70% | 90% | N/A | 20% | 80% | 
| **Gemmma 7B**     | 28% |  1% |  1% |  7% | 60% | 44% | 53% | 63% | 22% | 16% | 
| **Phi**           | 80% | 80% | 60% | 40% | 70% | 90% | 50% | N/A | 10% | 60% | 

```
pip install -r requirements.txt
```
