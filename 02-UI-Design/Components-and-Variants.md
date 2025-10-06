# Components and Variants

## Introduction

Components are reusable design elements that maintain consistency across projects and enable scalable design systems. When you update a main component, all instances update automatically—ensuring consistency, saving time, and reducing errors. Components transform design from individual artboards into systematic, maintainable libraries that mirror how developers build with code.

Variants elevate components further, allowing multiple states, sizes, and configurations within a single component set. Instead of managing separate components for button-primary, button-secondary, button-small, button-large, you create one button component with variants for state (default, hover, active) and size (small, medium, large). This drastically reduces component clutter and makes designs more organized and scalable.

Mastering components and variants is essential for building [[Design-Systems]], collaborating with developers, and working on complex products where consistency matters. They're the foundation of professional UI design work and the bridge between design and code.

## Learning Objectives

By mastering Components and Variants, you will be able to:

- Create [[Main Components]] and understand their relationship to [[Instances]]
- Use [[Component Properties]] to control visibility, content, and behavior
- Organize components using [[Variants]] for states, sizes, and types
- Apply [[Auto-Layout]] within components for flexibility
- Build nested component structures for complex UI patterns
- Publish and manage [[Component Libraries]]
- Use [[Swap Instance]] to change between related components
- Create [[Interactive Components]] with state transitions

## Key Knowledge Points

### Component Fundamentals

- [[Components]]

  - Reusable design elements
  - Create: Cmd/Ctrl + Opt/Alt + K
  - Purple outline indicates component
  - Two types:
    - [[Main Component]] (source of truth, purple diamond icon)
    - [[Instance]] (copy linked to main, purple diamond with dot)

- [[Main Component]]

  - Original, editable definition
  - Changes propagate to all instances
  - Usually stored in component library or dedicated page
  - Can publish to team library

- [[Instance]]
  - Linked copy of main component
  - Inherits properties from main
  - Can [[Override]] specific properties
  - [[Detach Instance]]: break link to become regular frame

### Component Properties

- [[Component Properties]]
  - Modern way to make components flexible
  - Types:
    - [[Boolean Properties]] (show/hide elements, e.g., "Show Icon")
    - [[Text Properties]] (editable text fields, e.g., "Label")
    - [[Instance Swap Properties]] (swap nested components, e.g., "Icon")
    - [[Variant Properties]] (switch between variants)
- **Benefits:**
  - No need to detach instances
  - Cleaner properties panel
  - More semantic (developers understand intent)
  - Better handoff

### Variants

- [[Variants]]

  - Multiple states/versions within single component
  - Organized by properties (State, Size, Type, etc.)
  - Purple container with dashed outline
  - Create: Select multiple components → Combine as Variants

- [[Variant Properties]]
  - Custom properties that define differences
  - Common patterns:
    - **State:** Default, Hover, Pressed, Disabled, Focus
    - **Size:** Small, Medium, Large
    - **Type:** Primary, Secondary, Tertiary, Ghost
    - **Theme:** Light, Dark
    - **Icon:** True, False
- **Organization:**
  - Property names show in properties panel
  - Can have multiple properties (e.g., Size + State + Type)
  - Instances can switch between variants

### Component Structure

- [[Component Organization]]

  - Use slash notation for hierarchy
    - "Button/Primary/Default"
    - "Input/Text/Normal"
    - "Icon/Navigation/Home"
  - Helps with:
    - [[Assets Panel]] organization
    - [[Library]] browsing
    - [[Swap Instance]] suggestions

- [[Component Page]]
  - Dedicated page for components (common pattern)
  - Name: "🔷 Components" or "📦 Library"
  - Organized sections by category
  - Documentation and examples

### Nested Components

- [[Nested Components]]

  - Components within components
  - Example: Button contains Icon component and Text
  - Enables:
    - Icon swapping (different icons, same button)
    - Reusable sub-components
    - Modular design

- [[Instance Swap]]
  - Change nested component to different component
  - Properties panel: dropdown to select replacement
  - Example: Change icon in button from "search" to "arrow"

### Component States

- [[Component States]]
  - Different interactive states as variants
  - Common states:
    - [[Default State]]
    - [[Hover State]]
    - [[Pressed State]] / [[Active State]]
    - [[Disabled State]]
    - [[Focus State]]
    - [[Error State]]
    - [[Loading State]]
- **Best Practice:**
  - Create all states for interactive elements
  - Helps developers understand interactions
  - See [[Interactive Components]]

### Component Libraries

- [[Component Library]]
  - Collection of reusable components
  - Can be:
    - Local (within file)
    - Team library (published across organization)
- [[Publishing Components]]

  - Publish library to team
  - Others enable library and use components
  - Version control and updates
  - Update notification when library changes

- [[Team Library]]
  - Shared component library
  - Enable: Assets panel → Team Libraries icon
  - Accept updates when library is updated
  - Centralized [[Design-Systems]]

### Interactive Components

- [[Interactive Components]]

  - Components with prototyping built in
  - Variant transitions automated
  - Example: Button component with hover/press states
  - When hovered in prototype, shows hover variant
  - See [[Figma-Prototyping]]

- [[Component Playground]]
  - Test area for component variations
  - Show all states, sizes, configurations
  - Documentation and QA

## Related Topics

- [[Figma-Basics]]
- [[Auto-Layout]]
- [[Design-Systems]]
- [[Style-Guides]]
- [[Design-Tokens]]
- [[Component-Libraries]]
- [[Figma-Prototyping]]
- [[UI-Components]]

## Tools & Resources

- Figma Component Documentation
- Figma Community component libraries (study examples)
- Material Design Component Library (reference)
- iOS Design Kit (reference)

## Practice Exercises

1. **Button Component System:** Create a button component with variants for:

   - Size: Small, Medium, Large
   - Type: Primary, Secondary, Tertiary, Ghost
   - State: Default, Hover, Pressed, Disabled
     Total: 48 variants (4 sizes × 4 types × 3 states)

2. **Input Field Component:** Build a text input with:

   - Boolean property: "Show Icon"
   - Text properties: "Label", "Placeholder", "Helper Text"
   - Variants: Normal, Focus, Error, Disabled
   - Instance swap property: Icon selection

3. **Card Component:** Create a card with:

   - Boolean properties: "Show Image", "Show CTA Button"
   - Text properties: "Title", "Description", "Button Label"
   - Nested components: Button (swap instance)
   - Use Auto-Layout for flexible sizing

4. **Icon System:** Build an icon component library:

   - 20 icons (navigation, actions, social)
   - Consistent sizing (24x24px)
   - Variants for size: 16, 24, 32, 48px
   - Use as nested component in buttons/nav

5. **Component Library Publishing:** Create a mini design system:
   - 5 components (Button, Input, Card, Badge, Avatar)
   - Publish as team library
   - Create test page using library instances
   - Make update to library and accept update

## Further Reading

- Figma: Components Documentation
- Figma: Variants Documentation
- "Building Design Systems in Figma" (YouTube)
- Design Systems Handbook (component architecture)
- Brad Frost: Atomic Design (component philosophy)
