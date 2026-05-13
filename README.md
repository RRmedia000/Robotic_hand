# 3D Printed Robotic Hand

A servo-driven robotic hand built with a 3D printed structure, fishing wire tendons, and an Arduino Mega. Pressing a button closes the hand by pulling four servos simultaneously.

---

## Why I built this

This project started as a practical portfolio piece — I wanted to build something real and hands-on that showed what I could do with electronics, 3D printing, and code all in one. A robotic hand felt like the perfect challenge.

Beyond the portfolio side of things, I'm releasing this completely free because I genuinely want to help the community. If this helps someone learn Arduino, get into robotics, or just have fun building something cool, that's more than enough for me. It was a great project to work on and I hope others get as much out of it as I did.

---

## How it works

The hand is 3D printed and actuated by four micro servos connected to an Arduino Mega. Each finger is linked to its servo via fishing wire routed through the palm — when the servos rotate, they pull the wire and curl the fingers closed. Elastic tendons on the back of the hand act as passive supports, keeping the fingers extended in the open position and returning them when the servos release.

A single button on pin 13 triggers the whole hand to close. Releasing the button lets the back tendons pull the fingers back open.

---

## Hardware

| Component | Details |
|---|---|
| Microcontroller | Arduino Mega |
| Servos | 4× micro servos |
| Servo pins | 3, 7, 8, 10 |
| Button pin | 13 |
| Structure | 3D printed |
| Tendon (pull) | Fishing wire |
| Tendon (return) | Elastic on back of hand |

---
##3D Print
Export hand5.3mf **without** supports!!
## Wiring

- **Servos** — signal wires to pins 3, 7, 8, 10. Power (red) to 5V rail, ground (brown/black) to GND rail on breadboard.
- **Button** — one leg to pin 13, other leg to GND. Uses Arduino's internal pull-up resistor, no external resistor needed.
- **Power** — use an external 5V supply (2A or more) to power the servos. Connect the supply GND to the Arduino GND to share a common ground.

---


> If 90° doesn't fully close the fingers, increase the angle — servos typically go up to 180°. Tune each servo individually if the fingers close unevenly.

---

## Build notes

- Route the fishing wire carefully through the finger channels so it pulls straight without binding.
- Tension the back tendons so the hand rests fully open but isn't fighting the servos when closing.
- The Arduino Mega's pin 13 has an onboard LED tied to it — it will light up when the button is pressed. This is normal and harmless.
