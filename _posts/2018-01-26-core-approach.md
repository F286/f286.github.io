---
published: true
---
## Leadership

- Important to have a good atmosphere : )

- Important to have an open atmosphere. That is, an atmosphere of open conversation about how code is structured and ways of accomplishing tasks.

- Read Extreme Ownership by Jocko Willink. 

## Design

When developing apps professionally as general guidelines we do things in three phases. *Prototype, Build, and Polish*.

1. Define the *Target Goals* for a prototype

2. Prototype in Unity, exporting to the iPad. It is important to iterate, and hit all Target Goals *simultaneously*. *Test with kids!*

3. Build the app based on the prototype. *Test with kids!*

4. Polish the app, tweaking the graphics, interactions and minor bugs once we have a releasable app.

## Best Practices

### You can drag a prefab into a scene, and it just works.

Easier to test in Editor, a prefab can be tested by simply
dragging it into the scene.

- Simplifies object creation - GameObject.Instantiate() just works!

- Easier for code to work with *Edit and Continue*, where I can
rapidly iterate by editing code while the Editor is in Play Mode.

### Content can be created and edited in the Unity Editor without code

- Allows Designers to work in the Unity Editor directly

- Allows Designers to be productive with less back and forth with
Programmers

- Easier to scale content creation to a large project

- Most data is stored on prefabs as public fields

- *Example:* An Designer can create a new Block from scratch by
creating a prefab, and create the graphics for it without back
and forth with a programmer

### Leverage Unity, go with the grain

- Public fields in the Unity Inspector should be used to hook up
references between objects. This is easy to inspect and debug.

- All object state should be viewable though the inspector, you
can then click on GameObjects while in Play Mode and debug
and experiment easily. There are tricks such as using
[Serializable] structs which allow for inspectable sub-objects.

- Unity’s built-in functionality is very consistent across platforms,
so it will lead to less bugs when targeting new platforms.

### KISS: Keep it super simple

- Advanced language features such as Reflection have inconsistent
behaviour across platforms, since the code is auto-translated,
which can lead to bugs which occur only on device which are very
painful.

- Plugins are good if not too invasive, or there is a strong need that
is not possible with built-in functionality (Example: DOTween,
Android native functionality)

- Keep number of lines of code as few as possible, as more code
will lead to more bugs and is harder to maintain

- Don’t over structure code. It’s good to keep state as public fields so they can be viewable from the inspector.

## Conclusion

All of this will directly lead to less bugs, faster development, and a higher quality product. The code will be simpler, which means less bugs. This will let you focus on fun things such as making the app, instead of staying up until morning to fix an iPad specific bug. Unity will be leveraged, this will let you develop at least three times faster. This means more beach time and less working weekends time. Design will be integrated, which means you won't have to redo the same thing three times.<sup>1</sup> 

Expanding your mindset can feel like changing your religion. The archetypal hero will do this, painfully, and be reborn. Be the hero. Slay the dragon. Get the princess.

<sup>1</sup> Relatively modest increases in productivity will lead to exponential increases in output, since the 'rich get richer, and the poor get poorer'. Related to the Pareto Distribution. [Link](https://youtu.be/-k_FfS1kHfY)
