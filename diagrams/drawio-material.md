# Draw.io Style Guide - Material Design

## Overview
Material Design-based style guide for professional, consistent Draw.io architecture diagrams using light fills with darker borders.

## Canvas Settings
- **Grid Size**: 20px
- **Canvas**: 1600x1200
- **Shadow**: Disabled
- **Guides**: Enabled

## Color Palette

| Type | Fill | Stroke | Usage |
|------|------|--------|-------|
| **Input** | `#e3f2fd` | `#1976d2` | User interfaces, inputs |
| **Process** | `#f3e5f5` | `#7b1fa2` | Core business logic |
| **AI/ML** | `#fce4ec` | `#c2185b` | AI services, optimization |
| **Output** | `#e8f5e8` | `#2e7d32` | Results, final outputs |
| **External** | `#fff3e0` | `#f57c00` | Third-party APIs |
| **Security** | `#ffebee` | `#d32f2f` | Auth, security |
| **Database** | `#e8f5e8` | `#388e3c` | Storage, persistence |
| **Network** | `#e1f5fe` | `#0288d1` | Communication |
| **Config** | `#f9fbe7` | `#689f38` | Settings, parameters |
| **Monitor** | `#fff8e1` | `#ffa000` | Metrics, logging |

## Typography
- **Title**: 24px, bold
- **Layer Headers**: 18px, bold
- **Components**: 16px, bold
- **Labels**: 14px, bold
- **Text Color**: Black (`#000000`)

## Components

### Swimlane Layers
- **Dimensions**: 280×180px
- **Header**: 60px height
- **Stroke**: 4px width
- **Grid aligned**: 20px snap

### Component Boxes
- **Dimensions**: 200×80px
- **Margins**: 40px from edges
- **Stroke**: 3px width
- **Rounded corners**: Enabled

## Connections

### Primary Flow
- **Width**: 6px
- **Style**: Orthogonal, rounded
- **Color**: Matches source component

### Secondary/Optional
- **Width**: 4px
- **Style**: Dashed (12-12 pattern)
- **Usage**: Fallback paths

### External Services
- **Width**: 4px
- **Style**: Bidirectional arrows
- **Color**: Orange (`#f57c00`)

## Labels
- **Position**: Above line (-20px offset)
- **Format**: Protocol/method + purpose
- **Example**: `HTTP/HTTPS\nWeb Scraping`

## Spacing
- **Layer gap**: 400px horizontal
- **Component margins**: 40px from layer edges
- **Grid alignment**: 20px snap
- **Canvas margins**: 80px

## Export
- **Presentations**: PNG, 300 DPI, white background
- **Documentation**: SVG, embedded fonts
- **Web**: SVG/PNG, optimized, max 1200px width

## Checklist
- [ ] Material Design colors used
- [ ] Grid alignment consistent
- [ ] No shadows or 3D effects
- [ ] Labels don't overlap
- [ ] All text readable at 100% zoom
- [ ] Stroke widths indicate importance
- [ ] Naming: `project-name-architecture.drawio`