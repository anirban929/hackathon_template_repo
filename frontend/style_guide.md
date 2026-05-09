Visual Theme: Dark-mode, high-contrast, "Terminal/System Telemetry" aesthetic.  
1\. Color Palette (CSS Variables)  
Background (Surface): \#111827 (Deep Gray/Black)  
Card/Modal Background: \#1f2937 (Lighter Gray)  
Primary Action (Blue): \#3b82f6  
Success (Active/Green): \#4ade80  
Danger (Error/Red): \#f87171  
Text (Primary): \#ffffff (Pure White)  
Text (Muted/Labels): \#9ca3af (Cool Gray)  
Border/Divider: \#374151  
2\. Component Blueprints  
A. Buttons  
Primary: Background \#3b82f6, white text, small border-radius (4px-6px), bold font, hover state: brightness 110%.  
Action (Edit/Neutral): Transparent background, border 1px solid \#374151, color white, hover: background \#374151.  
Sizing: Padding 8px 16px for standard; 4px 8px for table actions.  
B. Typography  
Headings: Uppercase, letter-spacing 0.05em, bold. (Example: RECONFIGURING\_IDENTITY)  
Labels: Small, muted color (\#9ca3af), bold, bottom margin 4px.  
Inputs: Background \#111827, border 1px solid \#374151, color white. Focus state: border-color \#3b82f6.  
C. Data Tables  
Header: Darker background, muted uppercase text, sticky position.  
Cells: Border-bottom 1px solid \#374151, padding 12px 16px.  
Status Indicators: Small colored dots (8px circle) next to text.  
3\. Logic & API Standards  
State Management: Use useState for form data and useEffect for data fetching.  
API Pattern: Use a centralized api object (e.g., api.request(path, method, body)).  
Request Handling: Always include Authorization: Bearer \<token\> in headers.  
Form Logic: Use a unified handleChange function that detects type="checkbox" to handle booleans via e.target.checked and strings via e.target.value.  
Update Strategy: Use .map() to update specific items in a list state to maintain UI reactivity without full reloads.  
4\. Layout Rules  
Spacing: Use a base-4 grid (4px, 8px, 16px, 24px, 32px).  
Modals: Centered overlay, semi-transparent backdrop (rgba(0,0,0,0.7)), maximum width 500px.  
Icons: Use SVG stroke-based icons (lucide-style), set to 1.2em size.  
Instructions for LLM:  
"When generating React components, use Tailwind CSS classes or inline styles that strictly adhere to the hex codes and spacing rules above. Ensure all form components include a 'Loading' state and an 'Error' display message using the system red (\#f87171).”