# Elm render 2D game

This library aims to enable creating 2d games based on WebGL using elm.

TODO: pretty pictures and more examples


## Related Libraries

  * [game-resources](http://package.elm-lang.org/packages/Zinggi/elm-game-resources/latest) - A library for managing textures


## Goals

My current goal is just to enable users with no WebGL and GLSL knowledge to create simple games.
Hopefully this will eventually grow into something bigger, but currently that's what this is.

This library is for you, if
 * you want to create a simple 2d game as a learning experience
 * you want to use elm
 * you've used elm-graphics, but are looking for a slightly more powerful option without going full WebGL.


If you want to create a "real" game, I strongly recommend other options such as Unity / Unreal3/4 / LibGdx etc...


## Examples
 * [Jump and run](https://zinggi.github.io/elm-2d-game-examples/MarioLike.html) / [src](https://github.com/Zinggi/elm-2d-game-examples/blob/master/MarioLike.elm)

 * [Bouncy ball](https://zinggi.github.io/elm-2d-game-examples/bouncyBall.html) / [src](https://github.com/Zinggi/elm-2d-game-examples/blob/master/bouncyBall.elm)

 * [Random tests](https://zinggi.github.io/elm-2d-game-examples/example1.html) / [src](https://github.com/Zinggi/elm-2d-game-examples/blob/master/example1.elm)


## Vision

The vision for this library is to grow into something bigger.
Currently it only provides a way to render things to the screen.

It does not provide a way to structure your physics/gameplay code,
no resource management, no input management, no sound, no networking, etc.

However, the idea is that each of the mentioned missing topics can be created as a separate package that would live under the same namespace. E.g. a 2d physics engine might live in a package called `elm-game-2d-physics` and provide the namespace `Game.TwoD.Physics`

## Update log

* ** 2.0.0 -> 3.0.0 **
    * **Breaking changes:**
        - Removed `rectangle`. Use `shape rectangle` instead
        - Changed what the pivot affects.
        Previously, the pivot only affected the center of rotation. Now it also affects the offset in position. If you want the previous behavior, use `(x - px*w, y - py*h)` instead of `(px, py)` for position. TODO: fact check that!
    * ** New stuff: **
        - Added more prototyping shapes, thanks to [@yourSenchou](https://github.com/yourSenchou).

* **1.0.1 -> 2.0.0**
    * Updated to WebGL 2.0.
    * Renamed Vertex attribute `a_position` to `position`
