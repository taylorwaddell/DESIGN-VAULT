# Contrast and Accessibility

## Introduction

Contrast is the measurable difference in perceived luminance between two colors, and it's fundamental to creating accessible, readable, and usable interfaces. Poor contrast makes text illegible, interactive elements invisible, and interfaces unusable for millions of users—particularly those with visual impairments, color blindness, or age-related vision changes. Mastering contrast isn't optional; it's a core responsibility of every designer.

The Web Content Accessibility Guidelines ([[WCAG]]) provide specific mathematical standards for minimum contrast ratios, but effective contrast design goes beyond compliance. It encompasses thoughtful hierarchy, strategic emphasis, and inclusive design thinking. High contrast draws attention, low contrast recedes, and the interplay between the two creates [[Visual Hierarchy]] and guides user attention through interfaces.

Understanding contrast empowers designers to make bold, confident color choices while ensuring everyone can use their designs. It transforms accessibility from a checklist item into a design advantage, resulting in clearer, more impactful interfaces that work for everyone.

## Learning Objectives

By mastering Contrast and Accessibility, you will be able to:

- Calculate and evaluate [[Contrast Ratio]] between text and backgrounds
- Apply [[WCAG AA]] (4.5:1 for normal text, 3:1 for large text) and [[WCAG AAA]] (7:1 for normal text, 4.5:1 for large text) standards
- Design for [[Color Blindness]] (protanopia, deuteranopia, tritanopia, achromatopsia)
- Use contrast strategically to create [[Visual Hierarchy]] and guide user attention
- Apply [[Accessible Color Palettes]] across UI components
- Test designs with [[Contrast Checker Tools]] and simulation tools
- Balance aesthetic goals with accessibility requirements

## Key Knowledge Points

### Contrast Fundamentals

- [[Contrast Ratio]]

  - Mathematical measure of luminance difference
  - Scale: 1:1 (no contrast) to 21:1 (maximum contrast)
  - Based on [[Luminance]], not just color difference

- [[WCAG]] (Web Content Accessibility Guidelines)
  - [[WCAG AA]] (minimum standard)
    - 4.5:1 for normal text (under 18pt or 14pt bold)
    - 3:1 for large text (18pt+ or 14pt+ bold)
    - 3:1 for UI components and graphics
  - [[WCAG AAA]] (enhanced standard)
    - 7:1 for normal text
    - 4.5:1 for large text
  - [[Non-Text Contrast]] requirements

### Color Accessibility

- [[Color Blindness]]
  - [[Protanopia]] (red-blind, ~1% males)
  - [[Deuteranopia]] (green-blind, ~1% males)
  - [[Tritanopia]] (blue-blind, rare)
  - [[Achromatopsia]] (total color blindness, very rare)
- [[Color is Not Enough]] principle
  - Never rely on color alone to convey information
  - Use [[Icons]], [[Patterns]], [[Text Labels]], [[Shape]]
- [[Color-Blind Safe Palettes]]

### Contrast Strategies

- [[Luminance Contrast]]
- [[Hue Contrast]]
- [[Saturation Contrast]]
- [[Text Contrast]]
  - Body text contrast
  - [[Large Text]] vs [[Small Text]]
  - [[Light Text on Dark Background]] (dark mode)
  - [[Dark Text on Light Background]] (light mode)
- [[Button Contrast]]
- [[Border Contrast]]
- [[Focus Indicator Contrast]]
- [[Disabled State Contrast]]
- [[Link Contrast]]

### Testing & Tools

- [[Contrast Checker Tools]]
  - [[Stark]] (Figma plugin)
  - [[WebAIM Contrast Checker]]
  - [[Colour Contrast Analyser]]
  - [[Chrome DevTools]] accessibility audit
- [[Color Blindness Simulators]]
  - Stark simulation modes
  - [[Colorblind Web Page Filter]]
- [[Accessible Color Palette Generators]]

## Related Topics

- [[Color-Theory]]
- [[Color-Harmonies]]
- [[Typography]] (text size affects contrast requirements)
- [[Accessibility]]
- [[WCAG-Guidelines]]
- [[Visual Hierarchy]]
- [[Design-Systems]] (documenting contrast requirements)
- [[Dark Mode]] (contrast in different themes)

## Tools & Resources

- [[Stark]] (Figma/Sketch plugin)
- [[WebAIM Contrast Checker]]
- [[Coolors]] (contrast checking built-in)
- [[Adobe Color]] (accessibility tools)
- [[Who Can Use]] (real-world contrast impact simulator)
- [[Contrast Finder]] (suggests accessible alternatives)

## Practice Exercises

1. **Audit & Fix:** Take 5 existing designs (yours or others) and audit text contrast. Fix any failures.
2. **Color Blind Testing:** Design a status system (success/warning/error) that works without color. Use shape, icon, and position.
3. **Dark Mode Challenge:** Create a color palette that meets WCAG AA in both light and dark modes
4. **Contrast Exploration:** Build a single interface with three contrast levels: minimum (4.5:1), comfortable (7:1), and maximum (15:1+). Compare usability.
5. **Real-World Testing:** Test your design using color blindness simulators and adjust palette based on findings

## Further Reading

- W3C: WCAG 2.1 Understanding Contrast Requirements
- WebAIM: Contrast and Color Accessibility
- "Accessibility for Everyone" by Laura Kalbag
- Material Design: Accessibility Color Guidelines
- Apple HIG: Color and Contrast
