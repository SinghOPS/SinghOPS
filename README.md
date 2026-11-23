<img src="assets/profile-banner.png" width="100%" alt="Sahajpreet Singh Khasria — Backend &amp; Full-Stack Engineer · AI Systems &amp; Cloud Infrastructure">

<a href="#technology-stack"><img src="assets/paper-links/technology-stack.svg" width="164" height="29" alt="Technology stack"></a> <a href="#featured-work"><img src="assets/paper-links/featured-work.svg" width="140" height="29" alt="Featured work"></a> <a href="#project-directory"><img src="assets/paper-links/project-directory.svg" width="172" height="29" alt="Project directory"></a>

<img src="assets/paper/intro.svg" width="100%" alt="Hi, I’m Sahajpreet. I build backend services and full-stack applications. For a patent research tool, I connected a Next.js frontend to AWS APIs and made long-running searches resumable. At ASU’s AI Cloud Innovation Center I worked on getting a question to the right agent, a source into the answer, and the whole thing running on AWS. Ask me about the time a chatbot found the answer and still lost the citation.">

## Technology stack

<img src="assets/paper/stack.svg" width="100%" alt="Python, TypeScript, JavaScript, Java, Swift, SQL, Go, React, Next.js, Node.js, Flask, SwiftUI, AWS, AWS CDK, Lambda, API Gateway, EKS Fargate, S3, DynamoDB, Docker, Kubernetes, Google Cloud, Cloud Run, Bedrock, Strands Agents SDK, Amazon Q, Vertex AI, Gemini, Milvus, PostgreSQL, Redis, Gunicorn, Nginx, Prometheus, Grafana, Jaeger">

## Featured work

<img src="assets/paper/i-echo-multi-agent-rag-on-aws.svg" width="100%" alt="I‑ECHO · Multi-agent RAG on AWS. I added the EKS Fargate stack and integrated API Gateway and the load balancer. I refined routing to specialist agents, fixed streaming behavior, and added citation handling with document links. My 10 merged PRs also include PowerPoint-to-PDF ingestion and session management.

I‑ECHO uses AWS Bedrock and Strands to route questions about tuberculosis and agriculture to domain-specific agents. The ingestion pipeline makes uploaded slide decks available for retrieval. On the response side, I fixed how the orchestrator handles thinking tags during streaming and added an endpoint that generates links to cited documents.">

<a href="https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/eee2f173e37885c3e1cd0047af41467d31f0b367"><img src="assets/paper-links/infrastructure.svg" width="148" height="29" alt="Infrastructure"></a> <a href="https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/commit/e29dfdcff4273dce122a97500a3ff923798d6c90"><img src="assets/paper-links/agent-routing.svg" width="140" height="29" alt="Agent routing"></a> <a href="https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/5"><img src="assets/paper-links/ingestion-pr.svg" width="132" height="29" alt="Ingestion PR"></a> <a href="https://github.com/ASUCICREPO/IECHO-RAG-CHATBOT/pull/2"><img src="assets/paper-links/session-management.svg" width="180" height="29" alt="Session management"></a>

<img src="assets/paper/mlh-url-shortener-backend-performance.svg" width="100%" alt="MLH URL Shortener · Backend performance. I added Redis redirect caching with invalidation, reduced database and serialization overhead, and tuned Gunicorn and Nginx. In the merged PR’s development benchmark, GET /urls handled 76.6% more requests per second with 43.4% lower latency. All 174 existing tests passed.

For updates, I limited database writes to the fields that changed. For list endpoints, I returned dictionaries directly to avoid constructing model objects for every row. Redirects use Redis with invalidation when a URL changes or is deleted. I also adjusted PostgreSQL WAL settings, Nginx response buffers, and Gunicorn connection reuse.">

<a href="https://github.com/RETR0-OS/MLH_PE_URL_Shortener"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/RETR0-OS/MLH_PE_URL_Shortener/pull/16"><img src="assets/paper-links/merged-pr-and-benchmarks.svg" width="228" height="29" alt="Merged PR and benchmarks"></a>

<img src="assets/paper/hope-crisis-resource-chatbot.svg" width="100%" alt="HOPE · Crisis resource chatbot. I improved geographic resource search, restored missing citations by adding a retrieval step before generation, and fixed session handling so follow-up messages retained context. I also migrated inference to Amazon Nova 2 Lite.

HOPE connects users with WestCare Arizona resources. I worked on location-aware search and the location questionnaire, corrected how the first request obtains a Bedrock session ID, and carried that ID into later messages. I also fixed source display for off-topic responses, updated cross-region inference permissions, and wrote a customization guide.">

<a href="https://github.com/ASUCICREPO/crisis-help-chatbot"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/ASUCICREPO/crisis-help-chatbot/commit/fb8bcba2a0b904210f83ed26b9b847add3141556"><img src="assets/paper-links/geo-search.svg" width="116" height="29" alt="Geo-search"></a> <a href="https://github.com/ASUCICREPO/crisis-help-chatbot/commit/608582b9c7caacad4fd37266e8bccc59ebad4f38"><img src="assets/paper-links/citation-fix.svg" width="132" height="29" alt="Citation fix"></a> <a href="https://github.com/ASUCICREPO/crisis-help-chatbot/commit/e0611e8585d718df4a0e717e5285fdd36367886d"><img src="assets/paper-links/session-handling.svg" width="164" height="29" alt="Session handling"></a>

<img src="assets/paper/patent-novelty-assessment.svg" width="100%" alt="Patent Novelty Assessment. Integrated deployment across Next.js, API Gateway, and Lambda. Added early stopping and resume for patent and literature searches, with persisted progress and clearer error feedback.

The platform searches patent databases and academic literature for prior art. I connected the frontend to handlers for agent invocation, S3 uploads, and DynamoDB-backed data. For searches that outlast a page visit, I updated polling and state persistence so users can resume an ongoing search, see the final result count, and understand when a search stopped early.">

<a href="https://github.com/ASUCICREPO/Patent-Novelty-Assessment"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/ASUCICREPO/Patent-Novelty-Assessment/commit/2c0d9acb25f12c4842b3fc45811f9094c9e583b7"><img src="assets/paper-links/search-workflow.svg" width="156" height="29" alt="Search workflow"></a> <a href="https://github.com/ASUCICREPO/Patent-Novelty-Assessment/pull/23"><img src="assets/paper-links/deployment-pr.svg" width="140" height="29" alt="Deployment PR"></a>

<img src="assets/paper/naswa-multilingual-rag-chatbot.svg" width="100%" alt="NASWA Multilingual RAG Chatbot. Added CDK infrastructure and a Bedrock Lambda handler, English and Spanish selection, and conversation memory. Refactored retrieval to use Bedrock RetrieveAndGenerate with Guardrails.

The assistant helps National Association of State Workforce Agencies users query documents in English or Spanish and inspect the sources behind an answer. I carried the language choice into both retrieval and direct prompts, improved the mapping from retrieved documents to sources, and made follow-up queries use conversation context.">

<a href="https://github.com/ASUCICREPO/multilingual-RAG-chatbot"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b3fd7c69b106135ba0d7e12ab6bb6e927524b53d"><img src="assets/paper-links/retrieval-refactor.svg" width="180" height="29" alt="Retrieval refactor"></a> <a href="https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/b8f98f390858fe5672f2de78928056c016c28b9e"><img src="assets/paper-links/backend-infrastructure.svg" width="212" height="29" alt="Backend infrastructure"></a> <a href="https://github.com/ASUCICREPO/multilingual-RAG-chatbot/commit/0e32b48e64f5bca3b0d0cfa10fccd29f2fd90d5b"><img src="assets/paper-links/conversation-memory.svg" width="188" height="29" alt="Conversation memory"></a>

## Project directory

<details>
<summary>Multi-Agent Inference-Time Evaluation</summary>

<img src="assets/paper/multi-agent-inference-time-evaluation.svg" width="100%" alt="Multi-Agent Inference-Time Evaluation. Evaluated specialist agents across five question domains using techniques such as code execution and retries with error feedback. Accuracy rose from 20.5% to 26% on 200 mixed examples.

The five domains were math, coding, planning, common sense, and future prediction. I tested generated code, fed execution errors back to the model for another attempt, and compared those results with direct generation, prompting, and voting. On 100 coding examples, execution with retries reached 32%, compared with 25% for direct generation. The experiments also exposed weaker approaches, including a math judge that scored below 10%.">

<a href="https://github.com/SinghOPS/CSE476-Final-project#performance-results"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a>

</details>

<details>
<summary>Guardian — The Algorithmic Auditor</summary>

<img src="assets/paper/guardian-the-algorithmic-auditor.svg" width="100%" alt="Guardian — The Algorithmic Auditor. AWS and Next.js fairness-auditing prototype with disparate-impact and proxy-bias checks. My commits cover project setup, CSV upload validation, test data, and architecture and testing guides.

Guardian pairs a Next.js dashboard with a Python Lambda ingestion and bias-analysis pipeline. Users upload a CSV, inspect group selection rates and disparate-impact checks, and explore the results with a Bedrock-powered Socratic tutor. I initialized the project, added upload-size validation and a sample dataset, and documented architecture, deployment, and testing.">

<a href="https://github.com/SinghOPS/spark-challenge"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/SinghOPS/spark-challenge/commit/dbe1a7b03621b35eaeafb041835839333f1b6ba9"><img src="assets/paper-links/csv-validation.svg" width="148" height="29" alt="CSV validation"></a>

</details>

<details>
<summary>TravelBuddy</summary>

<img src="assets/paper/travelbuddy.svg" width="100%" alt="TravelBuddy. Built out the Swift UI and navigation and integrated text and image generation APIs.

My iOS work included the login screen, the initial navigation flow, and integration of the screens into a working interface. I then connected both generation APIs and removed the earlier SwiftData dependency as part of that integration.">

<a href="https://github.com/SinghOPS/TravelBuddy"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/SinghOPS/TravelBuddy/commit/dfea0184e3fd7540500ca96f30a667488ee7fc95"><img src="assets/paper-links/api-integration.svg" width="156" height="29" alt="API integration"></a>

</details>

<details>
<summary>PrepU</summary>

<img src="assets/paper/prepu.svg" width="100%" alt="PrepU. Added a summarizer, an API module, and face and emotion analysis modules for interview tooling.

PrepU combines a React frontend with Python modules. My authored commits introduced the summarizer, API integration module, face detection, and emotion analysis, giving the project separate components for processing text and visual input.">

<a href="https://github.com/SinghOPS/PrepU/commits/main/"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a>

</details>

<details>
<summary>InterviewIQ</summary>

<img src="assets/paper/interviewiq.svg" width="100%" alt="InterviewIQ. This React mock interview prototype pairs video playback with structured feedback on answers.

The interviewer view presents a behavioral question alongside a recorded response. It requests feedback from the interview API, displays a rating, strengths, weaknesses, and suggested improvements, and synchronizes the returned expression labels with the video timeline.">

<a href="https://github.com/aryankhanna2004/InterviewIQ"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a>

</details>

<details>
<summary>ASDA</summary>

<img src="assets/paper/asda.svg" width="100%" alt="ASDA. Authored nine upstream commits, including a crawler and Flask UI updates to a Form 990 search prototype.

The prototype helps users explore nonprofit tax filings by city, state, gross revenue, and net revenue. My work spanned the JavaScript crawler and retrieval code, HTML templates and styles, and formatting changes in the Flask application.">

<a href="https://github.com/daniel10015/ASDA"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/daniel10015/ASDA/commit/52282587de8c304ee3621998b93ed6de3fac1ee1"><img src="assets/paper-links/crawler-commit.svg" width="148" height="29" alt="Crawler commit"></a>

</details>

<details>
<summary>AWS AI Chatbot for Corrections</summary>

<img src="assets/paper/aws-ai-chatbot-for-corrections.svg" width="100%" alt="AWS AI Chatbot for Corrections. Updated the infrastructure deployment guide.

The project provisions an Amazon Q Business assistant with a web crawler, index, and retriever through AWS CDK. My upstream change was to the infrastructure-as-code deployment guide used to set up that stack.">

<a href="https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections"><img src="assets/paper-links/project.svg" width="92" height="29" alt="Project"></a> <a href="https://github.com/ASUCICREPO/CIC-AI-Chatbot-Corrections/pull/2"><img src="assets/paper-links/organization-pr.svg" width="156" height="29" alt="Organization PR"></a>

</details>

<a href="https://github.com/SinghOPS?tab=repositories"><img src="assets/paper-links/browse-my-repositories.svg" width="212" height="29" alt="Browse my repositories"></a>
