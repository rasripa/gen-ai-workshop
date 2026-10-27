# GenAI Workshop — July/August 2023

A hands-on generative AI workshop I built in **July and August 2023** to bring fellow AWS Solutions
Architects up to speed on building with foundation models.

**This is an archive, kept deliberately.** It is a snapshot of how you built generative AI
applications on AWS *before Amazon Bedrock was generally available* — when the practical path was a
SageMaker JumpStart endpoint, LangChain, and a RAG pipeline you assembled yourself. The libraries
have moved a long way since; this has not moved with them, and that's the point.

## Why it's still here

Two reasons, and neither is that the code is current.

**It's a primary source on a stack that no longer exists.** FLAN-T5-XXL and GPT-J-6B deployed as
JumpStart endpoints, embeddings served from a second endpoint, retrieval wired by hand, fine-tuning
through the SageMaker training API. If you want to see what the pre-managed-API era actually looked
like in working code rather than in retrospectives, it's here.

**It's dated.** The commit history runs 26 July to 4 August 2023 and can't be backdated. It records
peer enablement on generative AI at the point the field was still forming.

## Do not run this as-is

LangChain's public API changed substantially after 2023, several of the JumpStart model identifiers
have been retired, and nothing here has been revalidated. Expect import errors and deprecated
arguments. Read it as a historical document, or port the ideas — don't `pip install` and hope.

If you want current equivalents of this material, the workshops under my
[profile](https://github.com/rasripa) use Strands Agents, MCP and Amazon Bedrock AgentCore.

## Contents

### `reference-code/`
- **`00-langchain-basic.ipynb`** — LangChain fundamentals: prompts, chains, and calling a SageMaker
  endpoint as an LLM
- **`01-langchain_advanced.ipynb`** — retrieval-augmented generation end to end, document loaders
  (including URL loading) and prompt engineering
- **`test-py-gpt6b-deploy.ipynb`** — deploying and fine-tuning GPT-J-6B on SageMaker, then loading
  the trained artifact back from S3

### `src/`
- **`uki_ent_retail_sa-generativeai_workshop-09aug2023.ipynb`** — the workshop as delivered to the
  UKI Enterprise Retail SA team on 9 August 2023
- **`workshop_text2text_generation.ipynb`** — text-to-text generation with FLAN-T5
- **`RAGflow.png`**, **`flow.png`** — the architecture diagrams used in the session

### `data/`
Sample corpora for the retrieval exercises: Amazon SageMaker FAQs, Amazon SEC filings, a retail
product catalogue (`retail_items.csv`, `products.yaml`) and small fine-tuning datasets. All public
or synthetic.

## Credits

Built by **Rajesh Sripathi**, with contributions from
[**@Adibuer-lab**](https://github.com/Adibuer-lab) — retail data processing for better document
construction, and the prompt-engineering and URL-loader additions.

## Note

Account identifiers and bucket names in the notebooks have been replaced with placeholders. Saved
cell outputs are left in place, since the model responses of mid-2023 are part of what makes this
worth keeping.

---

A personal project. Not an official AWS project, and not supported by AWS.
