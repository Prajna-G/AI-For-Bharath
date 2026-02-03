# BetweenLines AI Tutor - Design Document

## System Overview

BetweenLines is a conversational AI tutoring system that helps coders bridge the reasoning gap between problem statements and algorithmic solutions. The system uses diagnostic questioning and adaptive explanations to guide learners toward understanding problem-solving approaches without providing direct solutions.

### Architecture Philosophy
- **Thinking-First**: Prioritize understanding reasoning process over solution delivery
- **Non-Cheating**: Maintain educational integrity by avoiding complete solutions
- **Adaptive**: Tailor explanations to individual learning styles and knowledge levels
- **Diagnostic**: Use targeted questioning to identify specific reasoning gaps

## Key Components

### 1. User Interface Layer
- **Text-based conversational interface**
- **Problem presentation module**: Displays problem statements clearly
- **Response collection system**: Captures user's free-form reasoning attempts
- **Feedback display**: Shows AI guidance and explanations

### 2. AI Interaction Layer
- **Input processor**: Parses and normalizes user responses
- **Context manager**: Maintains conversation state and user reasoning history
- **Response generator**: Formats AI output for optimal learning experience
- **Session controller**: Manages interaction flow and timing

### 3. Reasoning Analysis Engine
- **Gap detection module**: Identifies missing concepts in user reasoning
- **Question generator**: Creates targeted diagnostic questions
- **Abstraction mapper**: Links problems to appropriate algorithm families
- **Explanation synthesizer**: Generates educational content without solutions

### 4. Knowledge Base
- **Problem categorization**: Decision-based/hidden-structure problem types
- **Algorithm family mappings**: Connects problem patterns to solution approaches
- **Diagnostic question templates**: Structured questioning strategies
- **Explanation frameworks**: Educational content templates

## User Interaction Flow

### Phase 1: Problem Introduction
1. **System presents problem statement**
   - Clear, focused problem description
   - Minimal context to avoid overwhelming user
   
2. **User provides initial thoughts**
   - Free-form response about approach or confusion
   - No pressure for correct answers

### Phase 2: Diagnostic Questioning
3. **System analyzes user response**
   - Identifies reasoning patterns and gaps
   - Determines appropriate diagnostic strategy
   
4. **System asks targeted questions (2-3 maximum)**
   - Questions designed to reveal thinking process
   - Focus on understanding, not testing knowledge
   
5. **User responds to each question**
   - Short, honest answers about their reasoning
   - System encourages exploration over correctness

### Phase 3: Educational Guidance
6. **System identifies core reasoning gap**
   - Synthesizes user responses to pinpoint missing concept
   - Connects gap to broader problem-solving patterns
   
7. **System provides educational explanation**
   - Explains the missing abstraction or approach
   - Hints toward relevant algorithm family
   - Maintains focus on "why" rather than "how"

## AI Reasoning Workflow

### 1. Input Analysis
```
User Response → Parse Intent → Extract Reasoning Patterns → Identify Confidence Level
```

### 2. Gap Detection
```
Reasoning Patterns → Compare to Problem Requirements → Identify Missing Concepts → Prioritize Gaps
```

### 3. Diagnostic Strategy
```
Priority Gaps → Select Question Type → Generate Specific Question → Predict Learning Path
```

### 4. Response Synthesis
```
User Answers → Update Gap Analysis → Generate Explanation → Format for User Level
```

## Model Usage Strategy

### LLM Integration
- **External API approach**: Use existing LLM via API calls (LLM providers via API)
- **No custom training**: Rely on prompt engineering and context management
- **Structured prompting**: Use consistent templates for different interaction phases

### Prompt Engineering Framework
- **System prompts**: Define tutoring persona and constraints
- **Context injection**: Include problem type, user history, and current phase
- **Output formatting**: Structure responses for consistency and clarity
- **Safety constraints**: Prevent solution leakage and maintain educational focus

### Response Processing
- **Content filtering**: Ensure no complete solutions in output
- **Quality validation**: Check for educational value and appropriateness
- **Adaptive formatting**: Adjust complexity based on user responses

## Design Principles

### 1. Thinking-First Approach
- Always prioritize understanding over solution delivery
- Guide users to discover insights rather than providing answers
- Focus on reasoning process development

### 2. Non-Cheating Commitment
- Never provide complete implementations or solutions
- Maintain clear boundaries between guidance and cheating
- Support learning without enabling academic dishonesty

### 3. Adaptive Explanations
- Tailor communication style to user's demonstrated level
- Adjust complexity based on user responses and confusion
- Provide multiple explanation approaches when needed

### 4. Diagnostic Precision
- Use targeted questions to identify specific knowledge gaps
- Avoid generic or overly broad questioning
- Focus diagnostic effort on most impactful learning opportunities

## MVP Limitations and Constraints

### Current Scope Boundaries
- **Single problem category**: Decision-based/hidden-structure problems only
- **Text-only interaction**: No visual aids, diagrams, or multimedia
- **Limited session depth**: 2-3 diagnostic questions maximum
- **No persistence**: Sessions are independent with no user history

### Technical Constraints
- **API dependency**: Relies on external LLM service availability
- **Response latency**: Subject to API response times
- **Context limitations**: Bounded by LLM context window size
- **No custom training**: Limited to prompt engineering approaches

## Future Extensibility

### Planned Enhancements
- **Multiple problem categories**: Graph algorithms, dynamic programming, etc.
- **Visual problem representation**: Diagrams and interactive elements
- **User progress tracking**: Learning analytics and improvement metrics
- **Personalized learning paths**: Adaptive curriculum based on user strengths
- **Subject to ethical review**: All enhancements will undergo ethical evaluation to maintain educational integrity

### Technical Evolution
- **Custom model fine-tuning**: Domain-specific AI training
- **Advanced reasoning engines**: More sophisticated gap detection
- **Integration capabilities**: Connect with coding platforms and IDEs
- **Real-time collaboration**: Multi-user learning sessions

## Correctness Properties

### Property 1: Solution Avoidance
**Specification**: The system must never provide complete problem solutions or implementation code.
**Validation**: All system outputs are checked to ensure no complete algorithmic implementations are present.

### Property 2: Educational Value
**Specification**: Every system response must contribute to user's understanding of problem-solving approaches.
**Validation**: Responses contain explanatory content that helps users understand reasoning processes.

### Property 3: Diagnostic Accuracy
**Specification**: System questions must be relevant to identified reasoning gaps.
**Validation**: Generated questions directly address gaps detected in user's reasoning patterns.

### Property 4: Adaptive Communication
**Specification**: System explanations must match the complexity level demonstrated by user responses.
**Validation**: Response complexity correlates with user's demonstrated understanding level.

## Testing Strategy

### Unit Testing
- Input parsing and validation
- Gap detection algorithms
- Question generation logic
- Response formatting functions

### Integration Testing
- End-to-end conversation flows
- LLM API integration
- Context management across interactions
- Educational constraint enforcement

### Property-Based Testing
- Solution avoidance verification across all possible inputs
- Educational value assessment for generated responses
- Diagnostic question relevance validation
- Adaptive communication consistency testing