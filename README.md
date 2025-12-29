Problem Statement
Air pollution is a severe health threat in Indian cities, especially Delhi—causing respiratory problems, triggering chronic diseases, and reducing life expectancy for millions. Most citizens do not receive timely, personalized alerts or practical advice during harmful pollution surges, either because most existing solutions are too generic, inconvenient, or fail to deliver actionable guidance on platforms commonly used by the public, like Telegram.

Solution Statement
CleanAirAI is a multi-agent, LLM-powered system that automates real-time air quality interpretation, risk classification, and health advisories for urban citizens. The system fetches live AQI data for any specified city or area, intelligently interprets health risks based on user background (e.g., asthmatic, senior), and generates concise, actionable alerts. These personalized health alerts and recommendations are pushed instantly to the user's mobile via a Telegram bot—the tool most accessible for typical city dwellers.

By combining agents for data fetching, AI-based interpretation, and end-user alerting, CleanAirAI empowers users with timely information and guidance that can dramatically reduce health risks associated with pollution exposure.

Architecture
Agent Roles
AQI Fetcher Agent: Connects to live air quality APIs (WAQI) to retrieve real-time pollution data for a user’s selected city.
Interpreter Agent (LLM): Processes AQI data, analyzes threshold levels for specific user groups, and determines risk level (e.g., “Unhealthy for Sensitive Groups”).
Alert Generator Agent: Crafts a clear, actionable alert message, tailored by the Interpreter Agent’s classification and contextual details.
Health Advisor Agent: Summarizes 3-4 targeted health and safety recommendations for the current AQI/risk level, making the alert immediately actionable.
Session/Memory Manager: Manages user IDs, alert history, and session logs for personalization, future learning, and transparency.
Telegram Bot Tool: Handles seamless delivery of all notification and advisory messages to users’ mobile devices via the Telegram app.
System Workflow
1.User (or demo script) inputs a city and user group (e.g., “Delhi,” “Asthmatic”).

2.AQI Fetcher Agent grabs the latest pollution data.

3.Interpreter Agent (using an LLM) classifies health risk.

4.Alert Generator Agent formulates a Telegram-ready message.

5.Health Advisor Agent appends practical advice to the alert.

6.Telegram Bot Tool pushes the alert/advice instantly to the end user.

7.Session/Memory Manager tracks the workflow and stores key user interactions for context-aware improvements.

Core Implementation Concepts
Multi-agent coordination: Specialized agents with distinct tasks coordinate through a central workflow—enabling modularity and easy scalability.
Session & memory: User-specific sessions help persist alert history and contextualize future advice.
Tool use: Integrates external APIs (WAQI, OpenAI), Telegram APIs, and system memory—demonstrating robust tool/agent orchestration.
Observability: Built-in performance logging, alert/event logs, and customizable thresholds.
Technical Challenges & Solutions
1.Overcame cloud notebook (Kaggle) API/network restrictions by implementing a robust fallback and clear documentation of live vs. demo output.

2.Designed agent roles and handoffs for maximum reusability and transparency.

3.Modular code design makes it simple to plug in new data sources, alert channels, or additional health intelligence agents.

Value Statement
CleanAirAI makes city air quality risk actionable for the common citizen, directly improving health outcomes and empowering vulnerable groups to take timely precautions. It dramatically reduces the information-to-action time by automating risk detection, alert creation, and mobile delivery. This solution is rapidly extensible—new cities, new risk categories, and new alerting platforms can be supported with minimal extra code.

From a technical perspective, CleanAirAI illustrates best practices in modular multi-agent architecture, tool integration, session handling, and observability—making it a practical template for similar agent-powered social good projects.

Conclusion
CleanAirAI is a bold demonstration of how modern AI agents, real-time data tools, and accessible messaging apps can come together to solve urgent public health problems at urban scale. With its modular architecture, robust handling of notebook/cloud limitations, and practical focus on user benefit, it stands as a model for open, impactful agent-based AI applications for societal good.

If given more time, additional features could include predictive air quality modeling agents, multilingual alerting, more granular user personalization, and integration with local health authorities or urban IoT systems.
