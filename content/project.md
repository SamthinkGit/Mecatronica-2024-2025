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

# Modeling Eva's Body in FreeCAD 🛠️

This section explains the process of designing Eva's body, starting with a spherical base that is deformed into an ovoid shape and using cutting and slicing operations to shape it into the desired form.

---

## Step 1: Creating the Spherical Base 🌐
1. **Insert a Sphere:**
   - Open the **Part Workbench**.
   - Insert a sphere using the **Create Primitive** tool.
   - Adjust the sphere's radius to roughly match the initial size of Eva's body.

<div align="center">
    <img class="logo" src="../media/project/body-sphere.png" alt="image" width="30%">
</div>

> FreeCad File: `Drafts/Sphere`

2. **Deform the Sphere into an Ovoid:**
   - Use the **Scale Tool** or adjust the properties of the sphere to stretch it along the Z-axis.
   - This creates the ovoid shape characteristic of Eva's body.

3. **Position the Ovoid Shape:**
   - Move the deformed sphere along the Z-axis to align it with the overall design.
   - Ensure it represents the main volume of the body.

<div align="center">
    <img class="logo" src="../media/project/body-base.png" alt="image" width="30%">
</div>

> FreeCad File: `Non-Sized-Parts/.../EvaBody/Body/Sphere001`

## Step 2: Shaping the Neck 🌀

1. **Build Other Sphere:**
   - Generate another sphere with the same radious
   - Locate the sphere at the neck.

2. **Perform a Boolean Cut:**
   - Use the **Boolean Difference Tool** to subtract the smaller ovoid from the larger one.

<div align="center">
    <img class="logo" src="../media/project/body-neck.png" alt="image" width="30%">
</div>

## Step 3: Shaping the Body ✂️
1. **Slice the Ovoid:**
   - Insert a rectangular **Cut Plane** using the **Part Workbench**.
   - Position the plane to remove the bottom portion of the ovoid, flattening the base.
   - Use the **Boolean Cut Tool** to perform the slice.

2. **Create the Arm Openings:**
   - Insert two smaller spheres to represent the arm sockets.
   - Position these spheres symmetrically on the sides of the hollow body.
   - Use the **Boolean Difference Tool** to cut the arm sockets out of the body.

<div align="center">
    <img class="logo" src="../media/project/body-plane-cut.png" alt="image" width="30%">
</div>

## Step 4: Refining the Model ✨
1. **Smooth the Edges:**
   - Apply the **Fillet Tool** to round any sharp edges left from the slicing and cutting operations.

2. **Validate the Design:**
   - Ensure all operations were performed correctly and the resulting body is symmetrical and smooth.

<div align="center">
    <img class="logo" src="../media/project/body-shape.gif" alt="image" width="30%">
</div>

## Construction Tree Breakdown 🌳
| Step            | Operation         | Description                                |
|-----------------|-------------------|--------------------------------------------|
| `Sphere001`     | Create Sphere     | Main body volume                           |
| `Sphere002`     | Create Smaller Sphere | Inner cavity for hollowing the body       |
| `ArmCutLeft`    | Add Sphere        | Sphere positioned to cut left arm socket   |
| `ArmCut`        | Add Sphere        | Sphere positioned to cut right arm socket  |
| `Slice`         | Add Cut Plane     | Plane used to flatten the bottom           |
| `CuttedBody`    | Boolean Operations| Final body after all slicing and cutting   |


The body design is now ready for further detailing, such as attaching arms or adding internal mechanisms.

