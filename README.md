[README (1).md](https://github.com/user-attachments/files/33661306/README.1.md)[Uploading# Rigid Body Dynamics

An interactive simulation for learning **moment of inertia, torque, angular acceleration and angular momentum**. It's built for IB Diploma Physics (HL, rigid body mechanics) but works for any introductory rotational dynamics course.

The setting is a rotation bay on a space station in free fall. Gravity plays no part, so students can focus entirely on the rotational physics.

**Live site:** rigidbodyphysics.netlify.app

---

## Two modes

### Sandbox
A free-play lab for exploring how each variable affects the motion.

- Drag point masses onto a 2D platform. Positions snap to a 1 cm grid.
- Move the **axle** to see how *I* changes when the axis changes.
- Mount a **thruster**. Drag the ring at the arrow tip to set its size and direction, or type exact values.
- Set a **burn time** to explore angular impulse, or choose continuous thrust.
- Optional overlays show the position vector **r**, the angle **θ** and the **lever arm** on the bay.
- Live readouts show:
  - *m r²* for each mass, and the total *I*
  - τ = *rF* sin θ
  - α = τ / *I*
  - angular impulse τΔt
  - ω, *L* = *I*ω and *E*ₖ = ½*I*ω²
  - a graph of ω against *t*

#### Free-floating option
Switch the axle from **Bolted** to **Free-floating**. With nothing holding it in place, the system:

- spins about its **centre of mass**, and
- drifts as the thrust also accelerates the centre of mass, with *a* = *F* / *M*.

A trail shows the path of the centre of mass, and the camera can follow it. Two good things to demonstrate:

- A thrust whose line of action passes through the centre of mass gives pure translation with no spin.
- A thrust off to one side gives spin and drift together.

### Rescue Mission
A puzzle game. A debris strike has knocked out five systems on the station, and the student is the astronaut who has to repair them. Each repair is a randomly generated challenge, and they get harder as the student progresses:

| # | System | Physics |
|---|--------|---------|
| 1 | Gyro stabiliser | Build a system with a target *I*, or calculate *I* for given masses |
| 2 | Attitude thrusters | Calculate or produce a target τ or α |
| 3 | Reaction wheel | Build a target *I*, then drive it to a target α |
| 4 | Solar array drive | Reverse engineering: arrange masses around a fixed thruster, move the axle, or use angular impulse to reach a target *L* |
| 5 | Habitat centrifuge | Burn then coast: reach a target ω or *E*ₖ after a burn of set length |

- **Live values are hidden.** Students have to work things out themselves, using the scratch pad provided.
- **Feedback:** each check reports whether each quantity is correct, too high or too low (with a percentage), or in the wrong direction. A match within 2% passes.
- **Help:** after three failed attempts, Mission Control can send a worked solution laid out like a markscheme (equation, rearrange, substitute, evaluate). A repair made with the solution open doesn't count, so the student has to solve a fresh fault on their own.
- **Winning:** restore all five systems to save the station.
- Every puzzle is generated backwards from a hidden valid setup, so it can always be solved on the 1 cm grid.

---

## Physics conventions

- **Anticlockwise is positive** for angles, torque, α, ω and *L*.
- Force directions are measured anticlockwise from the +x axis.
- *I* = Σ *m r²*, using point masses on a massless rigid frame.
- τ = *rF* sin θ, where θ is the angle from **r** to **F**.
- The thruster is fixed to the platform and turns with it, so τ and α stay constant during a burn.
- The axle has no friction. After a burn, the system keeps rotating at constant ω.
- Positions are given in cm on screen. Calculations use SI units.

---

## Running it

The whole app is a single file, `index.html`, with no build step and no dependencies.

- **Locally:** open `index.html` in any modern desktop browser.
- **Netlify:** connect the GitHub repository, or drag the folder into Netlify. Make sure `index.html` sits at the top level of the repository, not in a subfolder.
- **GitHub Pages:** enable Pages on the repository's main branch.

Fonts (Oxanium and JetBrains Mono) load from Google Fonts. Without an internet connection, the app falls back to bold system fonts and still works.

The app is designed for desktop or laptop use with a mouse. It isn't optimised for tablets or phones.

---

## Controls

| Action | How |
|--------|-----|
| Select an object | Click it |
| Move an object | Drag it, or use the arrow keys (1 cm steps; hold Shift for 10 cm) |
| Remove a mass | Select it and press Delete |
| Aim or resize the thruster | Drag the ring at the arrow tip |
| Exact values | Type them in the **Selected** panel |
| Run the simulation | **Fire thruster**, then **Pause** or **Reset** |

---

## Author

Christopher B. Slough. Physics teacher, Head of Science and Design Technology, and IB Physics examiner.
 README (1).md…]()
