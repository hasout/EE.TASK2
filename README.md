Algorithm for Walking Motion in Humanoid Robot
🦿 Assumptions:
Servo 1 (D9): Left Hip

Servo 2 (D10): Left Knee

Servo 3 (D11): Right Hip

Servo 4 (D12): Right Knee

Each leg consists of two joints.

Movement is simplified to forward walking (no balancing).

🧠 Walking Motion Logic (High-Level Pseudocode):
Initialize servos.

Set all servos to standing position.

Repeat walking cycle:

Lift left leg:

Raise left knee (servo 2).

Tilt left hip forward (servo 1).

Move left leg forward:

Lower left knee (servo 2).

Shift weight to left leg.

Lift right leg:

Raise right knee (servo 4).

Tilt right hip forward (servo 3).

Move right leg forward:

Lower right knee (servo 4).

Shift weight to right leg.

 Notes:
Tune write() angles based on your servo calibration and robot structure.

Use delay() for timing; later you can optimize using millis() for smoother motion.

For real-world implementation, consider adding balance sensors (e.g., MPU6050).
