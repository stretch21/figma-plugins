# Competency Skills Chart Widget

A FigJam widget for tracking and visualizing professional competencies across Enterprise Functional and Product Design skill areas.

## Features

- **10 Interactive Skill Bars**: Assess competencies across two main categories
- **5 Proficiency Levels**: From Foundational to Expert
- **Visual Progress Tracking**: Click on bars to set your skill level
- **Category Groups**:
  - **Enterprise Functional Competencies** (6 skills)
    - Adaptability / Agility
    - Client / Customer Centricity
    - Communication
    - Execution
    - Organizational & Business Insight
    - Partnership
  - **Product Design Functional Competencies** (4 skills)
    - Consulting
    - Experience Strategy
    - Product Strategy
    - Visual & Interaction Design

## Skill Levels

1. **Foundational** - Basic understanding and capability
2. **Developing** - Growing proficiency and confidence
3. **Proficient** - Solid competence and independence
4. **Advanced** - High expertise and leadership
5. **Expert** - Mastery and organizational influence

## Setup & Installation

### Prerequisites

First, download Node.js which comes with NPM:
https://nodejs.org/en/download/

### Install Dependencies

```bash
npm install
```

### Build the Widget

```bash
npm run build
```

Or use watch mode for development:

```bash
npm run watch
```

## Import into FigJam

1. Open FigJam
2. Go to **Menu > Widgets > Development > Import widget from manifest**
3. Select the `manifest.json` file from this directory
4. The widget will appear in your FigJam widgets panel

## Development

This widget uses:
- **TypeScript** for type-safe code
- **esbuild** for fast bundling
- **Figma Widget API** v1.0.0

### File Structure

```
SkillChart/
├── manifest.json       # Widget configuration
├── package.json        # NPM configuration
├── code.tsx           # Main widget source code
├── levelinfo.tsx      # Skill definitions and descriptions
├── code.js            # Compiled output (auto-generated)
├── levelinfo.js       # Compiled output (auto-generated)
├── tsconfig.json      # TypeScript configuration
└── images/
    ├── Icon.png       # Widget icon
    └── CoverArt.png   # Widget cover image
```

### Editing Skills & Levels

Edit the skill definitions in `levelinfo.tsx`:

```typescript
export const levelDescriptions = [
    {
        skill: 'Adaptability / Agility',
        level: 'Foundational',
        description: 'Your description here'
    },
    // ... more levels
];
```

### Customizing Categories

Edit the category definitions in `code.tsx`:

```typescript
var enterpriseCategory = {
    name: "Enterprise Functional Competencies",
    color: "#9747FF",
    skills: ["Adaptability / Agility", ...],
    skillDescriptions: ["", "", ...]
};
```

## Widget API Documentation

For more information about the Figma Widget API:
https://www.figma.com/widget-docs/

## TypeScript

This widget is written in TypeScript. For more information:
https://www.typescriptlang.org/

## License

MIT
