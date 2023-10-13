# layering header only dependencies with tipi

This example showcases how to shadow a dependency using a local project copy of it.

- `/3rdparty/msm-alt` contains a slightly modified version of `boostorg/msm` (added a ctor to `state_machine_def` that writes a string to stdout for sake of demoing change)
- the `./tipi/deps` file has a local project entry that places the dependency on the project's include path in a way that the `msm` that is brought in by the dependency to `boostorg/boost` gets shadowed


> NOTE: this might break in more complex cases where it's probably more sane to maintain a fork or the impacted dependency sub tree