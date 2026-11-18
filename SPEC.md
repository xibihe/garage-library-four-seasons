# Garage Library · Four Seasons

The four SPZ scenes share a coordinate system. A click starts the next season's small ripple at the picked location. Ripples can propagate concurrently, and the newest ripple takes precedence where it has arrived. The shader changes opacity and shading at the boundary and briefly shows a subset of the original splat outlines. Around the car, a wider overlap and transmittance-based blending maintain coverage as one reconstruction hands off to the next.

The Wave control applies to the next click. Small ripple is the default. Double crest sends a narrow reflection ahead of the seasonal boundary, which catches up as it crosses the room. Crosscurrent spreads farther toward the upper right of the view at the instant of the click, drawing an oblique front across the walls and floor. Each front stays attached to the scene as the camera moves.

The original five views are embedded in `DEFAULT_CAMERA_PATH` in their capture order. The path plays once after loading. The Camera path panel supports saving, revisiting, replacing, and deleting views. Edits are stored in the current browser. Each path segment interpolates camera position, pitch, and yaw, with continuous velocities between views.

Drag to look and right-drag or Shift-drag to pan. Scroll, WASD, and Q/E move the camera. WASD applies gentle first-person walking motion. Manual movement stops path playback and uses the current pose as its starting point.

Each season uses all two million original splats. The viewer precomputes depth orders for individual seasons and adjacent pairs and composites the necessary seasons when ripples overlap. A worker updates depth ordering when the camera moves.

Recording targets 60 fps, defaults to 4K, and offers 1440p and 1080p. The MP4 captures the canvas without the interface. Resolution affects output dimensions and bitrate. Every resolution keeps the original splat count.
