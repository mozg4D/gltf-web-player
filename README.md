# 3D web player (gltf, glb, ..) *LinksPlayer (three.js based)

Usage: <iframe src="LinksPlayer.htm?id=1" allowfullscreen></iframe>

Example: https://3d-modellers.com/

Player automatically adapts to any 3D model. No input parameters needed.

prepare model using https://github.com/AnalyticalGraphicsInc/gltf-pipeline

Roadmap:
1. Adopt .basis image format (50% complete)
2. Windows application for 3D model preparation (using gltf-pipeline) and setting player attributes.
3. Advanced Cinema4D-like camera navigation
4. VR AR support
5. Set markers and links on 3D model

*Player can be used for other 3D formats. Use different loader for that https://threejs.org/docs/#manual/en/introduction/Loading-3D-models

If you need additional features for $ - contact me mozg4D@gmail.com

Cinema4D + Redshift workflow:

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_2.jpg)

0 - make your 3D model
1 - find "Bake Object..." comand in "Customize Commands"
2 - select objects that you want to bake and execute "Bake Objects..." command
3 - In "Bake Object" window deselect "illuminate" option, select desired texture resulution, set pixel border to 8 and supersampling to 1
"Bake Object" will unwrap UV's for you
4 - Create "Redshift BakeSet" object
5 - Add objects that you want to bake with global illumination to "Redshift BakeSet" --> Objects
6 - Set desired resolution and bake

You can use Cinema4D "Bake object" comand with "illuminate" option on and skip redshift baker

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_1.jpg)




