Around ten days back, OpenAI released the new gpt-4o-mini and gpt-4o-2024-08-06 models, which supports Structured JSON Outputs.
 
Here's a brief step-by-step tutorial on integrating structured outputs with OpenAI SDKs.

- Install OpenAI SDK with `pip install openai -U`.
- Import necessary libraries like `json` and `openai`.
- Create an OpenAI client instance using `client = OpenAI()`.
- You can use Structured Outputs in two ways:￼￼**a) When you use function calling, supply `strict: true` within your function definition** to ensure that the model’s output will match your exact schema.￼**b) You can now supply a `json_schema` as a `response_format` option**, along with a full definition of your schema. Set `strict: true` to ensure that model outputs will reliably match your schema.
- In the example code below we implement the option b above, using a `json_schema` for the `response_format` option and `strict: true`
- Use `client.chat.completions.create()` to send a request, including the model, messages, and response format.
- Extract and parse the structured response from `response.choices.message`.
 \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzQVzFXtwpdsfmdXhGVZJncjcdnF](https://mail.google.com/mail/u/0/#inbox/FMfcgzQVzFXtwpdsfmdXhGVZJncjcdnF)\>      
[https://colab.research.google.com/drive/1u8OFl2SoBku3gF0XkmLpN8wK09aVbdLN?usp=sharing](https://colab.research.google.com/drive/1u8OFl2SoBku3gF0XkmLpN8wK09aVbdLN?usp=sharing)