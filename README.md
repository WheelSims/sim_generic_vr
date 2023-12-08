# sim_generic_vr

Generic Unity3D project with included submodules, used to work on scenes and assets independently of a given hardware configuration. This repository can then be used as a template to develop a specific wheelchair simulator.

The Assets folder contains git submodules that implement different modular aspects of the simulator:

  - `vr_static_objects` : Static objects such as benches, light posts, etc., as prefabs that include their geometry, textures and colliders. This can also includes larger prefabs that combine many related prefabs (e.g., a complete room), but not a complete scene (scenes include more components such as volumes, sky boxes, etc. and are versionned in `vr_scenes`).
  - `vr_dynamic_objects` : Dynamic objects such as pedestrians and cars, as prefabs that include their geometry, textures, colliders, animators and scripts.
  - `vr_street_lights` : Configurable street light and road prefabs that allow interaction with the user with a push button.
  - `vr_user` : A game object with basic physics, one main camera and colliders that represents the user in a first-person point of view. We can then add more cameras and scripts to this game object to interact with other systems (e.g., DBox, haptics, motion analysis).
  - `vr_scenes` : Different worlds built using the prefabs from `vr_static_objects`, `vr_dynamic_objects`, `vr_street_lights` and `vr_user`.

## Installing

This repository must be cloned including its submodule, using:

```
git clone --recurse-submodules git://github.com/wheelsims/sim_generic_vr
```

## Editing

When working on the game, one must make sure that the new files (scripts, textures, etc.) added to a scene are placed in the correct folder, so that they will be added to the right repository.

## Committing

Changes must be first committed to submodules, then to the main repository.
