# sim_generic_vr

Generic Unity3D project with included submodules, used to work on scenes and assets independently of a given hardware configuration. This repository can then be used as a template to develop a specific wheelchair simulator.

Note: The same structure and installation/edition method applies for any toplevel repository, such as `sim_irglm_vr`.

In the `Assets` folder of this repository, there are several git submodules that implement different modular aspects of the simulator:

  - `vr_scenes` : This is the main submodule. It contains the scenes to simulate, and most static (non-moving) assets. Static assets are benches, light posts, etc., and they are prefabs that include their geometry, textures and colliders. The scenes generally make references to other contents from the `vr_dynamic_objects`, `vr_street_lights` and `vr_user` submodules.
  - `vr_dynamic_objects` : Dynamic objects such as pedestrians and cars, as prefabs that include their geometry, textures, colliders, animators and scripts.
  - `vr_street_lights` : Configurable street light and road prefabs that allow interaction with the user with a push button.
  - `vr_user` : A game object with basic physics, one main camera and colliders that represents the user in a first-person point of view. This is also where we put the interfacing scripts with external devices, such as DBox, haptics, motion analysis.

## Installing

This repository must be cloned including its submodule, using:

```
git clone --recurse-submodules git://github.com/wheelsims/sim_generic_vr
```

If you're using SourceTree, choose `New` → `Clone from URL` and fill these informations:

![image](https://github.com/WheelSims/sim_generic_vr/assets/34967663/d9d2e243-29f7-4dea-994a-e5b46fa4fef7)

Once cloned, the project looks like this in SourceTree (note the submodules):

![Screen Shot 2024-02-14 at 15 37 06](https://github.com/WheelSims/sim_generic_vr/assets/34967663/5093f6aa-ee5a-4223-9402-8472cb9290a4)

In the screenshot above (which was not taken right after a clone), we can see that two submodules need our attention. These ones need both pushes and pulls.


## Updating (pull)

To update the whole project to the newest version, double-click on every submodule to open it in its own window, then pull its changes.

![image](https://github.com/WheelSims/sim_generic_vr/assets/34967663/d4e2efba-0d0c-493c-8c35-79157907dab6)


## Editing

When working on the game, one must make sure that the new files (scripts, textures, etc.) added to a scene are placed in the correct folder, so that they will be added to the right repository.

## Committing

To commit the changes, start by commiting and pushing every change to the submodules. Then, commit and push the changes to the main repository.
