# Installation
If you don't have Blender 3D, get it here: https://www.blender.org/download/ Either version will work.
Download terrain_nodes.zip, DO NOT EXTRACT IT, open Blender, Preferences > Add-ons > Install then open location of terrain_nodes.zip and install.

# How To Use
If you have used Blender Nodes before this will be easy, a more detailed tutorial will be coming later..

Terrain Nodes add-on can be found Editor Type selector, where compositor and material editor selecters are. After opening the Terrain Nodes editor click New. Now you can create a node tree with Shift+A. You will need an input, such as an Image node, an Object node (see known issues) or a Generated Noise node. To filter the input with erosion, add Erosion Filter node. To output and begin calculations add an Output node and specify location for output.

# Tips
Opening Window > System Consoule will show you which node is being processed. For the Erosion Filter node it will give you estimated time for completion.

# Compatibility
Blender version 2.80

Requires NVIDIA graphics card, minimum compute capability 2.0 see this page for compatible graphics cards: https://en.wikipedia.org/wiki/CUDA#Version_features_and_specifications

# Known Issues
Currently this version is restricted to 1024x1024 max resolution for the Erosion Filter.

Object Input node - This node converts mesh to a height map. The restriction is that all of the vertices have to have equivalent distance between each other. This means that if you have a subdivided plane or A.N.T.Landscape generate object, the vertices inside that object cannot be moved in the X and Y direction (inside the mesh editor), only in the Z direction. For now this restriction allows for a fast height map generation on a single thread. This node is very useful for landscapes generated with the A.N.T.Landscape add-on.

Viewer node - Currently very buggy, either I don't know how to make it work properly or Blender's API needs to be updated to allow for proper view upadates. This node might be removed or changed completely.

Erosion node - Slope output does not output anything yet.

Interface - Node that is being processed will light up green. This usually works properly but sometimes will lag one node behind.

There is still a lot of fine-tuning and user safety code to write. The main goal right now is to test the basic functionality.

# Contact
If you have any problems / bugs / ideas / requests, please let me know. 

Discord: https://discord.gg/qQ2cYHQ

Email: val.barashkov at gmail.com

Twitter: https://twitter.com/ValeraBarashkov

# Thank You!
Thanks for using / testing Terrain Nodes!!
