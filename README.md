![Sahajpreet Singh Khasria — Backend & Full-Stack Engineer · AI Systems & Cloud Infrastructure](assets/ink-masthead-rounded.png)

[Technology stack](#technology-stack) · [Featured work](#featured-work) · [Project directory](#project-directory)

## Hi, I’m Sahajpreet.

I build backend services and full-stack applications. For a patent research tool, I connected a Next.js frontend to AWS APIs and made long-running searches resumable. At ASU’s AI Cloud Innovation Center I worked on getting a question to the right agent, a source into the answer, and the whole thing running on AWS. Ask me about the time a chatbot found the answer and still lost the citation.

## Technology stack

<img src="assets/paper/technology-stack-sql.png" width="100%" alt="Technology stack: languages, applications, cloud and deployment, AI and retrieval, data and operations">

## Featured work

### ![I‑ECHO · Multi-agent RAG on AWS](assets/sections/rounded-feature-1.png)

I added the **EKS Fargate stack** and integrated API Gateway and the load balancer. I refined routing to specialist agents, fixed streaming behavior, and added citation handling with document links. My **10 merged PRs** also include PowerPoint-to-PDF ingestion and session management.

I‑ECHO uses AWS Bedrock and Strands to route questions about tuberculosis and agriculture to domain-specific agents. The ingestion pipeline makes uploaded slide decks available for retrieval. On the response side, I fixed how the orchestrator handles thinking tags during streaming and added an endpoint that generates links to cited documents.

[Project](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT) · [Infrastructure](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/eee2f173e37885c3e1cd0047af41467d31f0b367) · [Agent routing](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/e29dfdcff4273dce122a97500a3ff923798d6c90) · [Ingestion PR](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/5) · [Session management](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/2)

### ![MLH URL Shortener · Backend performance](assets/sections/rounded-feature-2.png)

[![Development benchmark for GET /urls: throughput up 76.6%, latency down 43.4%, 174 tests passed.](assets/mlh-benchmark.svg)](https://github.com/RETR0-OS/MLH_PE_URL_Shortener/pull/16)

I added Redis redirect caching with invalidation, reduced database and serialization overhead, and tuned Gunicorn and Nginx. In the merged PR’s development benchmark, **`GET /urls` handled 76.6% more requests per second with 43.4% lower latency**. All 174 existing tests passed.

For updates, I limited database writes to the fields that changed. For list endpoints, I returned dictionaries directly to avoid constructing model objects for every row. Redirects use Redis with invalidation when a URL changes or is deleted. I also adjusted PostgreSQL WAL settings, Nginx response buffers, and Gunicorn connection reuse.

[Project](https://github.com/RETR0-OS/MLH_PE_URL_Shortener) · [Merged PR and benchmarks](https://github.com/RETR0-OS/MLH_PE_URL_Shortener/pull/16)

### ![HOPE · Crisis resource chatbot](assets/sections/rounded-feature-3.png)

I improved geographic resource search, restored missing citations by adding a retrieval step before generation, and fixed session handling so follow-up messages retained context. I also migrated inference to Amazon Nova 2 Lite.

HOPE connects users with WestCare Arizona resources. I worked on location-aware search and the location questionnaire, corrected how the first request obtains a Bedrock session ID, and carried that ID into later messages. I also fixed source display for off-topic responses, updated cross-region inference permissions, and wrote a customization guide.

[Project](https://github.com/ASUCICREPO/crisis-help-chatbot) · [Geo-search](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/fb8bcba2a0b904210f83ed26b9b847add3141556) · [Citation fix](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/608582b9c7caacad4fd37266e8bccc59ebad4f38) · [Session handling](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/e0611e8585d718df4a0e717e5285fdd36367886d)

### ![Patent Novelty Assessment](assets/sections/rounded-feature-4.png)

Integrated deployment across Next.js, API Gateway, and Lambda. Added early stopping and resume for patent and literature searches, with persisted progress and clearer error feedback.

The platform searches patent databases and academic literature for prior art. I connected the frontend to handlers for agent invocation, S3 uploads, and DynamoDB-backed data. For searches that outlast a page visit, I updated polling and state persistence so users can resume an ongoing search, see the final result count, and understand when a search stopped early.

[Project](https://github.com/ASUCICREPO/Patent-Novelty-Assessment) · [Search workflow](https://github.com/ASUCICREPO/Patent-Novelty-Assessment/commit/2c0d9acb25f12c4842b3fc45811f9094c9e583b7) · [Deployment PR](https://github.com/ASUCICREPO/Patent-Novelty-Assessment/pull/23)

### ![NASWA Multilingual RAG Chatbot](assets/sections/rounded-feature-5.png)

Added CDK infrastructure and a Bedrock Lambda handler, English and Spanish selection, and conversation memory. Refactored retrieval to use Bedrock `RetrieveAndGenerate` with Guardrails.

The assistant helps National Association of State Workforce Agencies users query documents in English or Spanish and inspect the sources behind an answer. I carried the language choice into both retrieval and direct prompts, improved the mapping from retrieved documents to sources, and made follow-up queries use conversation context.

[Project](https://github.com/ASUCICREPO/multilingual-RAG-chatbot) · [Retrieval refactor](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b3fd7c69b106135ba0d7e12ab6bb6e927524b53d) · [Backend infrastructure](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b8f98f390858fe5672f2de78928056c016c28b9e) · [Conversation memory](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/0e32b48e64f5bca3b0d0cfa10fccd29f2fd90d5b)

## Project directory

### AI research & tooling

<details>
<summary><strong>Multi-Agent Inference-Time Evaluation</strong> · Execution retries and accuracy</summary>

[Repository](https://github.com/SinghOPS/CSE476-Final-project) · `Python`

Compare five question domains and see where execution retries improved accuracy.

Evaluated specialist agents across five question domains using techniques such as code execution and retries with error feedback. Accuracy rose from **20.5% to 26%** on 200 mixed examples.

The five domains were math, coding, planning, common sense, and future prediction. I tested generated code, fed execution errors back to the model for another attempt, and compared those results with direct generation, prompting, and voting. On 100 coding examples, execution with retries reached **32%**, compared with **25%** for direct generation. The experiments also exposed weaker approaches, including a math judge that scored below 10%.

[Project](https://github.com/SinghOPS/CSE476-Final-project#performance-results)

</details>

<details>
<summary><strong>Guardian — The Algorithmic Auditor</strong> · CSV validation and bias checks</summary>

[Repository](https://github.com/SinghOPS/spark-challenge) · `Next.js · AWS`

Audit selection rates and explore potential proxy bias with a Bedrock tutor.

AWS and Next.js fairness-auditing prototype with disparate-impact and proxy-bias checks. My commits cover project setup, CSV upload validation, test data, and architecture and testing guides.

Guardian pairs a Next.js dashboard with a Python Lambda ingestion and bias-analysis pipeline. Users upload a CSV, inspect group selection rates and disparate-impact checks, and explore the results with a Bedrock-powered Socratic tutor. I initialized the project, added upload-size validation and a sample dataset, and documented architecture, deployment, and testing.

[Project](https://github.com/SinghOPS/spark-challenge) · [CSV validation](https://github.com/SinghOPS/spark-challenge/commit/dbe1a7b03621b35eaeafb041835839333f1b6ba9)

</details>

### Applications

<details>
<summary><strong>TravelBuddy</strong> · Personalized iOS trip planner</summary>

[Repository](https://github.com/SinghOPS/TravelBuddy) · `SwiftUI · Gemini`

TravelBuddy is a SwiftUI trip planner. Travelers enter their route, dates, budget, group size, and transportation preferences. Gemini builds a day-by-day itinerary, and the app organizes it into timed activities with estimated costs and travel tips.

I built the login screen and navigation, connected the trip form to the itinerary view, and integrated the APIs for itinerary generation and destination imagery.

[Project](https://github.com/SinghOPS/TravelBuddy) · [API integration](https://github.com/SinghOPS/TravelBuddy/commit/dfea0184e3fd7540500ca96f30a667488ee7fc95)

</details>

<details>
<summary><strong>PrepU</strong> · Interview summaries and visual analysis</summary>

[Repository](https://github.com/SinghOPS/PrepU) · `React · Python`

Explore Python modules for summarizing interviews and analyzing visual input.

Added a summarizer, an API module, and face and emotion analysis modules for interview tooling.

PrepU combines a React frontend with Python modules. My authored commits introduced the summarizer, API integration module, face detection, and emotion analysis, giving the project separate components for processing text and visual input.

[Project](https://github.com/SinghOPS/PrepU/commits/main/)

</details>

<details>
<summary><strong>InterviewIQ</strong> · Video playback and feedback</summary>

[Repository](https://github.com/aryankhanna2004/InterviewIQ) · `React`

Review a recorded mock interview alongside structured feedback.

This React mock interview prototype pairs video playback with structured feedback on answers.

The interviewer view presents a behavioral question alongside a recorded response. It requests feedback from the interview API, displays a rating, strengths, weaknesses, and suggested improvements, and synchronizes the returned expression labels with the video timeline.

[Project](https://github.com/aryankhanna2004/InterviewIQ)

</details>

### Data & infrastructure

<details>
<summary><strong>ASDA</strong> · Form 990 crawler and search</summary>

[Repository](https://github.com/daniel10015/ASDA) · `Flask · JavaScript`

Search nonprofit Form 990 filings by location and revenue.

Authored nine upstream commits, including a crawler and Flask UI updates to a Form 990 search prototype.

The prototype helps users explore nonprofit tax filings by city, state, gross revenue, and net revenue. My work spanned the JavaScript crawler and retrieval code, HTML templates and styles, and formatting changes in the Flask application.

[Project](https://github.com/daniel10015/ASDA) · [Crawler commit](https://github.com/daniel10015/ASDA/commit/52282587de8c304ee3621998b93ed6de3fac1ee1)

</details>

<details>
<summary><strong>AWS AI Chatbot for Corrections</strong> · CDK deployment guide</summary>

[Repository](https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections) · `AWS CDK`

Deploy an Amazon Q Business assistant with a web crawler and search index.

Updated the infrastructure deployment guide.

The project provisions an Amazon Q Business assistant with a web crawler, index, and retriever through AWS CDK. My upstream change was to the infrastructure-as-code deployment guide used to set up that stack.

[Project](https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections) · [Organization PR](https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections/pull/2)

</details>

[Browse my repositories](https://github.com/SinghOPS?tab=repositories)

