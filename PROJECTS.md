<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/profile-dark.png">
  <img src="assets/profile-banner.png" alt="Sahajpreet Singh Khasria — Backend &amp; Full-Stack Engineer · AI Systems &amp; Cloud Infrastructure">
</picture>

[Technology stack](#technology-stack) · [Featured work](#featured-work) · [Project directory](#project-directory)

## Hi, I’m Sahajpreet.

I build backend services and full-stack applications. For a patent research tool, I connected a Next.js frontend to AWS APIs and made long-running searches resumable. At ASU’s AI Cloud Innovation Center I worked on getting a question to the right agent, a source into the answer, and the whole thing running on AWS. Ask me about the time a chatbot found the answer and still lost the citation.

## Technology stack

**Languages**

<img src="assets/chips/python.png" width="87" height="30" alt="Python"> <img src="assets/chips/typescript.png" width="120" height="30" alt="TypeScript"> <img src="assets/chips/javascript.png" width="120" height="30" alt="JavaScript"> <img src="assets/chips/java.png" width="71" height="30" alt="Java"> <img src="assets/chips/swift.png" width="79" height="30" alt="Swift">· SQL · <img src="assets/chips/go.png" width="54" height="30" alt="Go">

**Applications**

<img src="assets/chips/react.png" width="79" height="30" alt="React"> <img src="assets/chips/next-js.png" width="95" height="30" alt="Next.js"> <img src="assets/chips/node-js.png" width="95" height="30" alt="Node.js"> <img src="assets/chips/flask.png" width="79" height="30" alt="Flask"> <img src="assets/chips/swiftui.png" width="95" height="30" alt="SwiftUI">

**Cloud & deployment**

<img src="assets/chips/aws.png" width="63" height="30" alt="AWS"> <img src="assets/chips/aws-cdk.png" width="95" height="30" alt="AWS CDK"> <img src="assets/chips/lambda.png" width="87" height="30" alt="Lambda"> <img src="assets/chips/api-gateway.png" width="128" height="30" alt="API Gateway"> <img src="assets/chips/eks-fargate.png" width="128" height="30" alt="EKS Fargate"> <img src="assets/chips/s3.png" width="54" height="30" alt="S3"> <img src="assets/chips/dynamodb.png" width="104" height="30" alt="DynamoDB"> <img src="assets/chips/docker.png" width="87" height="30" alt="Docker"> <img src="assets/chips/kubernetes.png" width="120" height="30" alt="Kubernetes"> <img src="assets/chips/google-cloud.png" width="136" height="30" alt="Google Cloud"> <img src="assets/chips/cloud-run.png" width="112" height="30" alt="Cloud Run">

**AI & retrieval**

<img src="assets/chips/bedrock.png" width="95" height="30" alt="Bedrock"> <img src="assets/chips/strands-agents-sdk.png" width="186" height="30" alt="Strands Agents SDK"> <img src="assets/chips/amazon-q.png" width="104" height="30" alt="Amazon Q"> <img src="assets/chips/vertex-ai.png" width="112" height="30" alt="Vertex AI"> <img src="assets/chips/gemini.png" width="87" height="30" alt="Gemini"> <img src="assets/chips/milvus.png" width="87" height="30" alt="Milvus">

**Data & operations**

<img src="assets/chips/postgresql.png" width="120" height="30" alt="PostgreSQL"> <img src="assets/chips/redis.png" width="79" height="30" alt="Redis"> <img src="assets/chips/gunicorn.png" width="104" height="30" alt="Gunicorn"> <img src="assets/chips/nginx.png" width="79" height="30" alt="Nginx"> <img src="assets/chips/prometheus.png" width="120" height="30" alt="Prometheus"> <img src="assets/chips/grafana.png" width="95" height="30" alt="Grafana"> <img src="assets/chips/jaeger.png" width="87" height="30" alt="Jaeger">

## Featured work

### I‑ECHO · Multi-agent RAG on AWS

I added the **EKS Fargate stack** and integrated API Gateway and the load balancer. I refined routing to specialist agents, fixed streaming behavior, and added citation handling with document links. My **10 merged PRs** also include PowerPoint-to-PDF ingestion and session management.

I‑ECHO uses AWS Bedrock and Strands to route questions about tuberculosis and agriculture to domain-specific agents. The ingestion pipeline makes uploaded slide decks available for retrieval. On the response side, I fixed how the orchestrator handles thinking tags during streaming and added an endpoint that generates links to cited documents.

[Project](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT) · [Infrastructure](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/eee2f173e37885c3e1cd0047af41467d31f0b367) · [Agent routing](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/e29dfdcff4273dce122a97500a3ff923798d6c90) · [Ingestion PR](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/5) · [Session management](https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/2)

### MLH URL Shortener · Backend performance

I added Redis redirect caching with invalidation, reduced database and serialization overhead, and tuned Gunicorn and Nginx. In the merged PR’s development benchmark, **`GET /urls` handled 76.6% more requests per second with 43.4% lower latency**. All 174 existing tests passed.

For updates, I limited database writes to the fields that changed. For list endpoints, I returned dictionaries directly to avoid constructing model objects for every row. Redirects use Redis with invalidation when a URL changes or is deleted. I also adjusted PostgreSQL WAL settings, Nginx response buffers, and Gunicorn connection reuse.

[Project](https://github.com/RETR0-OS/MLH_PE_URL_Shortener) · [Merged PR and benchmarks](https://github.com/RETR0-OS/MLH_PE_URL_Shortener/pull/16)

### HOPE · Crisis resource chatbot

I improved geographic resource search, restored missing citations by adding a retrieval step before generation, and fixed session handling so follow-up messages retained context. I also migrated inference to Amazon Nova 2 Lite.

HOPE connects users with WestCare Arizona resources. I worked on location-aware search and the location questionnaire, corrected how the first request obtains a Bedrock session ID, and carried that ID into later messages. I also fixed source display for off-topic responses, updated cross-region inference permissions, and wrote a customization guide.

[Project](https://github.com/ASUCICREPO/crisis-help-chatbot) · [Geo-search](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/fb8bcba2a0b904210f83ed26b9b847add3141556) · [Citation fix](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/608582b9c7caacad4fd37266e8bccc59ebad4f38) · [Session handling](https://github.com/ASUCICREPO/crisis-help-chatbot/commit/e0611e8585d718df4a0e717e5285fdd36367886d)

### Patent Novelty Assessment

Integrated deployment across Next.js, API Gateway, and Lambda. Added early stopping and resume for patent and literature searches, with persisted progress and clearer error feedback.

The platform searches patent databases and academic literature for prior art. I connected the frontend to handlers for agent invocation, S3 uploads, and DynamoDB-backed data. For searches that outlast a page visit, I updated polling and state persistence so users can resume an ongoing search, see the final result count, and understand when a search stopped early.

[Project](https://github.com/ASUCICREPO/Patent-Novelty-Assessment) · [Search workflow](https://github.com/ASUCICREPO/Patent-Novelty-Assessment/commit/2c0d9acb25f12c4842b3fc45811f9094c9e583b7) · [Deployment PR](https://github.com/ASUCICREPO/Patent-Novelty-Assessment/pull/23)

### NASWA Multilingual RAG Chatbot

Added CDK infrastructure and a Bedrock Lambda handler, English and Spanish selection, and conversation memory. Refactored retrieval to use Bedrock `RetrieveAndGenerate` with Guardrails.

The assistant helps National Association of State Workforce Agencies users query documents in English or Spanish and inspect the sources behind an answer. I carried the language choice into both retrieval and direct prompts, improved the mapping from retrieved documents to sources, and made follow-up queries use conversation context.

[Project](https://github.com/ASUCICREPO/multilingual-RAG-chatbot) · [Retrieval refactor](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b3fd7c69b106135ba0d7e12ab6bb6e927524b53d) · [Backend infrastructure](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b8f98f390858fe5672f2de78928056c016c28b9e) · [Conversation memory](https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/0e32b48e64f5bca3b0d0cfa10fccd29f2fd90d5b)

## Project directory

<details>
<summary>Multi-Agent Inference-Time Evaluation</summary>

Evaluated specialist agents across five question domains using techniques such as code execution and retries with error feedback. Accuracy rose from **20.5% to 26%** on 200 mixed examples.

The five domains were math, coding, planning, common sense, and future prediction. I tested generated code, fed execution errors back to the model for another attempt, and compared those results with direct generation, prompting, and voting. On 100 coding examples, execution with retries reached **32%**, compared with **25%** for direct generation. The experiments also exposed weaker approaches, including a math judge that scored below 10%.

[Project](https://github.com/SinghOPS/CSE476-Final-project#performance-results)

</details>

<details>
<summary>Guardian — The Algorithmic Auditor</summary>

AWS and Next.js fairness-auditing prototype with disparate-impact and proxy-bias checks. My commits cover project setup, CSV upload validation, test data, and architecture and testing guides.

Guardian pairs a Next.js dashboard with a Python Lambda ingestion and bias-analysis pipeline. Users upload a CSV, inspect group selection rates and disparate-impact checks, and explore the results with a Bedrock-powered Socratic tutor. I initialized the project, added upload-size validation and a sample dataset, and documented architecture, deployment, and testing.

[Project](https://github.com/SinghOPS/spark-challenge) · [CSV validation](https://github.com/SinghOPS/spark-challenge/commit/dbe1a7b03621b35eaeafb041835839333f1b6ba9)

</details>

<details>
<summary>TravelBuddy · Personalized iOS trip planner</summary>

TravelBuddy is a SwiftUI trip planner. Travelers enter their route, dates, budget, group size, and transportation preferences. Gemini builds a day-by-day itinerary, and the app organizes it into timed activities with estimated costs and travel tips.

I built the login screen and navigation, connected the trip form to the itinerary view, and integrated the APIs for itinerary generation and destination imagery.

[Project](https://github.com/SinghOPS/TravelBuddy) · [API integration](https://github.com/SinghOPS/TravelBuddy/commit/dfea0184e3fd7540500ca96f30a667488ee7fc95)

</details>

<details>
<summary>PrepU</summary>

Added a summarizer, an API module, and face and emotion analysis modules for interview tooling.

PrepU combines a React frontend with Python modules. My authored commits introduced the summarizer, API integration module, face detection, and emotion analysis, giving the project separate components for processing text and visual input.

[Project](https://github.com/SinghOPS/PrepU/commits/main/)

</details>

<details>
<summary>InterviewIQ</summary>

This React mock interview prototype pairs video playback with structured feedback on answers.

The interviewer view presents a behavioral question alongside a recorded response. It requests feedback from the interview API, displays a rating, strengths, weaknesses, and suggested improvements, and synchronizes the returned expression labels with the video timeline.

[Project](https://github.com/aryankhanna2004/InterviewIQ)

</details>

<details>
<summary>ASDA</summary>

Authored nine upstream commits, including a crawler and Flask UI updates to a Form 990 search prototype.

The prototype helps users explore nonprofit tax filings by city, state, gross revenue, and net revenue. My work spanned the JavaScript crawler and retrieval code, HTML templates and styles, and formatting changes in the Flask application.

[Project](https://github.com/daniel10015/ASDA) · [Crawler commit](https://github.com/daniel10015/ASDA/commit/52282587de8c304ee3621998b93ed6de3fac1ee1)

</details>

<details>
<summary>AWS AI Chatbot for Corrections</summary>

Updated the infrastructure deployment guide.

The project provisions an Amazon Q Business assistant with a web crawler, index, and retriever through AWS CDK. My upstream change was to the infrastructure-as-code deployment guide used to set up that stack.

[Project](https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections) · [Organization PR](https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections/pull/2)

</details>

[Browse my repositories](https://github.com/SinghOPS?tab=repositories)
