# Ender-3-V2-to-CNC-Conversion-Kit
<p align="center">
  <img src="https://github.com/user-attachments/assets/fde26a69-b4e4-4216-8b2c-7941ee93d98f" width="45%">
  <img src="https://github.com/user-attachments/assets/58074ded-d65f-4463-9266-b847b966a9f2" width="45%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/44ec8f83-43c1-4ada-b4b4-cba5a7c209e7" width="45%">
  <img src="https://github.com/user-attachments/assets/2e127329-a960-4753-9d7c-d55988c35208" width="45%">
</p>

## Description

This project features a modular CNC conversion of the Ender 3 V2 printer, transforming my old Ender 3 V2 into a belt-driven, gantry-style CNC. The design reimagines the stock aluminum extrusion frame, stepper-driven motion system, and V-wheel linear guidance architecture, while integrating a custom spindle assembly, rigid spoilboard, and structural gantry.

---

## Mechanical Overview

### Gantry Kinematics

<table>
  <tr>
    <td width="50%" valign="top">
        <strong>Axis Actuation & Functional Roles</strong><br><br>
        <strong>X-Axis (Red):</strong> Uses a belt-driven gantry designed for high-speed motion translation across the work area.<br><br>
        <strong>Y-Axis (Green):</strong> Focuses on translating the spindle across the bed, shifting the workpiece along the longitudinal plane.<br><br>
        <strong>Z-Axis (Blue):</strong> Uses a lead screw-driven assembly to manage tool depth, providing mechanical advantage over the controlled lifting forces.
    </td>
    <td width="50%" valign="top">
      <img src="https://github.com/user-attachments/assets/e897d695-331a-4e4c-8dd1-6997a34c39f1" width="450" alt="Kinematic Diagram">
    </td>
  </tr>
</table>

### V-Wheel System

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="https://github.com/user-attachments/assets/71585cb4-8a1d-4296-832e-db81c7f01ff1" width="85%" alt="V-Wheel Guidance System">
    </td>
    <td width="50%" valign="top">
      <strong>V-Wheel Constraint System</strong>
      <br><br>
      This system uses a triangular V-wheel layout to constrain motion along the aluminum extrusion. The two upper rollers and one lower roller create a three-point contact pattern that improves stability and reduces rocking under machining load. Ideler wheels are mounted directly to a Nema 17, both harvested from the V2
      <br><br>
     The V-wheels must be tightened enough to remove wobble, but not so tight that they create friction. This adjustment is important because loose rollers can cause deflection, vibration, and chatter during machining.
      <br><br>
      The Y-axis uses the same mechanism to constrain the spindle and promote movement along the Y-axis.
    </td>
  </tr>
</table>

## Spindle Assembly

<table>
  <tr>
    <td width="50%" valign="top">
      <strong>Spindle Mount and Z-Axis Integration</strong>
      <br><br>
      The spindle is mounted to the Z-axis carriage using a custom bracket designed to maintain alignment while cutting dense materials. The mount constrains the spindle body and positions the bit along the machine’s vertical axis.
      <br><br>
      The Z-axis uses a lead screw-driven assembly to control vertical motion and cutting depth. Because the spindle is placed to the side of the carriage, this region is succeptible to bending and vibration during machining.
      <br><br>
      The surrounding carriage and V-wheel system guide the spindle along the extrusion while resisting deflection.
    </td>
    <td width="50%" valign="top" align="center">
      <img src="https://github.com/user-attachments/assets/24975f8f-bd35-4c13-9b61-711f591c1358" width="90%" alt="Spindle Assembly">
      <br>
    </td>
  </tr>
</table>
---

## Machining Capability

It can machine wood, plastics, and composites, with performance depending upon spindle speed and depth of cut. Because the system is belt-driven and V-wheel guided, it is not intended for heavy material removal. Harder materials such as aluminum require shallow passes, low cutting forces, and careful control of vibration. Steel machining should be done using extremely light passes.The main goal of this system is to demonstrate machining potential on a repurposed 3D printer and to cut carbon fiber drone frames, which is it highly capable of. 
Spindle assembly and spindle can be changed to accomodate different spindles, so one can machine different materials per individual specs.

---

## Tolerances and Fits

Printed parts were designed with 3D printing tolerances in mind and was made with intent to print on an A1. Clearance was added around bolt holes, sliding interfaces, and mating features to account for printer variation and easier assembly.

For most parts, a clearance of.1 mm is used.

---

### Bambu Lab A1 Recommended Settings

Recommended material: **PLA or ABS**

| Setting | Recommended Value |
|---|---|
| Layer Height | 0.16–0.20 mm |
| Nozzle Diameter | 0.4 mm |
| Wall Loops | 5–7 walls |
| Top Layers | 6–8 |
| Bottom Layers | 6–8 |
| Infill Density | 60–80% |
| Infill Pattern | Gyroid or Cubic |
| Print Speed | Standard or slower |
| Supports | Build plate only where needed |
| Brim | Recommended for tall or narrow parts |

For highly loaded parts, such as spindle mounts, V-wheel brackets, and gantry plates, use **70–80% infill** with at least **6 wall loops**. Parts should be oriented so that the main cutting loads act across the layer lines instead of pulling directly between layers.

---

### Bill of Materials

1) M3 Bolts
2) M4 Bolts
3) M5 Bolts
4) Spindle of choice (500W Spindle was used by me)
5) Ender 3 V2

## Author's Note

This project was created to explore my design capabilities through iterative design process. I started with my old Ender 3 V2, which was my first 3D printer, and admittingly it was quite neglected once I built my Worlds Fastest Printer and bought an A1. Therefore, I was inspired to reinvent this printer into something as beautiful as it once was. I also needed a CNC to cut carbon fiber drone frames, so I thought why not. Rather than designing a CNC machine from scratch, I worked within the constraints of reusing the printer’s existing frame, motion system, motors, electronics, and hardware. Aside from standard M3, M4, and M5 bolts, the rest of the conversion was designed solely using parts already available from the printer and custom 3D printed components. This constraint made the project more interesting because every design choice had to account for stiffness, load paths, vibration, manufacturability, and the mechanical limits of the original platform. The goal was to transform a familiar machine into something more capable while pushing my understanding of mechanical design. I hope to build it within the weeks coming and plan to make reports once I do. I hope you enjoy.

