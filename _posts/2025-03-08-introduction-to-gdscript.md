---
layout: post 
title: Introduction to GDScript 
date: 2025-03-08 12:00:00 
summary: A quick overview of GDScript, the language behind Godot Engine. 
categories: godot gdscript programming
---

GDScript is a high-level, dynamically typed programming language specifically designed for Godot Engine. 
It is tightly integrated with the engine, making it an excellent choice for game development in Godot. 
GDScript is optimized for simplicity and performance, providing a straightforward syntax that is easy to learn and use.

All links are easy to locate and discern, yet don't detract from the harmony of a paragraph. 
The same goes for italics and bold elements. Even the strikeout works if 
<del>for some reason you need to update your post</del>. For consistency's sake, 
<ins>The same goes for insertions</ins>, of course.

Example of GDScript in Action

Here’s a simple GDScript example that moves a character in the game:

{% highlight gdscript %} extends KinematicBody2D

var speed = 200

func _ready(): pass

func _process(delta): var motion = Vector2()

if Input.is_action_pressed("ui_right"):
motion.x += 1
if Input.is_action_pressed("ui_left"):
motion.x -= 1
if Input.is_action_pressed("ui_down"):
motion.y += 1
if Input.is_action_pressed("ui_up"):
motion.y -= 1

motion = motion.normalized() * speed * delta
move_and_slide(motion)

{% endhighlight %}
Syntax and Structure

GDScript’s syntax is simple and clear, resembling Python. 
It uses indentation to define blocks of code instead of braces, making the structure visually clean.
Functions

Functions are defined using the func keyword, and the return type is inferred. In the example above, 
_ready() is called when the object is initialized, and _process() is called every frame.
Variables

Variables can be declared using the var keyword, and the language supports type hinting for clarity. 
For example, var speed: int = 200 would define a variable with a specific type.
Lists and Loops

GDScript supports loops and lists, which are essential for game development. 
Here's an example of looping through an array:

{% highlight gdscript %} var items = ["Sword", "Shield", "Potion"]

for item in items: print(item) {% endhighlight %}

This code will print each item in the array to the console.
Signals and Events

GDScript allows easy handling of events using signals. You can connect signals to functions, 
allowing for reactive programming. For example, emitting a signal when a player picks up an item:

{% highlight gdscript %} signal item_picked_up

func _on_item_picked(): emit_signal("item_picked_up") {% endhighlight %}
Conclusion

GDScript is a fantastic language for anyone getting started with game development in Godot. 
It is designed to be both beginner-friendly and powerful, enabling rapid development without sacrificing performance. 
Whether you are making 2D or 3D games, GDScript is a tool that will fit perfectly within your development process.

Happy coding!
