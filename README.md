# 596-final-project
**LLaMA (Large Language Model Meta AI) efficiency project proposal**


CSCI 596
Amy Kim, M.S. Computer Science
Charley Kim, M.S. Computer Science


**Abstract**
With the public, free release of ChatGPT 3.5 and other large language models, AI is being trained on larger and larger data sets with billions and potentially trillions of data points. Our project proposes running queries on different sizes of Meta’s Large Language Model Meta AI (LLaMA) using a different number of cores to measure and compare the efficiency of the models. As AI and language models are applied to more aspects of technological and daily life, developers turn to user larger data and training sets, making it important to balance the accuracy of language models with their size and efficiency. 


![download](https://github.com/amykim21/596-final-project/assets/69876199/06f7d8fb-a11a-4d34-82cd-9f6dcc52d0c3)


**Goals/Objectives:**
In a race to make the “smartest” AI, companies are focusing largely on the accuracy of their models over the efficiency. This project proposal aims to measure if the efficiency of large language models can be improved further while maintaining or improving accuracy, as trends have demonstrated data sets growing tens of times larger per iteration. We can gain insight into how real-world industry uses software tools to measure and enhance performance of their large language models and potentially see the limitations on size because of the sheer size of data sets, which AI developers do not seem to be largely concerned with yet. 


**Potential Obstacles:**
ChatGPT and other large language models (LLM) are not open source, making it difficult to modify code and run the models on different cores. LLaMA is open source and available to the public, allowing developers to apply for a license and modify code. LLaMA does require obtaining a license that is usually approved. 


**Hypothesis:**
Running queries on same-sized datasets on more cores will make runtimes shorter and more efficient, but should not affect the accuracy of responses. However, running the queries on larger datasets will increase runtime but also increase accuracy of responses. 

Our hypothesis is partially supported by Meta’s publicly published data on model size vs scores on reasoning, comprehension, math, etc. but not on runtime or efficiency statistics as those have not been disclosed by Meta.


<img width="615" alt="Screen Shot 2023-12-01 at 3 33 53 PM" src="https://github.com/amykim21/596-final-project/assets/46797363/e13bd014-a81c-4a47-9fff-525d8928c06c">


**Procedure:**
Use a set of 5 queries to ask the language model on the 7B, 13B, and 70B sizes:

What is the value of pi?
What is the weather like today?
Can you write a MongoDB query to output the geospatial coordinates that are bounded within a triangle, square, and decagon?
Please calculate the integral of (4x^(2/3))cos(x)sin(2x^3) / e^x.
Write a few paragraphs of an original fictional short story featuring a child/parent relationship. 

For each of the model sizes and queries, run the code on 1, 2, 4, and 8 cores and record the runtime as well as the answers of each and assign the answers an accuracy score from 1 - 10. 

This is an expected total of:
3 models * 5 queries * 4 cores = 60 queries

We plan to use a performance/load testing software tool which is used in industry to measure the efficiency of LLaMA. Some options that we are considering are Apache JMeter, LoadRunner, or other software tools specialized for large language models.

We hope that the results show a pattern, such as if the time cost decreases as the number of cores used increases. Such results could aid in the development process and in business decisions, potentially changing approaches to the future of AI. However, if the time cost is random and does not show a pattern, it would be inappropriate to rely on this experiment to make decisions about how to optimize a large language model’s performance.


**Potential Conclusions and Implications:**
As developers aim to make AI models even smarter, training and datasets will inevitably keep growing. This project will hopefully provide insight into whether training models on larger and larger datasets is worth increased costs, or if there might be a potential limit to improvement. With too few parameters, the model may not have enough accuracy, while too many parameters may be a waste of computational resources including processing power and memory.  Our work can potentially explore the optimal number of parameters which yield the best performance, not just for Meta’s LLaMA, but also for the wide array of AI being developed by various companies that are being integrated more and more into our daily lives. 
