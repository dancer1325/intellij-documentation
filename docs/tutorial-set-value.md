[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-set-value.html)
[//]: # (Downloaded: 2025-12-17 20:04:47)

## Problem

Let's look at the following simple program:

import java.util.*; class Aquarium { private ArrayList<Fish> fish; public static void main(String[] args) { var aquarium = new Aquarium(); System.out.println(aquarium.getFish()); // fish has already been initialized System.out.println(aquarium.getFish()); // line n1 } private ArrayList<Fish> getFish() { if (fish == null) initFish(); return fish; } private void initFish() { fish = new ArrayList<>(Arrays.asList( new Fish("Bubbles"), new Fish("Calypso"), new Fish("Dory") )); } } class Fish { private String name; Fish(String name) { this.name = name; } public String toString() { return name; } } 

In this code, we have an instance variable `fish` that is printed out twice. It employs lazy initialization, which in our case means that the field is not assigned a value until its getter is called.

Consider the situation when you have already stepped to `line n1`, and `fish` has already been initialized, but you want to look into the `initFish` method? This method will only be executed if `(fish == null)` evaluates to `true`, which is no longer the case at `line n1`.

With this simple program, we could just restart the session. However, in more complex cases, you may find it very inconvenient to relaunch the session and reproduce the steps that lead to a certain state. Let's learn the smarter way.
