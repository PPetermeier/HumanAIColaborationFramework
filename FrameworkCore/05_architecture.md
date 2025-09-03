![](/pictures/banner_architecture.webp)

# Framework Architecture

The framework's architecture provides a structured approach to human-AI collaboration while maintaining flexibility for different needs and working styles. This document explains how the different components work together to support effective collaboration.

## Core Architecture Overview

The framework is organized into three main layers, each serving distinct but interconnected purposes. Think of these layers as the foundation, living space, and daily activities of a house - each builds upon the others to create a complete system.

```mermaid
graph TD
    %% Main Layers
    subgraph "Foundation Layer" [Foundation Layer]
        PF[Project Foundations]
        CP[Collaborator Profile]
        EG[Engagement Guidelines]
        GL[Glossary] 
        MT[Mental Tools ]
    end

    subgraph "Dynamic Layer" [Dynamic Layer]
        LQ[Living Questions]
        PP[Project Plan]

    end

    subgraph "Operational Layer" [Operational Layer]
        ST[Session Template]
        FS[First Session Template] 
        WF[Working Files]
        OCS[Onboarding Cheat Sheet] 
        QW[Quick Win Guide ] 
    end

    %% Direct Dependencies (Structural)
    PF --o LQ
    PF --o PP
    CP --o EG
    EG --o ST
    GL --o OCS
    GL --o QW
    MT --o FS
    
    %% Bidirectional Updates
    LQ <--> PP
    EG <--> OCS

    %% Operational Flow
    LQ --> ST
    PP --> ST
    ST --> LQ
    ST --> PP
    ST --> WF
    FS --> WF
    QW --> FS
    OCS --> FS

    %% Influence Relationships
    EG -.-> LQ
    CP -.-> ST
    PF -.-> ST
    GL -.-> ST
    MT -.-> LQ
    MT -.-> PP
    MT -.-> ST

    %% External Integration
    OCS -.-> CP
    QW -.-> PP

    %% Styling
    classDef foundation fill:#e6f3ff,stroke:#333,stroke-width:2px
    classDef dynamic fill:#f9f9f9,stroke:#333,stroke-width:2px
    classDef operational fill:#fff3e6,stroke:#333,stroke-width:2px
    classDef new fill:#e6ffef,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5
    
    class PF,CP,EG,MF,GL foundation
    class LQ,PP,MT dynamic
    class ST,FS,WF,OCS,QW operational
    
```


```mermaid
flowchart LR
    %% Connection Type 1: Direct Dependencies
    A1[A] --o B1[B]
    B1 ~~~ C1[Structural dependency -
    component B builds
    directly on A]
    
    %% Connection Type 2: Bidirectional Updates
    A2[A] <--> B2[B]
    B2 ~~~ C2[Continuous mutual update
    and influence
    between components]
    
    %% Connection Type 3: Operational Flow
    A3[A] --> B3[B]
    B3 ~~~ C3[Work process flow
     and information transfer]
    
    %% Connection Type 4: Influence
    A4[A] -.-> B4[B]
    B4 ~~~ C4[Indirect influence
    without structural
     dependency]
    
    %% Styling
    classDef default fill:#fff,stroke:#333
    classDef meaning fill:#fff,stroke:none
    class C1,C2,C3,C4 meaning
    
    %% Layout
    direction LR
```

### Foundation Layer

This layer establishes the basic structure for all collaboration. It includes:

Project Foundations:

- Defines core project parameters
- Establishes working principles
- Sets quality standards
- Creates basic infrastructure

Collaborator Profile:

- Documents working preferences
- Records expertise and experience
- Notes learning objectives
- Tracks development patterns

Engagement Guidelines:

- Establishes collaboration patterns
- Defines communication approaches
- Sets documentation standards
- Creates quality frameworks

Glossary:
- Defines key terms
- Ensures shared understanding  

Mental Tools:
 - First entry point for metacognitive and -cooperative practices
 - Designed to get you into practical iteration by pointing out possible entrypoints

### Dynamic Layer

This layer manages the evolving aspects of your work. It contains:

Living Questions:

- Tracks knowledge development
- Records open inquiries
- Documents insights
- Maintains understanding

Project Plan:

- Organizes work components
- Manages timelines
- Tracks progress
- Coordinates resources

### Operational Layer

This layer handles day-to-day collaboration. It includes:

Session Template:

- Structures individual sessions
- Maintains continuity
- Tracks progress
- Documents developments

Working Files:

- Contains project work
- Holds documentation
- Stores resources
- Maintains outputs

Quick Win Guide:
 - Provides immediate practical tips
 - Helps you get started quickly
 - Offers reminders for effective practices

Onboarding Cheat Sheet:
 - Summarizes key framework aspects
 - Guides initial setup
 - Supports early sessions
 - Provides quick reference

First Session Template:
 - Guides your initial working session
 - Structures first collaboration
 - Helps establish patterns
 - Documents early experiences  

## Component Relationships

Understanding how components relate helps you use them more effectively:

### Direct Dependencies

Some components build directly on others:

- Project Foundations inform Living Questions and Project Plan
- Collaborator Profile shapes Engagement Guidelines
- Engagement Guidelines structure Session Template

### Bidirectional Updates

Some components continuously influence each other:

- Living Questions and Project Plan evolve together
- Session experiences update Living Questions
- Project progress refines Project Plan

### Influence Relationships

Some components indirectly affect others:

- Engagement Guidelines influence Living Questions
- Collaborator Profile shapes Session Template
- Project Foundations guide overall development

## Practical Implementation

### Starting Simple

Begin with basic implementations:

1. Create minimal versions of each component
2. Focus on essential relationships
3. Add complexity gradually
4. Maintain clear documentation

### Growing Complexity

As your work develops:

1. Deepen component implementations
2. Strengthen relationships
3. Add sophisticated features
4. Maintain integration

### Quality Assurance

Throughout development:

1. Verify component effectiveness
2. Check relationship health
3. Validate integration
4. Ensure clarity

## Evolution and Maintenance

### Regular Review

Maintain system health through:

1. Component effectiveness checks
2. Relationship verification
3. Integration validation
4. Documentation updates

### Continuous Improvement

Support system development by:

1. Identifying enhancement needs
2. Planning improvements
3. Implementing changes
4. Validating results

## Advanced Considerations

### System Flexibility

The architecture supports:

- Different project types
- Various working styles
- Multiple complexity levels
- Diverse implementation approaches

### Integration Points

Key areas for integration:

- Component connections
- Information flow
- Process alignment
- Quality assurance

### Evolution Support

The system enables:

- Component development
- Relationship refinement
- Integration enhancement
- Capability growth

Remember that this architecture serves as a guide rather than a rigid structure. Adapt it to your needs while maintaining its essential principles and relationships.
