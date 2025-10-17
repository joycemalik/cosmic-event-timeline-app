# Interactive Cosmic Timeline

A breathtaking single-page web application that visualizes key events in the universe's history on an interactive timeline.

## How to Use

1.  **Save the file:** Save the provided `index.html` content into a file named `index.html` on your computer.
2.  **Open in browser:** Open the `index.html` file with any modern web browser (e.g., Chrome, Firefox, Safari).
3.  **Interact:** Scroll down to navigate the cosmic timeline. Click on any event card to expand and reveal a brief description, and click again to collapse it. The background features a subtle, animated starfield.

## Code Explanation

This project is a single-file web application (`index.html`) demonstrating a minimalist approach to interactive design:

*   **HTML Structure:**
    *   The page includes a main `div` for the `starfield` and another `div` for the `timeline-container`.
    *   Inside the `timeline-container`, each cosmic event is represented by an `event-card` `div` containing a title (`<h3>`), time (`<time>`), and a hidden description (`<p class="event-description">`).
*   **CSS Styling:**
    *   **Dark Theme & Fonts:** Uses a dark background, light text, and the "Poppins" font from Google Fonts.
    *   **Dynamic Starfield:** A pure CSS and JavaScript solution creates a parallax starfield. JavaScript generates multiple layers of stars using `box-shadow` properties, and CSS `@keyframes` animate their subtle movement and twinkling, giving a dynamic, ethereal background.
    *   **Timeline Beam:** A central glowing vertical line is created using a `::before` pseudo-element on the `timeline-container`, styled with a linear gradient and `box-shadow` for the glow effect.
    *   **Event Cards:** Cards are elegantly positioned to alternate left and right along the timeline. Each card features a `::after` pseudo-element that acts as a glowing circle, precisely aligned with the central timeline beam.
    *   **Expansion Effect:** The `event-description` uses `max-height: 0`, `opacity: 0`, and CSS `transition` to create a smooth expand/collapse animation when clicked.
    *   **Responsiveness:** Media queries are used to adjust the layout for smaller screens, transitioning the timeline to a single-column display where all cards are aligned to the left of the beam.
*   **Vanilla JavaScript:**
    *   **Starfield Generation:** A JavaScript function `generateStarfieldLayers` dynamically creates multiple layers of stars. It calculates random positions, sizes, and opacities for stars (using `box-shadow`) and applies CSS animations (`move-stars` and `twinkle`) with staggered delays to achieve the dynamic, parallax effect. This function also adapts the number of stars based on screen size.
    *   **Event Toggle:** An event listener is attached to each `event-card`. On click, it toggles an `expanded` class, which triggers the CSS transition to show or hide the event description.

## License

This project is licensed under the MIT License.