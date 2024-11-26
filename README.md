# EXP_10
## Exploring Prompting Techniques for Content Creation Using AI Models
### Aim

The aim of this experiment is to demonstrate how different prompting techniques, such as query decomposition, decision-making, and semantic filtering, can be employed in ChatGPT or similar models for generating various types of content. The objective is to understand how these techniques influence the quality, coherence, and structure of generated content like reports, articles, case studies, and creative works (e.g., comic book scripts).

### Softwares Required

Python (3.8+)

IDE: Jupyter Notebook or VS Code

Python Libraries: openai (for API access)

AI Models: OpenAI's ChatGPT API, or similar large language models

API Key: Required for OpenAI or equivalent model provider

### Experiment Design

This experiment explores different prompt structures to generate three types of content:

1.Report/Article

2.Case Study

3.Creative Work (Comic Book Script)

For each content type, we will use three different prompting techniques and analyze their impact.

#### Query Decomposition Prompt

This technique involves breaking a complex request into multiple simpler prompts to generate a comprehensive response.

##### Example Prompt:

Step 1: "Describe the impact of climate change on agriculture."
Step 2: "Explain how changes in temperature and rainfall patterns affect crop yields."
Step 3: "Summarize strategies farmers use to adapt to climate change."

#### Decision-Making Prompt

This technique directs the model to make choices based on given criteria, improving the specificity and clarity of the output.

##### Example Prompt:

"Create an article discussing remote work benefits. Focus on productivity, work-life balance, and employee satisfaction. Choose one benefit as the main theme and elaborate with supporting evidence."

#### Semantic Filtering Prompt

This approach involves using specific keywords or themes to guide the model’s response, ensuring the generated content aligns with the desired tone and style.

##### Example Prompt:

"Write a case study on a successful digital marketing campaign. Use keywords: 'target audience,' 'conversion rate,' and 'social media engagement.' Maintain a formal and analytical tone."

### Code

Python Code for Content Generation

This code demonstrates how to use OpenAI's API with different prompting techniques for generating content. import openai

OpenAI API Key

openai.api_key = "your_openai_api_key"

Function to generate content using a specific prompt def generate_content(prompt):

response = openai.ChatCompletion.create( model="gpt-4",

messages=[{"role": "user", "content": prompt}], max_tokens=500,

temperature=0.7

)

return response.choices[0].message['content']

Define Prompts query_decomposition_prompt = (

"Describe the impact of climate change on agriculture. "

"Then explain how changes in temperature and rainfall patterns affect crop yields. " "Finally, summarize strategies farmers use to adapt to climate change."

)

decision_making_prompt = (

"Create an article discussing remote work benefits. Focus on productivity, work-life balance, "

"and employee satisfaction. Choose one benefit as the main theme and elaborate with supporting evidence."

)

semantic_filtering_prompt = (

"Write a case study on a successful digital marketing campaign. Use keywords: "

"'target audience,' 'conversion rate,' and 'social media engagement.' Maintain a formal and analytical tone."

)

Generate Content

query_decomposition_output = generate_content(query_decomposition_prompt) decision_making_output = generate_content(decision_making_prompt) semantic_filtering_output = generate_content(semantic_filtering_prompt)

Display Results

print("Query Decomposition Output:\n", query_decomposition_output, "\n") print("Decision-Making Output:\n", decision_making_output, "\n") print("Semantic Filtering Output:\n", semantic_filtering_output, "\n")

### Output and Result
The content generated using each prompting technique will differ in structure, focus, and detail:

Query Decomposition: Provides a comprehensive response by addressing each part of the query in sequence, resulting in detailed and well-organized content.

Decision-Making: The content focuses on a specific theme, providing a clear and concise response with relevant supporting evidence.

Semantic Filtering: The response uses the specified keywords and adheres to the desired tone, ensuring alignment with the intended purpose.

### Expected Results:

Query Decomposition: Clear, logical flow with thorough coverage of the topic.

Decision-Making: Focused content with in-depth analysis of a chosen aspect.

Semantic Filtering: Targeted content that aligns with specified themes and keywords.
