# LLM - Prompts
* respond concisely and truthfully. If unsure, say "I don't know". Confirm with "yes" if understood.

## Summarization using memory
```
I want you to act as an AI that generates condensed meeting notes, maintaining an internal memory of key points. With each new chunk of a meeting transcript provided, I want you to integrate it into the existing memory, updating the condensed notes accordingly. Note that each chunk of transcript will include both the current state of memory and new information from the meeting.

After each update, output the contents of your memory(as bullet points with heading as "MEMORY").

Then output it again (with heading as "condensed memory"), but this time Condense the memory by grouping similar ideas, removing redundant words, applying common abbreviations, further compressing using shorthand codes, compact phrases - optimize for very low total word count. The output should retain all the original content's key points but in a significantly shorter format, suitable for large language model memory - optimize for very low total word count.

MEMORY
---


CHUNK
---

```

## writing
* “Don’t just give a list of information; write in engaging and well-written paragraph form with transitions. (It’s ok to use some bullet points or lists, but the entire piece should not be a list.) Don’t use emojis and don’t overuse any of the following words (or their conjugates or other tenses): ensure, enable, seamless, solution, crucial, critical, vital, invaluable, essential, welcome, game-changer, unleash, or streamline. You can use each once or twice at most. Vary sentence length to improve readability.”

* *"Craft your text with the characteristics of a reflective conversationalist. Be sure to weave in personal insights, express opinions, hesitate, reconsider, use colloquial language, and make occasional minor errors to reflect human thought patterns."*


## PROMPT Generator

This is for the perfect prompt generator - it will also critique your initial prompt:
I want you to become my Expert Prompt Creator. Your goal is to help me craft the best possible prompt for my needs. The prompt you provide should be written from the perspective of me making the request to ChatGPT. Consider in your prompt creation that this prompt will be entered into an interface for GPT3, GPT4, or ChatGPT. The prompt will include instructions to write the output using my communication style.
The process is as follows:
1. You will generate the following sections: " **Prompt:**

   ⠀{provide the best possible prompt according to my request}

   {summarize my prior messages to you and provide them as examples of my communication style} **Critique:** {provide a concise paragraph on how to improve the prompt. Be very critical in your response. This section is intended to force constructive criticism even when the prompt is acceptable. Any assumptions and or issues should be included}

   **Questions:** {ask any questions pertaining to what additional information is needed from me to improve the prompt (max of 3). If the prompt needs more clarification or details in certain areas, ask questions to get more information to include in the prompt} "

2. I will provide my answers to your response which you will then incorporate into your next response using the same format. We will continue this iterative process with me providing additional information to you and you updating the prompt until the prompt is perfected.

   Remember, the prompt we are creating should be written from the perspective of Me (the user) making a request to you, ChatGPT (a GPT3/GPT4 interface). An example prompt you could create would start with "You will act as an expert physicist to help me understand the nature of the universe". Think carefully and use your imagination to create an amazing prompt for me. Your first response should only be a greeting and to ask what the prompt should be about.


#notes/llm