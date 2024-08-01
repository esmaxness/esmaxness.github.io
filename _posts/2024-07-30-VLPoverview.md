---
layout: post
title:  Visual Light Positioning overview
date:   2024-07-30 14:05:10
description: General overview of VLP architecture, applications and advantages
tags: VLP
categories: iot
---
Visual Light Positioning (VLP) is a technology that uses visible light to determine the precise location of objects or people within a specific environment. This method leverages light-emitting diodes (LEDs), which are increasingly common in modern lighting solutions, to transmit data that can be received by photo sensors or cameras. 





The general architecture is composed of 4 building blocks:
<ul>
    <li>LED Light Sources: LED lights in a building are equipped with the ability to modulate their light output in a way that is imperceptible for the human eyes. Typically, frequencies under 50 Hz can cause headache and visual fatigue.  Frequencies between 50 Hz and 100 Hz also causes visual problems in workspaces. Frequencis between 100 Hz and 200 Hz causes visual fatigue in a long exposition, but it is less perceptible for humans.  To overcome visual fatigue in human the best frequencies are over 400 Hz.</li>
    <li>Cameras or photodiodes: these devices receive the modulated light signals. It is called Optical Camera Communication (OCC) when cameras are used.</li>
    <li>Decoding Signals: Devices decode the information embedded in the light. Frequencies provide information about the light source identifier and its precise location within the environment.</li>
    <li>Position Calculation: Using a tri-lateration algorithm, the device can calculate its exact position within the space.</li>
</ul>

#### Applications of VLP
<ul>
    <li>Indoor positioning for precise autonomous grounded vehicles positioning in airports shopping malls, or industrial areas.</li>
    <li>Asset tracking in warehouses and industrial areas.</li>
    <li>Context-awareness for improving Augmented Reality experiences.</li>
</ul>

#### Advantages of VLP
<ul>
    <li>It provides high accuracy in comparison to GPS. Usually, VLP systems provides positioning accuracy up to a few centimeters.</li>
    <li>Industrial scenarios usually present high interference from electromagnetic signals, so radio frequency-based systems are unsuitable.  VLP systems are immune to electromagnetic signals interferences.</li>
    <li>VLP systems are low-cost and energy efficient systems because they use existing lighting infrastructure. Mainly, the lighting infrastructure is based on LED lights which are  energy-efficient.</li>
</ul>

