# class147

 <!--Camera-->
        <a-entity position="0 0 15">
            <a-camera></a-camera>
        </a-entity>

        <a-entity
            sound="src: https://cdn.glitch.com/850dd813-e5e9-4dd0-9751-38981ae74172%2Ffh_space_discovery_-_earth_proud_music_preview(1).mp3?v=1604306441093; autoplay: true; volume: 0.5">
        </a-entity>

-----------------------------------

<a-sky> can be used to add 360 degree image texture or color to the scene.
The <a-sky> is a very large sphere which can have texture or color attached to the inner surface.
writes the code to add the <a-sky> tag inside the <a-scene> tag.


add a starry night texture to the sky.
add the sky image in the <a-sky> primitive.
Add an attribute src=“paste the link”.

<a-sky src="https://cdn.glitch.com/850dd813-e5e9-4dd0-9751-38981ae74172%2Fvia_lactea.png?v=1604296331712">

        </a-sky>
 ------------------------------------
 
 add textures to the sun and the planets.
 
 Note: Remove the color attribute of the sphere 
 
  <!--Sun-->
        <a-entity>
            <a-sphere position="0 0 0" radius="2"
                src="https://cdn.glitch.com/850dd813-e5e9-4dd0-9751-38981ae74172%2Fsol.jpg?v=1604296185621"></a-sphere>
        </a-entity>
  -------------------------------------
  repeat the same for other planets
  -------------------------------------
  how to show the orbiting path of the planets.
  
  
  Torus primitive in A-Frame to show the orbiting planet's path around the sun.
  
The <a-torus> helps to create tube shapes.

<!--Orbital Paths-->

        <!--Mercury-->
        <a-torus arc=180 color="grey" rotation="90 0 0" radius="5" radius-tubular="0.01" segments-tubular="1000"></a-torus>
-----------------------------------------
We can set many different attributes in <a-torus>.
Let’s discuss a few of them.
arc: This attribute sets the arc length of the tube. Default value is 360 degrees, a complete circular tube.
 
radius: This attribute sets the radius of the tube.
radius-tubular: This attribute sets the thickness of the tube.
segments-tubular: This attribute sets the number of segments the tube is made of. Default value is 32 segments.

set attributes position, rotation to modify the <a-torus> primitive.
arc=360 is by default

Try without arc value or with arc=180.



rotation= “90 0 0”
This will rotate the <a-torus> on the X-axis by 90 degrees.
radius: 0.3 radius-tubular: 0.01

Use arrow keys to zoom in and out to see the result.
---------------------------------------
Moon of planet--relative positions of the objects.


That means the position of one object depends on the other object.

Here in our solar system the position of earth depends on the sun, and the position of the moon depends on the earth.

So, revolving the moon around the earth, the moon has been the child entity of the earth.



 <!--Earth-->
        <a-entity position="0 0 0" rotation="0 0 0"
            animation="property: rotation; to: 0 360 0;easing:linear; loop: true; dur: 10000">
            <a-sphere position="10.5 0 0" radius="0.5"
                src="https://cdn.glitch.com/850dd813-e5e9-4dd0-9751-38981ae74172%2Fearth.jpg?v=1604312404511">
                <!--Moon-->
                <a-entity position="0 0 0" rotation="0 0 0"
                    animation="property: rotation; to: 0 360 0;easing:linear; loop: true; dur: 10000">
                    <a-sphere color="yellow" position="1  0 0" radius="0.2"></a-sphere>
                </a-entity>

            </a-sphere>
        </a-entity>
