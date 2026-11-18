# OOAD / UML Diagrams — Desi Auto Dhamaal

Five diagrams based on the actual HTML5 Canvas JavaScript game in `../index.html`:

1. **Class diagram** — conceptual classes for game state, player, traffic, missions, audio and input. The code is procedural JavaScript, so these are *analysis classes*, not literal ES6 classes.
2. **Use case diagram** — player interactions and game capabilities (represented using a Mermaid flowchart because Mermaid has no native UML use-case syntax).
3. **Activity diagram** — start, gameplay update, collision, drop-off, pause and game over.
4. **Sequence diagram** — interaction between input, game loop, mission, traffic, audio and renderer.
5. **Component diagram** — browser-based architectural modules (represented with a Mermaid flowchart).

## Viewing

GitHub can preview Mermaid diagrams when their source is pasted inside a fenced `mermaid` block in Markdown. You can also open the `.mmd` files in [Mermaid Live Editor](https://mermaid.live/) or with a Mermaid preview extension in VS Code.

## Important implementation notes

- Collisions use axis-aligned bounding boxes (AABB) with a narrower effective player width during a wheelie.
- The player has 3 lives; crashes cost a life and 20 points. A missed drop costs 50 points.
- A successful passenger delivery increases the level and awards `100 + floor(remainingTime) * 2` points.
- Music and sound are generated with Web Audio, with optional local audio files.
