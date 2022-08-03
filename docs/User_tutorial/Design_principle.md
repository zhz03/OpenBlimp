# Design principle

To build a successful blimp, you need to follow some basic design principles. 

Design principle involves two aspects:

- Payload estimate and checking: Whether the designed airship can be effectively suspended in the air.
- Motion primitives checking: Whether the designed blimp can effectively move in the 3D space

Please use following checkbox to see if your design satisfy these principles:

**Principle 1:** To allow the designed airship to maintain neutral buoyancy in the air. You need to make sure the following equation satisfied:


$$
F_B - m_{total} = 0
$$

where,

- $F_B​$ is the buoyancy produced by your designed airship

- $m_{total}$ is the total lifting capacity of your designed airship

- $m_{total} = m_{elec} + m_{envelop} + m_{sup} + m_{payload}$ 

  The lifting capacity can be divided into the weight of electronics, balloon envelope(Note: this is not something you can ignore), support materials and payload.

![Here requires one figure]()

**Principle 2**: To satisfy the needs of exploring the space, your design needs to satisfy the basic motion primitives:

- Maintaining forward speed. The blimp should be able to maintain a desired constant forward speed while having zero vertical speed and zero yaw angular speed.
- Changing altitude:  The blimp should be able to ascend or descend to the desired height. 
- Changing orientation: The blimp should be able to spin in place so that its yaw angle can be stabilized at any desired value.

![Here requires one figure]()