# Transformer-RCI
Transformer RCI, is an attempt to design and develop a new novel transformer specifically, to train for intelligence and reasoning as main outcomes, in AI.

# Minimal Prototype Reasoning Engine (v0.1) - Project Transformer

[![Project Status](https://img.shields.io/badge/Status-Completed_v0.1_Prototype-brightgreen.svg)](https://)  [![Python Version](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/) [![License](https://img.shields.io/badge/License-Apache-2.0)](https://opensource.org/licenses/Apache-2.0) ## Project Description

This repository contains the code for a **Minimal Prototype Reasoning Engine (v0.1)**, developed as part of "Project Transformer RCI."  This prototype demonstrates a basic end-to-end system for answering simple mathematical problems in natural language. It integrates several key components, including:

*   **Knowledge Base (KB):** A simplified in-memory knowledge base storing math definitions and formulas. Currently focuses on basic geometry concepts like "rectangle" and "area of rectangle."
*   **Retrieval-Augmented Generation (RAG) Module (v0.1 - Keyword Retrieval):** A basic RAG module that uses keyword matching to retrieve relevant knowledge from the KB based on the input problem text.
*   **Rule-Based Symbolic Logic Module (v0.1):** A simple module that extracts numerical values from the problem text, applies retrieved math formulas, and performs basic calculations using Python's `eval()` function (for prototype purposes only).
*   **Answer Text Generation (v0.1 - T5 Decoder):** A minimal answer generation module that uses the T5 Transformer Decoder to generate a textual answer based on the numerical result from the Symbolic Logic Module.

**Goal of v0.1 Prototype:**

The primary goal of this v0.1 prototype is to demonstrate a functional, end-to-end pipeline for a reasoning engine, even in a very simplified form.  It aims to showcase the integration of key components like knowledge retrieval, symbolic reasoning, and natural language generation using Transformer models.  This prototype is a foundational step towards building more sophisticated reasoning capabilities in future versions.

**Completed Steps (for v0.1):**

This Minimal Prototype (v0.1) successfully completes the following key steps:

1.  **Setup (Step 1):** Loading T5-base Transformer models and tokenizer.
2.  **Knowledge Base Initialization (Step 2):** Creating a simplified in-memory math knowledge base.
3.  **Basic RAG Module (Keyword Retrieval) Integration (Step 3):** Implementing and testing a basic RAG module for keyword-based knowledge retrieval.
4.  **Simple Rule-Based Symbolic Logic Module Integration (Step 4):** Implementing and testing a simple symbolic logic module for formula application and calculation.
5.  **Simple Answer Text Generation with T5 Decoder Integration (Step 5):**  Integrating a minimal answer generation module using the T5 Decoder.

**Example Problem and Output:**

The prototype is currently tested with the following sample problem:

> "A rectangle has a length of 5 cm and a width of 3 cm. Calculate its area."

For this input, the prototype successfully:

*   Retrieves the "area of rectangle" formula from the Knowledge Base.
*   Extracts the length (5 cm) and width (3 cm) values from the problem text.
*   Calculates the area using the formula: 5 cm * 3 cm = 15 cm².
*   Generates a basic answer text (currently: "15.0 - 15.0 - 15.0 - 15.0 - 15.0 -").  *Note: Answer generation in v0.1 is very basic and will be improved in future versions.*

**How to Run the Prototype:**

1.  **Clone this repository:** `git clone [https://github.com/Albiemc1303/Transformer-RCI]` 
2.  **Set up a Python virtual environment (recommended):** `python -m venv .venv` and activate it (e.g., `.venv\Scripts\activate` on Windows, `source .venv/bin/activate` on Linux/macOS).
3.  **Install required Python packages:** `pip install -r requirements.txt` 
4.  **Run the main script:** `python reasoning_engine_prototype.py`

**Requirements (requirements.txt):**

1. transformers
2. torch
3. re 

**Knowledge Base (KB v0.1):**

The Knowledge Base is currently defined directly within the `reasoning_engine_prototype.py` script.  It's a simple Python dictionary. Example entries include definitions and formulas for basic geometric concepts.  See the script for the current KB entries.

**Transformer Models:**

*   **Model:** `t5-base` (T5 Transformer base model from Hugging Face Transformers library)
*   **Tokenizer:** `T5Tokenizer.from_pretrained('t5-base')`
*   **Model Class for Generation:** `T5ForConditionalGeneration.from_pretrained('t5-base')`

**Future Directions (v0.Next):**

Planned enhancements and future versions include:

*   **Improved Answer Text Generation (v0.2):** Prompt engineering, contextual input for the T5 Decoder to generate more natural and informative answers.
*   **Enhanced Symbolic Logic Module (v0.2+):** More robust variable extraction, handling more complex formulas, units, and problem types, potentially using a symbolic algebra library like `sympy`.
*   **Expanded Knowledge Base (v0.Next):**  Adding more math concepts, relationships between concepts, and improving KB structure and retrieval methods.
*   **Evaluation and Testing (Ongoing):** Creating a test set and systematically evaluating the prototype's performance.
*   **Addressing "Incorrect Inferenced Data Overlap" (v0.Next):**  Exploring methods to leverage conceptual similarity and overlap for more nuanced reasoning and answer generation (as discussed in project discussions).

**License:**

Apache-2.0 

**Contact/Author:**

Albert Mc Manus
albiemc666@hotmail.co.za

---

**3.  Customize and Enhance:**

*   **Replace placeholders:**  Fill in the bracketed placeholders above (e.g., `[repository URL]`, license information, your name, etc.).
*   **Add more details:**  Expand on any sections that you feel need more explanation. For example, you could elaborate on the limitations of v0.1, specific implementation details, or challenges you faced.
*   **Add code snippets:** You can embed code snippets within the README using triple backticks (`````) for better readability.
*   **Use Markdown formatting:**  Make use of Markdown features like headings (`#`, `##`), lists (`*`, `-`), bold (`**`), italics (`*`), links (`[link text](URL)`), and images (if you want to add any).

**After you've created your `README.md` file, please:**

*   **Commit and push it to your GitHub repository.**
*   **Share the link to your GitHub repository with me!** I'd love to see it and give you any further feedback!
