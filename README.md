Website: https://mrlint01.github.io/flash-cards/

# sound-wave-visualizer

The files in the [public](/public) directory are deployed to: https://cse442.pages.cs.washington.edu/25au/fp/sound-wave-visualizer

## Development notes

- **Generative AI assistance**  
  - [`public/js/d3-sine-wave-combined.js`](/public/js/d3-sine-wave-combined.js): Helped coordinate mode toggles and the requestAnimationFrame loop without desynchronizing the two charts, maintaining consistency when switching between views and preserving the current frame to prevent sudden jumps or position shifts in the sine wave. For the dynamic visualization, also helped refine the frame-by-frame animation loop, including how phase progresses each frame, how requestAnimationFrame is scheduled, and how the waveform stays synced with the selected note.
  - [`public/js/d3-sine-wave-simulation.js`](/public/js/d3-sine-wave-simulation.js): Helped clarify the Web Audio API setup (oscillators, gain shaping, event wiring) and improve the simulation and interpolation (lerp) logic that trails previous waves while the active tone renders in the center.
  - [`public/js/d3-chord-wave.js`](/public/js/d3-chord-wave.js): As chord selections change, paths need to be added, updated, or removed without breaking the SVG. Received help identifying the issue that prevented it from working as expected.
  - [`public/js/piano.js`](/public/js/piano.js): Helped with constructing the piano and the logic behind computing white-key centers, positioning black keys relative to those centers, and wiring the pointer handlers so the layout and note playback stay aligned.
  - [`public/js/piano-chords.js`](/public/js/piano-chords.js): Helped in enabling multiple notes to play simultaneously while preventing dissonance issues (overlapping notes becoming excessively loud). This included refining gain control, handling note layering, and ensuring the resulting sound remained clean and pleasant.
  
