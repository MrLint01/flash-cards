Website: https://mrlint01.github.io/flash-cards/
# sound-wave-visualizer

The files in the [public](/public) directory are deployed to: https://cse442.pages.cs.washington.edu/25au/fp/sound-wave-visualizer

## Development notes

- **Generative AI assistance**  
  - [`public/js/d3-sine-wave-animation.js`](/public/js/d3-sine-wave-animation.js): Helped refine the frame-by-frame animation loop, including how phase progresses each frame, how requestAnimationFrame is scheduled, and how the waveform stays synced with the selected note.
  - [`public/js/d3-sine-wave-combined.js`](/public/js/d3-sine-wave-combined.js): Helped ensure the computation logic is shared between the static snapshot and the animated waveform, maintaining consistency while toggling between the two views, and preserving the current frame to prevent sudden jumps or position shifts in the sine wave.
  - [`public/js/d3-sine-wave-simulation.js`](/public/js/d3-sine-wave-simulation.js): Helped clarify the Web Audio API setup (oscillators, gain shaping, event wiring) and improve the simulation and interpolation (lerp) logic that trails previous waves while the active tone renders in the center.
