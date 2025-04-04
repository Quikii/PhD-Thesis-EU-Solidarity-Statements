# PhD-Thesis-EU-Solidarity-Statements

**Provisional Code Repository includes:**

1. **Preprocessing Code**
    - **Resolve Coreferences**
        - Eventually to be used as additional info for the LLM analysis  
    - **Extract Statements about Specific Countries**
    - **Extract Objects and Subjects of Sentences**
    - **Parallelization**

2. **Pre-Training LLM Code** 
    - Using unsloth interface to quantize and pre-train the free LLM model
        - Increases the performance significantly, also demands less RAM
    - So far: Llama 3.2 3B -> The goal would be to do this with several LLMs and average over the results
        - Based on the idea from the workshop paper 
    - **Missing:** Gemma, Phi.

4. **Running the Pre-trained LLM**
    - **Prompt Specification**
        - **Solidarity Speech Acts**
            - Extract Solidarity Statements -> Ran a first test run with 1000 inputs and technically it works well
            - Code Them as Speech Acts -> More complex, worked in preliminary tests
    - **Missing:** Tracking version control, incorporation of AI interpretability, testing optimally performing prompt
      
5. **Finetuning BERT**
    -  Using the aggregated LLM output to then finetune a BERT model
        - So dar done with EUROBert
    - The idea again would be to do this with several BERT-based models and extract average (for additional robustness) 

6. **Embeddings**
    - Training word and sentence embeddings on the corpus to extract differences between groups of countries
        - The underlying idea is to extract cosine similarity and infer from that linguistic inclusion
        - If we speak similarly about the countries -> they are more part of the European space 
