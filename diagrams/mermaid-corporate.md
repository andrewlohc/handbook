# Mermaid Corporate Minimalist Style Guide

## Overview
Professional, grayscale Mermaid diagrams for enterprise environments. Prioritizes clarity, accessibility, and timeless aesthetics.

## Design Principles
- Form follows function
- High contrast (4.5:1 minimum)
- No decorative elements
- Consistent visual language

## Color Palette

| Element | Color | Usage |
|---------|-------|-------|
| **Text Primary** | `#212529` | Headers, main content |
| **Text Secondary** | `#495057` | Labels, descriptions |
| **Text Tertiary** | `#6c757d` | Supporting text |
| **Component Fill** | `#ffffff` | Main components |
| **Layer Fill** | `#f8f9fa` | Subgraph backgrounds |
| **External Fill** | `#e9ecef` | Third-party services |
| **Border Primary** | `#495057` | Component borders |
| **Border Secondary** | `#6c757d` | External borders |

## Styles

```mermaid
// Layer containers
classDef layerStyle fill:#f8f9fa,stroke:#495057,stroke-width:2px,color:#212529,font-weight:bold

// Main components  
classDef componentStyle fill:#ffffff,stroke:#495057,stroke-width:1px,color:#212529

// External services
classDef externalStyle fill:#e9ecef,stroke:#6c757d,stroke-width:1px,color:#495057
```

## Connections

```mermaid
A -->|"Primary"| B     // Solid arrows
A -.->|"Optional"| B   // Dashed for fallback
A <-->|"Exchange"| B   // Bidirectional
```

## Labeling

### Components
- **Format**: `"Primary Name<br/>Description"`
- **Style**: Title Case for names, sentence case for descriptions

### Layers
- **Format**: `"LAYER NAME"` (ALL CAPS)
- **Examples**: `"INPUT LAYER"`, `"PROCESSING LAYER"`

### Connections
- **Brief phrases** in quotes
- **Examples**: `"API Request"`, `"Processed Data"`

## Layout

- **Direction**: LR (left-to-right) for processes, TD for hierarchies
- **Grouping**: Logical layers using subgraphs
- **Flow**: Sequential progression

## Template

```mermaid
flowchart LR
    subgraph L1 ["INPUT LAYER"]
        INPUT["Input Component<br/>Description"]
    end
    
    subgraph L2 ["PROCESSING LAYER"]
        PROCESS["Process Component<br/>Main Logic"]
    end
    
    subgraph L3 ["EXTERNAL LAYER"]
        API["External API<br/>Third-party Service"]
    end
    
    subgraph L4 ["OUTPUT LAYER"]
        OUTPUT["Output Component<br/>Final Result"]
    end
    
    INPUT -->|"Input Data"| PROCESS
    PROCESS -->|"API Request"| API
    API -->|"Response"| PROCESS
    PROCESS -->|"Processed Data"| OUTPUT
    
    classDef layerStyle fill:#f8f9fa,stroke:#495057,stroke-width:2px,color:#212529,font-weight:bold
    classDef componentStyle fill:#ffffff,stroke:#495057,stroke-width:1px,color:#212529
    classDef externalStyle fill:#e9ecef,stroke:#6c757d,stroke-width:1px,color:#495057
    
    class L1,L2,L4 layerStyle
    class L3 layerStyle
    class INPUT,PROCESS,OUTPUT componentStyle
    class API externalStyle
```

## Lineage/Process Flow Diagrams

For sequential processes with hierarchical detail tasks, use the lineage pattern:

### Design Pattern
- **Main timeline**: Horizontal flow with numbered phases
- **Branches**: Vertical branches from each main phase
- **Numbering**: Use "1 - ", "2 - " format to avoid markdown conflicts
- **Hierarchy**: Two levels maximum for clarity

### Styling Classes
```mermaid
classDef mainPhase fill:#6c757d,stroke:#495057,stroke-width:2px,color:#ffffff,font-weight:bold,font-size:14px
classDef subTask fill:#f8f9fa,stroke:#495057,stroke-width:1px,color:#212529,font-weight:normal,font-size:12px
```

### Template
```mermaid
flowchart LR
    %% Main Timeline
    A["1 - Phase One<br/>Primary objective"] --> B["2 - Phase Two<br/>Secondary objective"] --> C["3 - Phase Three<br/>Final objective"]
    
    %% Branches from each phase
    A --> A1["Sub-task A1<br/>Specific action"]
    A --> A2["Sub-task A2<br/>Specific action"]
    
    B --> B1["Sub-task B1<br/>Specific action"]
    B --> B2["Sub-task B2<br/>Specific action"]
    
    C --> C1["Sub-task C1<br/>Specific action"]
    C --> C2["Sub-task C2<br/>Specific action"]
    
    %% Corporate Styling Classes
    classDef mainPhase fill:#6c757d,stroke:#495057,stroke-width:2px,color:#ffffff,font-weight:bold,font-size:14px
    classDef subTask fill:#f8f9fa,stroke:#495057,stroke-width:1px,color:#212529,font-weight:normal,font-size:12px
    
    %% Apply Styling
    class A,B,C mainPhase
    class A1,A2,B1,B2,C1,C2 subTask
```

### Best Practices
- Keep branches to 2-5 items per main phase
- Use consistent labeling: "Primary Name<br/>Description"
- Avoid deep nesting (max 2 levels)
- Maintain visual balance across branches

## Use Cases
- System architecture diagrams
- Business process flows
- Data flow documentation
- API integration diagrams
- Executive presentations
- **Process evaluation workflows**
- **Sequential task breakdowns**

## Checklist

- [ ] Grayscale only (no colors)
- [ ] 4.5:1 contrast ratio minimum
- [ ] ALL CAPS layer labels
- [ ] Title Case component names
- [ ] Labeled connections
- [ ] Logical grouping
- [ ] Professional terminology