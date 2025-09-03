#### Task-Based Approach

Remember our discussion of the Pattern Completion and Statistical Simulator models? These help us understand why a structured task approach works so well with LLMs.

Let's start with a simple but powerful framework for analyzing any task before creating a prompt:

1. **Task classification**: What type of task is this?
   - Generation (creating new content)
   - Transformation (changing existing content)
   - Analysis (examining information)
   - Decision support (evaluating options)

2. **Input-output specification**: What exactly are you providing, and what do you want to receive?
   - Input format and detail level
   - Desired output format, length, style
   - Specific elements that must be included

3. **Constraint identification**: What limitations or requirements apply?
   - Factual boundaries
   - Stylistic requirements
   - Ethical considerations
   - Format necessities

4. **Success criteria**: How will you know if the output is successful?
   - Accuracy needs
   - Relevance requirements
   - Completeness expectations
   - Appropriate style/tone

**Example Transformation**:

*Before (vague prompt):*
"Give me marketing ideas for our new product."

*After (structured prompt):*
"I need 3-5 marketing campaign concepts for our new productivity app targeting remote professionals. For each concept, include:

- A campaign headline
- The primary value proposition highlighted
- The recommended channel (social, email, etc.)
- A brief description of the visual approach

Our brand voice is friendly yet professional, and we want to emphasize work-life balance benefits. Each concept should be distinctive in its approach."

Notice how the structured prompt provides clear directions on the task type, expected output, specific constraints, and implied criteria for success.

#### Context Setting Techniques

Drawing from our Context Window and Mirror models, we know that providing appropriate context significantly improves LLM performance.

Effective context setting includes:

1. **Role assignment**:
   "Act as an experienced data analyst examining quarterly performance metrics."

2. **Audience specification**:
   "The analysis will be presented to our executive team, who need strategic insights rather than technical details."

3. **Purpose clarification**:
   "This analysis will inform our Q2 resource allocation decisions."

4. **Background information**:
   "Our company has been experiencing rapid growth but facing increasing customer acquisition costs."

**Example Application:**

*Basic request:*
"Help me write an email to a customer who's had a technical issue."

*With context setting:*
"Act as a customer success specialist with experience in technical problem resolution. Help me draft an email to a customer who has experienced login failures with our SaaS platform for the past two days. The audience is a non-technical small business owner who is frustrated but has been a loyal customer for three years. The purpose of this email is to reassure them that we're addressing the issue while providing a temporary workaround they can use immediately. Our company voice is helpful, empathetic, and clear."

#### Structure Control Methods

These techniques ensure you receive outputs in exactly the format you need, making them immediately useful in your workflow.

1. **Template specification**:
   "Please format your response as a three-column table with headers: Feature | Benefit | Implementation Difficulty (Low/Medium/High)"

2. **Sequential instructions for complex outputs**:
   "First, summarize the key findings in 2-3 sentences. Then, list the top three insights as bullet points. Finally, provide a brief recommendation section with 1-2 specific next steps."

3. **Format demonstrations through examples (few-shot prompting)**:
   "Please analyze the following customer feedback in the same format as this example:

   Example:
   Feedback: 'Your checkout process is confusing and took too long.'
   Issue Category: User Experience
   Severity: High
   Suggested Action: Simplify checkout flow and reduce steps
   Business Impact: Potential increase in cart abandonment

   Now analyze this feedback:
   'I couldn't find information about shipping costs until after I entered my credit card.'"

#### A note on outputs

Asking for specific file types

#### Advanced Enhancement Techniques

Based on our Tool-with-Feedback-Loop and Augmented Cognition models, we can implement more sophisticated techniques:

1. **Chain-of-thought prompting** improves complex reasoning by guiding the model through a step-by-step thinking process.

   *Standard prompt:*
   "What's the most effective channel for marketing our enterprise software?"

   *Chain-of-thought prompt:*
   "What's the most effective marketing channel for our enterprise software? Let's think through this step by step: First, let's consider our target audience of IT directors and their typical information sources. Next, let's evaluate different channels based on their reach to this audience. Then, we'll consider cost efficiency and measurement capabilities. Finally, we'll consider how each channel aligns with our complex sale requiring technical explanation."

2. **Breaking complex tasks into subtasks** leverages the Context Window model to manage complexity.

   Instead of: "Create a complete go-to-market plan for our new product."

   Try: "We're developing a go-to-market plan for our new product. Let's approach this in stages:
   1. First, help me outline the key components we need to address in the plan.
   2. Then, we'll work through each component individually, starting with target market definition.
   3. After that, we'll develop the positioning statement.
   4. Then we'll address pricing strategy.
   [and so on]"

3. **Self-consistency techniques** generate multiple independent paths to solving a problem and then select the most reliable answer.

   "I need to estimate the market size for our productivity app. Generate three independent approaches to calculating this estimate, showing your reasoning for each approach. Then compare the results and explain which approach you think is most reliable and why."

4. **Do 1+2 *with* the LLM** Start with a general description of what you want to work on, and what requirements need to be fulfilled. Ask for an overview of solution strategies that could be viable with trade-offs(!) and recommendations. Decide which strategy to pursue, communicate the decision and ask for a more specific plan. (e.g. a software architecture), preferable visualized (ask for that as well) Save results for yourself and the LLM, use them to start a new chat working on specific subtasks laid out in the developed plan. In essense: **Be a project manager.**

### Metaphors for typical LLM prompt Problems

*Structured to highlight the impact of specificity in prompts and core LLM concepts*

| **Metaphor Concept**       | **Too Little Detail** (Weak Prompt)                          | **Detailed** (Strong Prompt)                                 | **Key Insight**                                                                 | **Linked LLM Concept**                             |  
|----------------------------|-------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------|  
| **GPS Navigation**          | "Find me something fun."                                     | "Find a dog-friendly hiking trail under 2 miles within 15 minutes of downtown, with parking." | Specificity guides the LLM like coordinates guide a GPS.                        | Pattern Recognition & Synthesis                   |  
| **Recipe**                  | "Bake a cake."                                               | "Bake a gluten-free chocolate layer cake with raspberry filling, using almond flour, at 350°F for 25 minutes." | Missing details lead to unpredictable outputs.                                  | Prompt Engineering Fundamentals                   |  
| **Construction Blueprint**  | "Build a house."                                             | "Design a 3-bedroom modern farmhouse with an open kitchen, solar panels, and a wraparound porch." | A blueprint ensures the output matches your vision.                             | Workflow Integration & Contextual Guidance        |  
| **Camera Focus**            | "Take a photo."                                              | "Capture a close-up of a sunflower at sunset with shallow depth of field, emphasizing golden light." | Clarity in input = clarity in output.                                           | Mirror Model (Clarity in = Clarity out)           |  
| **Library Search**          | "Tell me about history."                                     | "Summarize the economic causes of the French Revolution, focusing on taxation and bread prices." | LLMs can’t “browse shelves”—they need structured queries.                       | Knowledge Boundaries & Reproduction               |  
| **Jigsaw Puzzle**           | "Put this together."                                         | "Assemble the edge pieces first, then group by color (sky blue and wheat fields)."              | Context windows are like puzzle boxes: limited space to work with.              | Context Window Model                              |  
| **Compass vs. Map**         | "Go north."                                                  | "Follow the marked trail north for 2 miles, then turn east at the oak tree."                   | Directions need milestones, not just broad strokes.                             | Iterative Feedback Loop Model                     |  
| **Translator App**          | "Translate this."                                            | "Translate this technical manual paragraph from German to casual English, preserving acronyms." | LLMs process language statistically, not intuitively.                           | Language Processing & Statistical Simulator Model |  
| **Brainstorming Partner**   | "Give me ideas."                                             | "Suggest 5 blog topics about sustainable fashion for Gen Z, focusing on affordability and TikTok trends." | LLMs augment creativity but need guardrails.                                    | Creative Assistance & Collaborative Partner Model |  
| **Mirror**                  | "Fix my hair."                                               | "Trim 2 inches off the ends, add layers starting at chin length, and thin out the bulk."         | Your prompts reflect your intent—vagueness breeds vagueness.                    | Mirror Model & Anthropomorphization Pitfalls      |  
| **Chess Game**              | "Make a move."                                               | "Protect your queen, advance the central pawns, and prepare for a kingside castle."              | Strategic prompting requires anticipating next steps.                           | Augmented Cognition & Task Delegation             |  
| **Gardening**               | "Grow plants."                                               | "Plant drought-resistant succulents in full sun, using sandy soil, and water weekly in summer."  | LLMs need “care instructions” to thrive.                                        | Knowledge Gaps & Hallucinations                   |  
| **Theater Production**     | "Put on a play."                                            | "Stage *Hamlet* in modern dress, with a 90-minute runtime, spotlighting Ophelia’s perspective in Act III." | Roles (collaborator profiles) and scene plans (project phases) ensure coherence. | Collaborator Profile & Project Plan             |  
| **Architectural Blueprint**| "Build a skyscraper."                                       | "Design a 50-story eco-tower with solar-paneled facades, earthquake resistance, and rooftop gardens."      | Foundations (project framework) require precise specifications.                | Project Foundations & Technical Infrastructure  |  
| **Symphony Orchestra**     | "Play some music."                                          | "Perform Beethoven’s 5th with strings emphasized in measures 10-25, brass muted in the finale."            | The conductor (user) guides musicians (LLM) through structured scores (prompts).| Engagement Guidelines & Iterative Processes     |  
| **Chess Strategy**         | "Win the game."                                             | "Control the center with pawns, develop knights before bishops, and prepare a queen-side castle by move 10." | Strategic planning (project steps) adapts to the board’s constraints (context). | Project Plan & Risk Management                  |  
| **Scientific Experiment**  | "Test a hypothesis."                                        | "Measure how pH levels affect enzyme activity at 37°C, using three control groups and daily data logging."  | Methodology (prompts) and peer review (feedback) ensure validity.               | Methodological Approach & Quality Standards     |  
| **Legal Contract**         | "Draft an agreement."                                       | "Create a NDA covering IP protection for 2 years, with arbitration clauses for EU jurisdictions."          | Clear terms (roles) and clauses (guidelines) prevent misunderstandings.         | Engagement Guidelines & Documentation Standards |  
| **Medical Diagnosis**      | "Check the patient."                                        | "Assess for appendicitis: order CBC, abdominal ultrasound, and rebound tenderness test. Rule out UTI."     | Symptoms (inputs) guide targeted tests (prompts) and treatment (outputs).      | Prompt Engineering & Response Evaluation        |  
| **Urban Planning**         | "Develop the city."                                         | "Zone downtown for mixed-use buildings, prioritize bike lanes on Main St., and allocate 30% green space."  | Zoning (project structure) balances infrastructure (tools) and feedback.        | Integration Architecture & Operational Structure|  
| **Recipe Development**     | "Make a dessert."                                           | "Bake a vegan chocolate mousse with aquafaba, 70% dark chocolate, and raspberry coulis. Chill for 4 hours." | Ingredients (context) and steps (prompts) must align for success.               | Work Components & Iterative Refinement          |  
| **Software SDLC**          | "Build an app."                                             | "Develop a React Native fitness tracker with GPS integration, using Agile sprints and Jest for unit tests." | Requirements (project plan) drive coding (prompts) and testing (evaluation).    | Development Patterns & Tool Integration         |  

---

### How These Align with the Templates from the Framework (Theory)

1. **Theater Production** ↔ **Collaborator Profile**: Clarifies roles (actor vs. director) like technical backgrounds in profiles.  
2. **Architectural Blueprint** ↔ **Project Foundations**: Blueprints mirror technical infrastructure and integration architecture.  
3. **Symphony Orchestra** ↔ **Engagement Guidelines**: Structured communication (sheet music) aligns with session protocols.  
4. **Chess Strategy** ↔ **Project Plan**: Milestones (checkmates) map to phased objectives and risk mitigation.  
5. **Scientific Experiment** ↔ **Methodological Approach**: Hypothesis testing reflects prompt iteration and validation.  
