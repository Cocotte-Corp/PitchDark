# The Unit Test of the project

For the *Pitch Dark* project, we currently do not utilize traditional Unit Testing. This is primarily due to limitations within Unreal Engine 5’s testing framework, which does not adequately support scenarios focused on player-centric behavior. Since  is designed around dynamic player interactions and real-time gameplay elements, unit tests provide limited value in our development context.

Instead, our testing workflow emphasizes end-to-end validation of the game in its final production form. Before any changes are merged into the `Main Branch`, we perform full build tests using the Shipping configuration. This ensures that all performance, packaging, and runtime conditions are as close to the final release environment as possible. These build tests are configured with all the necessary parameters and optimizations intended for public release.

In addition to per-merge validations, we follow a structured release cycle. At the conclusion of each major development milestone or version, we generate and publish a tagged release on **GitHub**. This allows for version tracking, easy rollbacks if needed, and a clear history of progress throughout the project.

By focusing on real-world gameplay testing and production-ready builds, we ensure that *Pitch Dark* delivers a stable and immersive experience that aligns with the game’s design goals.
