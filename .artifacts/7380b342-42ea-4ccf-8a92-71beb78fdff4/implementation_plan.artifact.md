# Add Gameplay Screenshots to Home Page (Revised)

Replace the current gameplay screenshot placeholder with six actual screenshots from the `assets/` directory, arranged in a horizontal 6x1 row.

## User Review Required

> [!IMPORTANT]
> The layout will be adjusted to a 2/5 (text) and 3/5 (images) split on medium screens and above. The images will be displayed in a single row, which may make them appear quite narrow on smaller viewports unless handled with horizontal scrolling or stacking.

## Proposed Changes

### [Home Page]

#### [MODIFY] [index.html](file:///Users/han/Desktop/WildBridge /index.html)
- Update the Features Section grid:
    - Change `md:grid-cols-2` to `grid-cols-1 md:grid-cols-5`.
    - Wrap the text content in a `div` with `md:col-span-2`.
    - Replace the placeholder `div` with a container using `md:col-span-3`.
- Inside the image container:
    - Create a `grid grid-cols-3 sm:grid-cols-6` (or just `grid-cols-6` if space permits) to display images side-by-side.
    - Add the 6 screenshots:
        - `assets/scr1.jpg`
        - `assets/scr2.jpg`
        - `assets/scr3.PNG`
        - `assets/scr4.PNG`
        - `assets/scr5.PNG`
        - `assets/scr6.PNG`
    - Apply `rounded-xl` and `shadow-sm` to each image.
    - Ensure `w-full h-auto object-contain` to maintain proportions.
    - Set a `gap-2` or `gap-1` to keep them "closely side by side".

## Verification Plan

### Manual Verification
- Open `index.html` in a browser.
- Verify the 2:3 horizontal split between text and images on desktop.
- Verify all 6 images are in a single row.
- Check that images have rounded corners and maintain their aspect ratio.
- Verify the layout remains functional on mobile (likely stacking the text above the images).
