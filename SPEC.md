# Interactive Periodic Table - Specification

## 1. Project Overview

- **Project name**: Interactive Periodic Table
- **Project type**: React webapp (Vite)
- **Core functionality**: An interactive periodic table displaying all 118 elements with hover effects, click-to-select, and detailed element information
- **Target users**: Students, educators, chemistry enthusiasts

## 2. UI/UX Specification

### Layout Structure

- **Page layout**: Single page with centered content
- **Header**: App title at top
- **Main content**: Periodic table grid (18 columns x 10 rows layout)
- **Details panel**: Element details displayed in a sidebar/modal when element is selected
- **Responsive breakpoints**:
  - Desktop: Full grid, scale to fit
  - Tablet/Mobile: Scrollable or zoomable grid

### Visual Design

- **Color palette**:
  - Background: `#0a0a0f` (deep dark)
  - Surface: `#16161e` (card background)
  - Border: `#2a2a3a` (subtle borders)
  - Text primary: `#e8e8ec` (off-white)
  - Text secondary: `#8888a0` (muted)
  - Accent glow: `#00d4aa` (teal accent)

- **Element category colors**:
  - Alkali metals: `#ff6b6b` (coral red)
  - Alkaline earth: `#ffa94d` (orange)
  - Transition metals: `#ffd43b` (gold)
  - Post-transition: `#69db7c` (green)
  - Metalloids: `#38d9a9` (teal)
  - Nonmetals: `#4dabf7` (blue)
  - Halogens: `#9775fa` (purple)
  - Noble gases: `#f783ac` (pink)
  - Lanthanides: `#e599f7` (lavender)
  - Actinides: `#ff8787` (light red)
  - Unknown: `#495057` (gray)

- **Typography**:
  - Font family: `"JetBrains Mono", "Fira Code", monospace`
  - Element symbol: 18px bold
  - Atomic number: 10px
  - Element name (below symbol): 8px
  - Headings: 24px

- **Spacing**: 2px gap between element cells

- **Visual effects**:
  - Element cell hover: Scale 1.15x, glow effect with category color
  - Selected element: Ring indicator
  - Smooth transitions: 150ms ease-out

### Components

1. **ElementCell**
   - Shows: atomic number, symbol, name (abbreviated)
   - States: default, hover (scale + glow), selected (ring)
   - Colored background by category

2. **ElementDetails**
   - Modal or side panel
   - Shows: Full name, symbol, atomic number, atomic mass, category, electron configuration, discovery year, state at room temp
   - Close button

3. **PeriodicTable**
   - Grid container with proper element positioning
   - Lanthanide/Actinide separator row

## 3. Functionality Specification

### Core Features

1. **Display all 118 elements** in correct periodic table positions
2. **Hover interaction**: Element highlights with scale and glow effect
3. **Click to select**: Opens details panel with full element information
4. **Category color coding**: Each element colored by its category
5. **Lanthanide/Actinide rows**: Properly displayed below main table

### Element Data Required

- Atomic number (1-118)
- Symbol
- Name
- Atomic mass
- Category (alkali metal, noble gas, etc.)
- Electron configuration
- Discovery year
- Standard state (solid/liquid/gas)

### User Interactions

- Hover over element → visual highlight
- Click element → open details modal with full info
- Click outside modal or X button → close modal
- Keyboard: Escape closes modal

### Edge Cases

- Elements with unknown properties: display "Unknown" or "?"
- Mobile: ensure table is scrollable

## 4. Acceptance Criteria

- [ ] All 118 elements displayed in correct positions
- [ ] Elements colored by category
- [ ] Hover shows scale + glow effect
- [ ] Click opens details panel with element info
- [ ] Details panel shows: name, symbol, number, mass, category, electron config, year, state
- [ ] Smooth transitions throughout
- [ ] Monospace font used
- [ ] Dark theme with category-colored elements