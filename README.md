# 🎯 FOCUS FIGHTER
**A Hardcore Cybernetic Posture Tracker & Productivity HUD.**

🔴 **[PLAY THE LIVE DEMO HERE](https://saharan7317.github.io/Focus-Fighter/v3-cyber-cockpit/)**

Focus Fighter is a client-side AI web application that uses your webcam to monitor your posture, presence, and focus. If you slouch, look at your phone, or walk away from your desk, the system's alarms will trigger, your health bar will melt, and your screen will glitch. 

Sit straight. Stay focused. Survive.

---

## 🚀 The Evolution (Versions)
This project was built iteratively. You can explore the three major milestones of the codebase in their respective folders:

### 📁 `v1-classic` : The Core Engine
The foundation of the tracker. It establishes the live webcam feed and integrates Google's MediaPipe AI to map skeletal landmarks in real-time.
* Uses the Native Camera API to prevent infinite loading loops.
* Calculates the dynamic Y-axis distance between the user's ears and shoulders to detect "Text Neck" and slouching.

### 📁 `v2-soundboard` : The Audio Update
Introduces the Web Audio API to generate synthetic alarms dynamically without relying on external assets.
* Includes a custom dashboard for selecting audio profiles (Cyber Buzz, 8-Bit, Boing, Siren).
* **Custom Uploads:** Users can upload their own `.mp3` or `.wav` files. The engine mathematically slices the audio to play in rapid-fire bursts based on a user-controlled "Beep Delay" slider.

### 📁 `v3-cyber-cockpit` : The Ultimate HUD
Transforms the app into a full-blown cybernetic dashboard with advanced tracking logic and anti-cheat mechanics.
* **Floating Mini-Player (PiP):** Uses the native Picture-in-Picture API so you can pop the tracker out into an always-on-top window. Keep an eye on your health bar and posture grade while coding or working in other apps!
* **Anti-Cheat:** The AI measures facial yaw (looking away) and shoulder width (leaning/walking away). The timer pauses instantly if you break alignment.
* **Live Stats:** Tracks Peak Survival Time, total System Alerts, and assigns a live Posture Grade (S to F).
* **The Redemption Arc:** Holding perfect posture for 15 unbroken seconds "heals" your grade by erasing past errors.
* **Theme Engine:** CSS-variable driven color themes (Matrix Green, Ice Blue, Solar Flare, etc.) and a live Glitch Intensity slider that manipulates canvas translations and RGB splits.

---

## 🛠️ Under the Hood (Tech Stack)
* **Frontend:** HTML5, CSS3, Vanilla JavaScript.
* **AI Vision:** MediaPipe Pose (`modelComplexity: 1`).
* **Audio:** Native Web Audio API (`AudioContext`, `BiquadFilterNode`, `OscillatorNode`) and array buffer decoding.
* **Rendering:** HTML5 `<canvas>` for mirrored drawing, glitch effects, and UI overlays.
* **Zero Dependencies:** No local servers, Node packages, or backend required. Everything runs natively in the browser.

---

## 🎮 How to Play
You can play the final version instantly via the **[Live Demo](https://saharan7317.github.io/Focus-Fighter/v3-cyber-cockpit/)**, or run it locally:

1. Clone or download this repository.
2. Open any of the version folders (`v1-classic`, `v2-soundboard`, or `v3-cyber-cockpit`).
3. Double-click the `index.html` file to open it in your browser.
4. Grant camera access, calibrate your posture, and try to survive.

*(Note: Ensure you are in a well-lit room so the AI can accurately map your facial landmarks!)*

---

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details. Feel free to fork it, mod it, and build your own HUDs.
