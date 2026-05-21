# Pulse: 3D Gestural Particle System

A high-performance, interactive 3D particle simulation that morphs between beautiful mathematical templates and reacts in real-time to webcam hand gestures. Powered by **Three.js** (WebGL) and **MediaPipe Hands** (Machine Learning).

---

## 🚀 Technologies Used

- **HTML5 & CSS3**: Structured layout and premium, responsive Glassmorphic user interface utilizing custom variables, gradients, blur filters, and micro-interactions.
- **Three.js (r128)**: High-performance WebGL-based 3D rendering engine, custom particle shaders, additive blending, exp2 fog, and camera orbit controls.
- **MediaPipe Hands**: Google's machine learning framework for low-latency hand skeletal tracking and landmarks detection in browser.
- **WebRTC / MediaDevices API**: Real-time webcam capture and mirrored picture-in-picture video stream preview.
- **Google Fonts**: Modern typography featuring *Outfit* (headings) and *Inter* (body/controls).

---

## 🎨 Core Features

1. **6 Morphing Mathematical Templates**:
   - **Saturn Ring System**: Warm orange gaseous core surrounded by a tilted, icy blue flat disc ring.
   - **Pulsing Heart**: Radiant crimson/magenta heart structure mapped with organic pillowed thickness.
   - **Golden Flower Blossom**: Fibonacci spiral (phyllotaxis) blooming shape with yellow core and violet petals.
   - **Buddha Silhouette**: A gold meditative silhouette sitting under a blue/cyan backing aura halo.
   - **Radial Fireworks Burst**: Golden core explosions with outer multi-colored layered star shells.
   - **Custom Text Shape**: Enter any text inside the UI control panel, and watch the particles automatically sample its outline and morph to spell your word in 3D space.

2. **Webcam Gesture Control**:
   - **Fist (Closed Hand)**: Pulls particles inward and condenses shape size.
   - **Open Hand**: Expands particle size and spreads them out radially.
   - **Double Hand Control**: (Dual camera mode) Left hand maps to shape scaling, while the Right hand controls radial expansion.

3. **Skeleton Diagnostics Window**:
   - Small webcam preview on the bottom-right showing the mirrored live-feed.
   - Real-time colored skeletal overlay showcasing tracked nodes and fingertip vertices.
   - Live tension tracker (0% to 100%) indicating hand openness.

4. **Dynamic Customization Controls**:
   - **Color Tint Overlay**: A color picker to shift the global tint of the particle system.
   - **Base Particle Size**: Sliders to adjust the thickness of point textures.
   - **Morphing Inertia**: Sliders to adjust morph speed and interpolation smoothness.
   - **Mouse Camera Controls**: Left-click drag to rotate camera, right-click drag to pan, scroll to zoom in/out.

---

## 🛠️ How to Run

Because browsers restrict camera access (getUserMedia API) to secure origins (`localhost` or `https://`), you **must** serve this application through a local web server rather than opening the file directly from your disk (e.g. `file://` protocol).

Here are the easiest methods to run the project locally:

### Option 1: Python (Built-in)
If you have Python installed, run this command in your terminal:
```bash
python3 -m http.server 8000
```
Then open your browser and navigate to:
[http://localhost:8000](http://localhost:8000)

### Option 2: Node.js / npm
If you have Node.js installed, you can use `npx` to serve the static folder instantly:
```bash
npx serve
```
Then open your browser and navigate to:
[http://localhost:3000](http://localhost:3000) (or the port specified in terminal).

### Option 3: VS Code extension
If you use VS Code, install the **Live Server** extension, right-click `index.html`, and select **Open with Live Server**.

---

## 🎮 How to Use

1. When the page loads, you will see the **Saturn Ring System** spinning in space.
2. Click **Enable Webcam Tracking** in the control panel.
3. Grant the browser permission to access your webcam.
4. Position your hands (one or both) inside your webcam's view. You will see a live skeleton tracking overlay in the bottom right corner.
5. Close your hand into a fist to shrink and condense the 3D particles.
6. Open your hand wide to disperse and expand the 3D particles.
7. Use the visual shape panel on the left to morph between Saturn, Heart, Flower, Buddha, Fireworks, or Custom Text.
8. Customize the experience by choosing custom colors, particle sizes, or adjusting the morphing inertia speed.
9. Click **Reset Orbit Camera** or click & drag on the empty dark space to orbit around your 3D models.
