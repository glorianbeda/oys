# Project Slide Layout Guide

This guide defines the standardized 2-column, 4-card layout for project presentation slides. Every project slide should strictly follow this structure to maintain professional consistency.

## 1. Grid Structure

Each slide uses a **Two-Column Layout** with a `45px` gap.

- **Left Column**: Contains the Project Meta-information and a Hero Image.
- **Right Column**: Contains the System Capabilities and Technical Details.

## 2. Card Breakdown (The 4-Card Rule)

### Card A: Project Overview (Top Left)

- **Class**: `.glass-panel.details-card`
- **Content**: Icon + Title ("Project Overview"), followed by a "Project Details" section with badges for Engineering focus and Project Timeline.
- **Sizing**: `flex: 0 0 auto` (Grows to fit content).

### Card B: Image Card (Bottom Left)

- **Class**: `.glass-panel.image-card`
- **Content**: A single `<img>` tag.
- **Styling**: Must use `object-fit: cover` and `object-position: top` to handle fill-crop dashboard screenshots correctly.
- **Sizing**: `flex: 1` (Fills all remaining vertical space in the left column).
- **Rule**: No padding (`padding: 0 !important`).

### Card C: System Capabilities (Top Right)

- **Class**: `.glass-panel.features-card`
- **Content**: Large Icon + Title ("System Capabilities"), followed by a grid of feature items (Icon + Title + Description).
- **Sizing**: `flex: 1` (Dominant card on the right side).

### Card D: Technology Stack (Bottom Right)

- **Class**: `.glass-panel.tech-card`
- **Content**: Icon + Title ("Technology Stack"), followed by a wrap-list of technology badges.
- **Sizing**: `flex: 0 0 auto`.

## 3. Required HTML Structure Template

```html
<h1 class="page-title">Project Name</h1>
<div class="tech-container">
  <!-- Left Column -->
  <div class="tech-stack">
    <!-- Card 1: Project Overview -->
    <div class="glass-panel details-card">
      <h2 class="panel-title"><i class="material-icons">info</i><span>Project Overview</span></h2>
      <div class="tech-categories">
        <div class="tech-category">
          <div class="tech-items">
            <div class="tech-item">Department</div>
            <div class="tech-item">Timeline</div>
          </div>
        </div>
      </div>
    </div>
    <!-- Card 2: Hero Image -->
    <div class="glass-panel image-card">
      <img src="path/to/image.png" alt="Project Screenshot" style="object-position: top;" />
    </div>
  </div>

  <!-- Right Column -->
  <div class="gopro-highlight">
    <!-- Card 3: System Capabilities -->
    <div class="glass-panel features-card">
      <div class="gopro-content">
        <div class="gopro-header">
          <div class="gopro-logo"><i class="material-icons">icon_name</i></div>
          <h2 class="gopro-title">System Capabilities</h2>
        </div>
        <div class="gopro-features">
          <div class="feature-item">
             <div class="feature-icon"><i class="material-icons">icon</i></div>
             <div class="feature-text"><div class="feature-title">Feature</div> Description</div>
          </div>
          <!-- More features... -->
        </div>
      </div>
    </div>
    <!-- Card 4: Tech Stack -->
    <div class="glass-panel tech-card">
      <h2 class="panel-title"><i class="material-icons">layers</i><span>Technology Stack</span></h2>
      <div class="tech-items">
        <div class="tech-item">Tech 1</div>
        <!-- More tech... -->
      </div>
    </div>
  </div>
</div>
```

## 4. CSS Critical Rules (Ensure these are in your `<style>` block)

```css
.image-card {
  padding: 0 !important;
  overflow: hidden;
  flex: 1;
  min-height: 400px;
  display: block !important;
}

.image-card img {
  width: 100% !important;
  height: 100% !important;
  max-width: 100% !important;
  max-height: 100% !important;
  object-fit: cover;
  display: block;
  border: none !important;
  box-shadow: none !important;
  background: none !important;
  margin: 0 !important;
}
```
