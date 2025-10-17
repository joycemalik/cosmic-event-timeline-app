# Cosmic Timeline

A breathtaking single-page interactive cosmic timeline, tracing key events from the Big Bang to the emergence of life on Earth. The application features a dark, star-filled theme with a glowing timeline beam and expandable event cards.

## How to Use

1.  **Save the file:** Save the provided code as `index.html` on your computer.
2.  **Open in browser:** Double-click the `index.html` file, or open it with your preferred web browser.

The interactive timeline will load, displaying a series of cosmic events. Click on any event card to expand it and reveal a brief description, then click again to collapse it.

## Code Explanation

This project is a single-file web application (`index.html`) using only HTML and vanilla JavaScript for a minimalist approach.

*   **HTML Structure:** The `body` contains a main `h1` title and a `timeline-container`. Inside the container, a `timeline-beam` provides the central visual line, and multiple `timeline-event` divs represent each cosmic event. A `starfield-container` is added for dynamic stars.
*   **CSS Styling:**
    *   **Dark Theme & Fonts:** Global styles set a dark background (`--dark-bg`) and use the "Poppins" font imported from Google Fonts.
    *   **Dynamic Starfield:** JavaScript dynamically generates `.star` elements within the `.starfield-container`. CSS animations (`@keyframes twinkle`) give these stars a randomized twinkling effect, simulating a vibrant night sky.
    *   **Timeline Beam:** The `.timeline-beam` is a vertical line positioned centrally within its container, styled with a linear gradient and `box-shadow` for a glowing effect (`--timeline-glow`). On smaller screens, the beam shifts to the left for better readability.
    *   **Event Cards:** `.timeline-event` cards are styled with a semi-transparent dark background, rounded corners, and subtle shadows. They are positioned alternately to the left and right of the timeline beam using `margin` and `align-self` properties, managed by `nth-child(odd/even)` selectors. Each card has a `::before` pseudo-element to create the glowing dot directly on the timeline beam.
    *   **Interactivity & Transitions:** Event descriptions (`.event-description`) are initially hidden (`max-height: 0`, `opacity: 0`). When a card gains the `expanded` class (toggled by JavaScript), `max-height` and `opacity` are transitioned smoothly, creating an elegant expansion effect. Hover effects are also applied to cards.
    *   **Responsiveness:** Media queries are used to adapt the layout for various screen sizes. On screens smaller than 768px, all event cards stack on one side of a left-aligned timeline beam for a cleaner mobile experience.
*   **JavaScript Interactivity:**
    *   **Event Card Toggle:** A simple event listener is attached to each `.timeline-event`. On click, it toggles the `expanded` class, which triggers the CSS transitions for showing/hiding the event description.
    *   **Starfield Generation:** Upon page load, JavaScript programmatically creates a specified number of `div` elements, assigns them the `star` class, and places them at random positions and with random animation delays within the `starfield-container`, ensuring a unique and dynamic starfield appearance on each load.

## License

This project is licensed under the MIT License.