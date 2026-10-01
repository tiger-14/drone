# TSA Drone Project
A custom-built quadcopter drone with an integrated claw and live video feed, designed to remotely locate and retrieve caged and uncaged animals for TSA's 2026 Drone Challenge (Safari Rescue mission).

<img width="601" height="598" alt="image" src="https://github.com/user-attachments/assets/5db0209b-1781-4c3a-ad2e-87f845e1ab5b" />

<img width="982" height="625" alt="image" src="https://github.com/user-attachments/assets/326455fe-56a2-43a1-b644-139c3d407ec6" />

## 30+ Page Documentation Portfolio
The portfolio documents the complete build process of the drone with a photo log, a work log, engineered drawings, wired diagrams, and more!

[IHC Documentation Portfolio - Drone Challenge UAV  (1).pdf](https://github.com/user-attachments/files/29614611/IHC.Documentation.Portfolio.-.Drone.Challenge.UAV.1.pdf)

## Features

- 3D-printed frame, base structure, and claw mechanism, designed in SolidWorks
- 4x brushless motors (RS2205 2300KV) with tri-blade propellers for lift and thrust
- SoloGood F722 flight controller stack running Betaflight firmware in Angle Mode for automatic self-leveling
- BetaFPV ELRS 2.4GHz receiver paired with a BetaFPV controller for piloting
- Raspberry Pi Zero WH running Raspberry Pi OS, controlling the claw servos and USB webcam independently of the flight stack
- 3x SG90 micro servos actuating a 3-pronged claw for picking up and releasing targets
- XT30/XT60 smoke stopper for short-circuit protection
- Dual 3S LiPo 11.1V 5000mAh batteries

## How it works

The pilot flies the drone using a BetaFPV controller, which sends inputs to the onboard ELRS receiver at up to 500Hz. Betaflight, running on the SoloGood F722 stack, reads these inputs alongside data from the onboard IMU (gyroscope + accelerometer) and calculates motor outputs at 4-8kHz to keep the drone stable. In Angle Mode, the drone self-levels whenever the sticks are centered, which keeps it steady during claw operations without needing constant manual correction.

A Raspberry Pi Zero WH, handles the claw and camera. It drives the 3 SG90 servos that open and close the claw, and streams a live feed from a USB webcam back to the pilot's laptop for target identification. Betaflight and the Pi operate independently: Betaflight handles flight, the Pi handles the mission payload.

## Bill of Materials

| Part | Description | Qty |
|---|---|---|
| Anycubic Kobra 2 | 3D printer | 1 |
| Sunlu PETG | Print filament | 4 |
| Drone Frame (3D-printed) | Upper + lower frame housing all components | 2 |
| XT30/XT60 FPV Smoke Stopper | Short-circuit protection | 1 |
| Raspberry Pi Zero WH | Claw + video control | 1 |
| OVONIC D15 Dual LiPo Charger | Battery charging | 1 |
| 3S LiPo 11.1V 5000mAh | Power | 2 |
| BetaFPV Controller | Piloting | 1 |
| BetaFPV ELRS (2.4GHz, 500Hz) | Radio link | 1 |
| SoloGood F722 Stack | Flight controller | 1 |
| Readytosky RS2205 2300KV Brushless Motor | Lift/thrust | 4 |
| 5.1" 3-Paddle Propellers | — | 12 |
| Webcam | Target ID / video feed | 1 |
| SG90 Micro Servos | Claw actuation | 3 |
| 5V Converter | Powers Pi + servos | 1 |
| Claw (3D-printed) | Pickup mechanism | 1 |

## Compliance

Built and flown in accordance with FAA Part 107 and Remote ID requirements, 400ft altitude ceiling, and Georgia state UAS regulations. Full regulatory breakdown in the documentation portfolio.

## Credits

Built by Benjamin Antony, Taran Vijayakumar, Nathaniel Ramnath, and Ivin George for South Forsyth High School's TSA chapter — Georgia TSA SLC 2026, Athens, GA.

3D model sources: claw arm, landing gear, propeller guard, Pi enclosure, servo/webcam mounts, and drone frame base are credited with links in the documentation portfolio's Resources section.

## License
<img width="210" height="109" alt="image" src="https://github.com/user-attachments/assets/6999c28c-aa88-49fd-bd41-8bc148aaae9e" />
