# UI STANDARDS 📱

## The "One Screen" Rule
All MVP tools (calculators, converters, generators) MUST fit on a single screen (100dvh) on mobile devices.

### Requirements:
1.  **Container:** `h-dvh w-screen overflow-hidden` (Dynamic Viewport Height).
2.  **Layout:** `flex flex-col`
    -   Header (Logo): `flex-none`
    -   Main (Content): `flex-1 flex flex-col justify-center`
    -   Footer (Copyright): `flex-none`
3.  **Typography:** Responsive text sizes. `text-3xl` on mobile, `text-6xl` on desktop.
4.  **Input/Button:** Touch-friendly targets (44px+), but compact vertical spacing.
5.  **No Scrolling:** Unless absolutely necessary for result lists (use internal scrolling `overflow-y-auto` for specific divs, not the body).

### Code Snippet (Tailwind):
```html
<body class="h-dvh w-screen overflow-hidden bg-background text-text flex flex-col">
  <header class="p-4 flex-none">...</header>
  <main class="flex-1 flex flex-col justify-center items-center px-4">
    <!-- Content centered here -->
  </main>
  <footer class="p-4 flex-none text-center text-xs opacity-50">...</footer>
</body>
```
