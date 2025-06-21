# Draw.io Corporate Minimalist Style Guide

## Overview
Professional, grayscale Draw.io diagrams for enterprise environments. Prioritizes clarity, accessibility, and timeless aesthetics.

## Design Principles
- Form follows function
- High contrast (4.5:1 minimum)
- No decorative elements
- Consistent visual language

## Canvas Settings
- **Grid Size**: 20px
- **Canvas**: 1600x1200
- **Shadow**: Disabled
- **Guides**: Enabled

## Color Palette

| Element | Color | Usage |
|---------|-------|-------|
| **Text Primary** | `#212529` | Headers, main content |
| **Text Secondary** | `#495057` | Labels, descriptions |
| **Text Tertiary** | `#6c757d` | Supporting text |
| **Component Fill** | `#ffffff` | Main components |
| **Layer Fill L2** | `#f8f9fa` | Subgraph backgrounds |
| **Layer Fill L3** | `#e9ecef` | External services |
| **Layer Fill L4** | `#dee2e6` | Secondary layers |
| **Border Primary** | `#495057` | Component borders |
| **Border Secondary** | `#6c757d` | External borders |

## Typography
- **Title**: 20px, bold
- **Layer Headers**: 16px, bold
- **Components**: 14px, normal
- **Labels**: 12px, normal
- **Text Color**: Primary text (`#212529`)

## Components

### Layer Containers
- **Dimensions**: 280×180px
- **Header**: 60px height
- **Stroke**: 2px width
- **Fill**: Progressive gray scale
- **Corners**: Sharp edges (no rounding)

### Component Boxes
- **Dimensions**: 200×80px
- **Fill**: White (`#ffffff`)
- **Stroke**: 1px primary border
- **Corners**: Sharp edges
- **Margins**: 40px from layer edges

### External Services
- **Dimensions**: 240×100px
- **Fill**: Light gray (`#f8f9fa`)
- **Stroke**: 1px secondary border
- **Text**: Secondary gray (`#495057`)

## Connections

### Primary Flow
- **Width**: 3px
- **Style**: Orthogonal, sharp corners
- **Color**: Primary border (`#495057`)

### Secondary/Optional
- **Width**: 2px
- **Style**: Dashed (8-8 pattern)
- **Color**: Tertiary gray (`#6c757d`)
- **Usage**: Fallback paths

### External Services
- **Width**: 2px
- **Style**: Bidirectional arrows
- **Color**: Secondary border (`#6c757d`)

## Labels
- **Position**: Above line (-15 to -20px offset)
- **Format**: Brief, professional phrases
- **Examples**: `"API Request"`, `"Processed Data"`

## Layout
- **Direction**: Left-to-right for processes
- **Layer gap**: 400px horizontal
- **Component margins**: 40px from layer edges
- **Grid alignment**: 20px snap
- **Canvas margins**: 80px

## Export
- **Executive**: PNG, 300 DPI, white background
- **Documentation**: SVG, embedded fonts
- **Print**: PDF, grayscale, A4/Letter compatible

## Use Cases
- System architecture diagrams
- Business process flows
- Executive presentations
- Compliance documentation
- Technical specifications

## Checklist
- [ ] Grayscale only (no colors)
- [ ] 4.5:1 contrast ratio minimum
- [ ] Sharp edges (no rounded corners)
- [ ] Professional terminology
- [ ] Grid alignment consistent
- [ ] No shadows or 3D effects
- [ ] Naming: `project-name-architecture.drawio`