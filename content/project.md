# Designing Eva from Wall-E for a Mechatronics Project 🛠️

## Introduction
This document outlines the process of designing a 3D model of Eva from the movie *Wall-E*. The model is part of a semester-long mechatronics project, aimed at replicating Eva's iconic design for potential integration with robotics and automation. The design process will involve creating each part of Eva step-by-step using FreeCAD, starting with the head.

---

# Modeling Eva's Head in FreeCAD 🛠️

This section outlines how to model the head of Eva from *Wall-E* in FreeCAD using the **Sketcher** and **Part Design** workbenches. The head's round and smooth shape is created by sketching a profile and then using the Revolve tool to generate a 3D solid.


## Step 1: Drawing the Profile ✍️
The head's profile is drawn as a 2D cross-section of the shape that will be revolved.

1. **Create a New Sketch:**
   - Select the **XY Plane** as the sketching plane.
   - Click on **Create New Sketch** in the toolbar.

2. **Draw the Outline:**
   - Use the **Arc Tool** to draw the rounded top part of the head.
   - Use the **Line Tool** to draw the sides and base of the profile.
   - Ensure the lines and arcs form a closed shape.

<div align="center">
    <img class="logo" src="../media/project/drawing.png" alt="image" width="40%">
</div>

> FreeCad File: `Drafts/HeadSketch`

## Step 2: Revolving the Profile 🔄
1. **Switch to Part Design Workbench:**
   - Exit the Sketcher and switch to the **Part Design** workbench.

2. **Apply the Revolve Tool:**
   - Select the completed sketch in the Model Tree.
   - Click on **Revolve** in the toolbar.
   - Set the revolution axis as the vertical construction line from the sketch.
   - Choose **360 degrees** for the full revolution.

<div align="center">
    <img class="logo" src="../media/project/head.png" alt="image" width="40%">
</div>

> FreeCad File: `Drafts/Revolve`

## Result

The 2D sketch is now a 3D solid representing Eva's head.

<div align="center">
    <img class="logo" src="../media/project/head.gif" alt="image" width="40%">
</div>
