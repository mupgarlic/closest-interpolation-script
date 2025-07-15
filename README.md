# closest-interpolation-script
Blender script to change the "Interpolation" from all your Image Texture nodes in one click.

```python
import bpy

for material in bpy.data.materials:
    if material.use_nodes:
        nodes = material.node_tree.nodes
        target_node = nodes.get('Image Texture') 
        if target_node:
            target_node.interpolation = 'Closest'
```
Copy this script in the "Text Editor" and run it (Alt + P over the editor) to instantly set interpolation to 'Closest'. I made this to quickly fix the blurry effect on the textures of the 3D models you import from 'Mineways'. :D
