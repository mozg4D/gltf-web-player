# 3D web player (gltf, glb, ..) *LinksPlayer (three.js based)

Usage: <iframe src="LinksPlayer.htm?id=1" allowfullscreen></iframe>

Example: http://mozg4d.com/LinksPlayer/

Player automatically adapts to any 3D model. No input parameters needed.

prepare model using https://github.com/AnalyticalGraphicsInc/gltf-pipeline

V 1.1 (June 28 2019) : Exported camera support; load time and performavece improvements

Roadmap:
0. Cinema4d-like navigation
1. Adopt .basis image format (50% complete)
2. Windows application for 3D model preparation (using gltf-pipeline) and setting player attributes.
3. Advanced Cinema4D-like camera navigation
4. VR AR support
5. Set markers and links on 3D model

*Player can be used for other 3D formats. Use different loader for that https://threejs.org/docs/#manual/en/introduction/Loading-3D-models

If you need additional features for $ - contact me mozg4D@gmail.com

Cinema4D + Redshift workflow:

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_2.jpg)

0. make your 3D model
1. find "Bake Object..." comand in "Customize Commands"
2. select objects that you want to bake and execute "Bake Objects..." command
3. In "Bake Object" window deselect "illuminate" option, select desired texture resulution, set pixel border to 8 and supersampling to 1
"Bake Object" will unwrap UV's for you
4. Create "Redshift BakeSet" object
5. Add objects that you want to bake with global illumination to "Redshift BakeSet" --> Objects
6. Set desired resolution and bake

You can use Cinema4D "Bake object" comand with "illuminate" option on and skip redshift baker

Exporting GLTF:

use this amazing GLTF exporter by Basel Abu-sininni
https://labs.maxon.net/?p=3360

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/cinema4d_1.jpg)

1. turn on "Color" channel and set it's brightness to 0
2. turn on "Luminance" channel and set it's texture to recently baked one
3. turn on "Reflectance" channel and set reflection and specular strenghts to 0
4. Add camera (to overwrite default view angle in GLTF player)
5. (7) export with "export camera" and "export to binary" options on in "GLTF export options" window

* You must export fully baked scene. Web 3D player does not have light sources, nor it provedes environment maps due to peformance and load tilme issues

If you've done everything correctly, scene in web player should look EXACTLY as in cinema4D:

![Cinema4D workflow](https://github.com/mozg4D/gltf-web-player/blob/master/result.jpg)

To speed up the development of player feel free to donate some) or to upvote features you need the most)
https://www.paypal.me/mozg4d
