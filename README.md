# aframe-blink-teleportation

Blink-Teleportation Component For A-Frame.

![](https://github.com/thedart76/aframe-blink-teleportation/blob/master/aframe-blink-teleportation-v104.gif)

## Properties

| Property         | Description                                                      | Default Value |
| :--------------- | :--------------------------------------------------------------- | :------------ |
| camera           | Custom camera's ID.                                              | #cam          |
| cameraRig        | Custom camera rig's ID.                                          | #camRig       |
| raycasterObjects | Class name for selective intersections.                          | .clickable    |
| dof              | Specifies if targeted device is 3DOF or 6DOF.                    | 6             |
| hand             | Customisable value for Oculus Go only.                           | right         |
| color            | Fade-out image color.                                            | #000000       |
| pos              | Position to which the user will be teleported.                   |               |
| dur              | Duration of the black image animation (Fade IN - Fade OUT)       | 250           |
| hide             | Used to hide the blink-teleportation entity after clicking on it | false         |

💻 [**TRY THE DEMO**](https://thedart76.github.io/aframe-blink-teleportation/ "**TRY THE DEMO**")

------------

## Usage

### Requirements

You can attach the **blink-teleportation** component to any entity, but, if you use flat objects such as planes or images, you want to install also the [aframe-look-at-component](https://github.com/ngokevin/kframe/tree/master/components/look-at/ "aframe-look-at-component") created by Kevin Ngo for a better UX.

🙏 Thank you for your amazing components, [Kevin](https://github.com/ngokevin "Kevin")!

------------

### Browser Installation

Install and use by directly including the [browser files](https://github.com/thedart76/aframe-blink-teleportation/tree/master/js "browser files"), plus the required and suggested components:

	<head>
	    <title>Blink-Teleportation Component</title>
	    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
	    <script src="https://raw.githack.com/thedart76/aframe-blink-teleportation/master/js/aframe-blink-teleportation-min.js"></script>
	    <!-- SUGGESTED/REQUIRED COMPONENT FOR FLAT OBJECTS -->
	    <script src="https://unpkg.com/aframe-look-at-component@0.8.0/dist/aframe-look-at-component.min.js"></script>
	</head>

### Instructions

For the **blink-teleportation** component to work correctly, you should:

**1)** Use a camera rig

**2)** Disable the wasd-controls (Desktop mode)

**3)** Use classes on clickable objects (selective intersections)

For example:

	<!-- CAMERA RIG -->
	<a-entity id="cameraRig">
	    <!-- CAMERA -->
	    <a-camera wasd-controls-enabled="false">
	    </a-camera>
	</a-entity>

	<!-- THEN SET class="clickable" ON ANY BLINK-TELEPORTATION ELEMENT -->
	<a-entity blink-teleportation class="clickable"></a-entity>

### Important Notes

⚠️ Since the **blink-teleportation** component automatically sets selective intersactions using `raycaster="objects: .clickable"`, don't forget to set `class="clickable"` on all the objects the user can interact with in your scene.

⚠️ Because of the order-dependent rendering in A-Frame, make sure to place the lines of code for the camera rig and its child entities at the bottom of the HTML mark-up.

------------

👀 [**VIEW THE DEMO SOURCE CODE**](https://github.com/thedart76/aframe-blink-teleportation/blob/master/index.html "**VIEW THE DEMO SOURCE CODE**")


👀 [**VIEW THE COMPONENT SOURCE CODE**](https://github.com/thedart76/aframe-blink-teleportation/blob/master/js/aframe-blink-teleportation.js "**VIEW THE COMPONENT SOURCE CODE**")

------------

## License

Distributed under an [MIT License](https://github.com/thedart76/aframe-blink-teleportation/blob/master/LICENSE "MIT License").

Designed an coded by Danilo Pasquariello - [July 2018](https://twitter.com/theDart76/status/1019581230013206529 "July 2018")
