# BetweenLines AI Tutor - Requirements

## Product Purpose

BetweenLines is an AI-powered thinking tutor designed to help coders identify and understand the missing reasoning gap between a problem statement and its solution. The product focuses on the earliest stage of problem solving when learners are stuck and cannot see which algorithm or abstraction applies to an unfamiliar problem.

## User Problem

Beginner to intermediate coders often face a critical gap in their problem-solving journey:
- They can stare at a problem but don't know how to start
- They cannot identify which algorithm or abstraction applies
- They can implement known algorithms but struggle to derive solutions for unfamiliar problems
- They need guidance on thinking process, not just memorization of solutions

## Target Users

- **Primary**: Beginner to intermediate coders
- **Secondary**: Students practicing data structures & algorithms
- **Tertiary**: Learners who can apply known algorithms but struggle with problem recognition and abstraction

## Functional Requirements

### Core AI Capabilities
- **FR-1**: Infer thinking gaps from partial, imperfect user reasoning
- **FR-2**: Ask 2-3 diagnostic questions before suggesting any algorithm
- **FR-3**: Adapt explanation style based on how the user approaches the problem
- **FR-4**: Explain why an algorithm family fits, not how to implement it
- **FR-5**: Provide supportive, non-judgmental tutoring interactions

### MVP Scope (Version 0.1)
- **FR-6**: Support one category of problems (decision-based/hidden-structure problems)
- **FR-7**: Enable text-based interaction only
- **FR-8**: Limit to 2-3 diagnostic questions per problem session
- **FR-9**: Accept short free-form user responses
- **FR-10**: Generate output containing:
  - Identified reasoning gap
  - Explanation of missing abstraction
  - Hint toward algorithm family (no solution, no code)

### User Interaction Flow
- **FR-11**: Present problem statement to user
- **FR-12**: Collect initial user thoughts/approach
- **FR-13**: Ask targeted diagnostic questions based on user response
- **FR-14**: Analyze user reasoning to identify gaps
- **FR-15**: Provide explanatory feedback on missing concepts
- **FR-16**: Guide toward appropriate algorithm family without giving solutions

## Non-Functional Requirements

### Usability
- **NFR-1**: Responses must be clear and accessible to beginner programmers
- **NFR-2**: Interface should encourage exploration without fear of judgment
- **NFR-3**: Interaction flow should feel conversational and natural
- **NFR-4**: System should respond within 5 seconds for optimal learning flow

### Ethical Constraints
- **NFR-5**: Must not provide complete solutions or code implementations
- **NFR-6**: Should not enable interview cheating or academic dishonesty
- **NFR-7**: Must focus on teaching thinking process over memorization
- **NFR-8**: Should maintain educational integrity by promoting understanding

### Quality
- **NFR-9**: AI responses must be pedagogically sound and accurate
- **NFR-10**: System should handle ambiguous or incomplete user inputs gracefully
- **NFR-11**: Diagnostic questions should be relevant and insightful

## Explicit Out-of-Scope Items

### Version 0.1 Exclusions
- **OOS-1**: Code generation or implementation details
- **OOS-2**: Full problem solutions
- **OOS-3**: Multiple algorithm categories beyond decision-based problems
- **OOS-4**: User accounts or analytics tracking
- **OOS-5**: Custom model training or fine-tuning
- **OOS-6**: Visual or multimedia interactions
- **OOS-7**: Real-time collaboration features
- **OOS-8**: Progress tracking or gamification
- **OOS-9**: Integration with coding platforms or IDEs

## Success Criteria for MVP

### Learning Effectiveness
- **SC-1**: Users can identify at least one new reasoning approach after interaction
- **SC-2**: Users report improved confidence in approaching similar problems
- **SC-3**: System successfully identifies reasoning gaps in 80% of interactions

### User Experience
- **SC-4**: Average session completion rate above 70%
- **SC-5**: Users find explanations helpful and non-judgmental
- **SC-6**: Diagnostic questions feel relevant and insightful to users

### Technical Performance
- **SC-7**: System handles various types of user input without breaking
- **SC-8**: Response quality remains consistent across different problem approaches
- **SC-9**: AI maintains focus on teaching thinking rather than providing solutions

## Acceptance Criteria

### AC-1: Problem Analysis
- Given a decision-based problem statement
- When user provides initial thoughts or confusion
- Then system identifies specific reasoning gaps in user's approach

### AC-2: Diagnostic Questioning
- Given user's initial problem approach
- When system detects reasoning gaps
- Then system asks 2-3 targeted questions to understand thinking process

### AC-3: Educational Guidance
- Given user responses to diagnostic questions
- When system has identified the reasoning gap
- Then system explains missing abstraction and hints at algorithm family without giving solution

### AC-4: Non-Solution Constraint
- Given any user interaction
- When system provides guidance
- Then system never provides complete code or step-by-step implementation

### AC-5: Adaptive Communication
- Given different user communication styles
- When system responds
- Then system adapts explanation complexity and tone to match user's level