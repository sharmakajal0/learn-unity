## Cameras in VR

In the real world, when we want to take a 2D image of a 3D object, we normally use a camera. In 3D graphics, we use a normal camera. This virtual camera performs a perspective transform, which maps the object into 2D. The camera itself is positioned in 3D space. It has a transform which gives it a position and a rotation. The 2D images taken of the object from the position of the camera. So it is an image taken from the perspective of the camera, just like a real world camera. You can retake the camera, and so change the direction in which it's looking, just like a real world camera. So in a traditional 3D camera, your job is to position the camera just like a real world photographer to get the scene from the point of view that you want.

In VR, it's a bit more complicated. One of the most notable things about VR is that you have two screens in your headset, one for each eye. That means you need two images of the scene, one for your left eye and one for your right eye. To do that you need two virtual cameras. These cameras need to be spaced apart, the same distance apart as your eyes. But they need to be rigidly linked together, so that they move together, just like your real eyes.

Most importantly, the cameras move when your head moves. In all VR systems, there will be a rotation tracker that maps the rotation of your head onto the rotation of the cameras. So your view of the virtual world turns as you turn your head, just like the real world.

In high end systems, the same goes for your, move your head backwards and forwards, and left and right, linking the motion of your headset to the translation of the camera. It is this link between your head movements and the transforms of the camera that creates the VR experience.

## VR mode in Unity

VR mode is Unity's endeavor to try and make getting to work with VR content within Unity as simple as possible.

Each Scene has got a camera. If we want to export this out to a phone, it will just look the same. But when we're working with VR, we don't only want that.

So for instance, if it's in a Cardboard, it would need to be split into two separate stereo views, and there would need to be some distortions in there. 

## Keyframe Animation

One of the most flexible ways of creating movements for virtual reality is Keyframe Animation.
In early days, they created animation by:-
- They drew a lot of images and each image was subtly different from the previous one so that when you played them one after the other it looked like movements. So this was a fantastic way of creating appearance of the movements. For this you had to draw lots and lots and lots of images. Hence it's an enormous amount of work.

On a computer it's a lot easier to do the animation. You can create the most important animations which are called as keyframes. You can create these keyframes and the computer will do the animation for you.

Unlike physics, you are not you're not constrained by the laws of physics, and also you can do much more complex animations than you could do with a physics simulation.

## Materials

Objects in 3D graphics are made out of polygons and vertices. They form the shape of the object, which of course important. But if all you had was shape, objects would look pretty  boring.

In fact, real objects have a lot of other features. They have colors. They may have fine detail on the surface. And they can also have other properties which affect how they look. They could be shiny or dull, they could be smooth or rough. These are all properties of the surface of the object, and in most cases, they define how light interacts with that surface. Because we see things through the light that is reflected of an object, the interaction of light on the surface fundamentally affects how things look. These complex surface properties are represented in 3D graphics by something called a material.

## Lights in VR

The appearance of an object comes from how light interacts with its surface. One important part of that is shading.
We can see the 3-D shape of an object by the pattern of light and shadow on its surface as the light reflects off it. You can see on this object, there is a highlight and a shadow, which really shows how it looks in 3-D. Without this shading, the object just looks flat. So to create really 3-D looking objects, we need light.

In VR as well as virtual objects and virtual cameras, we have virtual lights. These are mathematical models of a light source that are used in a set of calculations that determine the shading of objects. They can have positions in 3-D space using transforms just like cameras. So the way you position or rotate a light can affect how it lights up an object. If a part of an object is facing the light, it will appear bright. Otherwise, it will appear dark or in shadows.

There are several types of lighting in 3-D graphics.
- **Directional Lights** - This is a light that shines in a particular direction but doesn't have a position. It just lights everywhere from that same direction. Directional lights are like the sun. Light just comes from the direction of the sun. It doesn't matter how near or far you are from it. It just lights up everything facing the sun.
- **Point lights** - Lights have a position but they send out lights in every direction. With a point light, what matters is if you're facing the position of the light and also how near or far you are from that light. The nearer it is, the brighter it will be.
- **Spotlight** - SpotLight has both a position and a direction. Just like a theater spotlight or an Anglepoise lamp, it has a beam of light that comes from it, and everything in that beam is illuminated. All of these lights represent real-world light sources, and you can use them to build up complex and interesting lighting patterns from them that will start to make your objects and your environment look really good.
