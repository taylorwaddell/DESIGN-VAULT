# Figma Basics

## Introduction

Figma is the industry-standard collaborative design tool for UI/UX work, combining powerful vector editing, prototyping, and design system capabilities in a browser-based platform. Mastering Figma isn't just about learning software—it's about understanding modern design workflows, component-based thinking, and real-time collaboration. Figma has fundamentally changed how designers work, enabling seamless handoff to developers and allowing entire teams to design together simultaneously.

Unlike traditional design tools, Figma embraces web-native principles: everything is cloud-based, version-controlled, and accessible from any device. This means designs are always up-to-date, feedback happens in context, and designers can work from anywhere. Understanding Figma's core concepts—[[Frames]], [[Auto-Layout]], [[Components]], [[Styles]], and [[Constraints]]—unlocks efficient, scalable, and maintainable design work.

For beginners, Figma can feel overwhelming, but its power comes from systematic thinking. Learn frames before auto-layout, master components before variants, and understand styles before building design systems. Each concept builds on the previous, creating a foundation for professional-level design work.

## Learning Objectives

By mastering Figma Basics, you will be able to:

- Navigate the Figma interface and understand [[Layers Panel]], [[Properties Panel]], and [[Canvas]]
- Create and manipulate [[Frames]] as containers for designs
- Use [[Vector Tools]] (pen, pencil, shape tools) to create custom graphics
- Apply [[Boolean Operations]] to combine shapes
- Organize designs using [[Pages]] and [[Sections]]
- Use [[Constraints]] to control how elements resize
- Apply [[Styles]] for colors, text, effects, and grids
- Export assets in multiple formats and resolutions
- Understand Figma's [[Multiplayer]] collaboration features

## Key Knowledge Points

### Interface & Navigation

- [[Figma Interface]]
  - [[Toolbar]] (top)
  - [[Layers Panel]] (left)
  - [[Properties Panel]] (right)
  - [[Canvas]] (center)
- [[Navigation]]
  - Zoom (Cmd/Ctrl + scroll, Cmd/Ctrl + 0 for 100%, Cmd/Ctrl + 1 for fit)
  - Pan (Space + drag, or trackpad)
  - [[Search]] (Cmd/Ctrl + /)
- [[Figma Files]]
  - [[Team Files]] vs [[Drafts]]
  - [[Pages]] (organize within file)
  - [[Sections]] (organize within page)

### Frames & Objects

- [[Frames]]
  - Containers for designs
  - Define artboards/screens
  - Can nest infinitely
  - Keyboard: F or A
  - Preset sizes (iPhone, Desktop, etc.)
  - vs [[Groups]] (groups don't clip content)
- [[Layers]]
  - [[Layer Hierarchy]]
  - Naming conventions
  - [[Lock]] and [[Hide]] layers
  - Layer shortcuts (Cmd/Ctrl + G for group, Cmd/Ctrl + Opt/Alt + G for frame)

### Vector Tools

- [[Shape Tools]]
  - [[Rectangle]] (R)
  - [[Ellipse]] (O)
  - [[Line]] (L)
  - [[Arrow]]
  - [[Polygon]]
  - [[Star]]
- [[Pen Tool]] (P)
  - [[Bezier Curves]]
  - [[Vector Networks]] (Figma-specific, any-to-any connections)
- [[Pencil Tool]] (Shift + P)
- [[Boolean Operations]]
  - [[Union]]
  - [[Subtract]]
  - [[Intersect]]
  - [[Exclude]]
  - [[Flatten]]

### Styling & Properties

- [[Fill]]
  - Solid colors
  - [[Gradients]] (linear, radial, angular, diamond)
  - [[Images]]
- [[Stroke]]
  - Position (center, inside, outside)
  - Weight, cap, join
  - Dashed strokes
- [[Effects]]
  - [[Drop Shadow]]
  - [[Inner Shadow]]
  - [[Layer Blur]]
  - [[Background Blur]]
- [[Blend Modes]]
- [[Opacity]]

### Text

- [[Text Tool]] (T)
- [[Text Properties]]
  - [[Font Family]], [[Font Weight]], [[Font Size]]
  - [[Line Height]], [[Letter Spacing]], [[Paragraph Spacing]]
  - [[Text Alignment]]
  - [[Text Case]]
- [[Text Styles]]
  - Reusable typography settings
  - See [[Typography]]

### Constraints & Resizing

- [[Constraints]]
  - Left, Right, Center, Left & Right, Scale
  - Top, Bottom, Center, Top & Bottom, Scale
  - Controls how child elements respond to parent frame resizing
  - Foundation for responsive design
- [[Resize Behavior]]
  - Fixed width/height
  - Hug contents
  - Fill container

### Styles

- [[Color Styles]]
  - Reusable color definitions
  - Update globally
- [[Text Styles]]
  - Reusable typography
  - H1, H2, Body, Caption, etc.
- [[Effect Styles]]
  - Reusable shadow/blur effects
- [[Grid Styles]]
  - Reusable layout grids
  - See [[Grid-Systems]]

### Organization

- [[Pages]]
  - Organize different sections (Cover, Designs, Archive, Components)
- [[Sections]]
  - Visual grouping on canvas
- [[Naming Conventions]]
  - Descriptive, consistent naming
  - Slash notation for organization (e.g., "Button/Primary/Default")

### Export & Handoff

- [[Export Settings]]
  - PNG, JPG, SVG, PDF
  - 1x, 2x, 3x resolutions
  - Suffix naming
- [[Slice Tool]] (S)
- [[Developer Handoff]]
  - Inspect mode
  - CSS, iOS, Android code snippets
  - Measurements and spacing

### Collaboration

- [[Multiplayer Editing]]
  - Real-time collaboration
  - See cursors and selections
- [[Comments]]
  - In-context feedback
  - @ mentions
  - Resolve threads
- [[Version History]]
  - Automatic saves
  - Named versions
  - Restore previous versions
- [[Sharing & Permissions]]
  - View, Edit, Admin
  - Link sharing
  - Password protection

## Related Topics

- [[Auto-Layout]]
- [[Components-and-Variants]]
- [[Figma-Prototyping]]
- [[Style-Guides]]
- [[Design-Systems]]
- [[Wireframing]]
- [[Hi-Fi-Prototyping]]

## Tools & Resources

- Figma Official Tutorials (YouTube, Help Center)
- Figma Community (templates, plugins, files)
- [[Figma Plugins]]
  - Content Reel (dummy content)
  - Unsplash (free images)
  - Iconify (icon library)
  - Stark (accessibility)
- Keyboard Shortcuts Cheatsheet

## Practice Exercises

1. **Interface Mastery:** Complete Figma's official playground tutorial. Practice all keyboard shortcuts for 30 minutes.

2. **Vector Practice:** Recreate 5 company logos using only shape tools and boolean operations. Focus on precision.

3. **Frame Organization:** Design a 3-page website wireframe. Use proper frame structure, naming, and sections.

4. **Styles Setup:** Create a basic style library: 8 colors, 5 text styles (H1-H3, Body, Caption), 3 shadow effects.

5. **Constraints Challenge:** Create a card component that maintains its design when resized from 320px to 1440px wide using only constraints (no Auto-Layout yet).

6. **Export Workflow:** Design a simple icon set (5 icons). Export in multiple formats: SVG, PNG @1x, @2x, @3x.

## Further Reading

- Figma Official Documentation
- "Figma for Beginners" tutorials (YouTube)
- Figma Community best practices
- "Figma to Code" workflow guides
