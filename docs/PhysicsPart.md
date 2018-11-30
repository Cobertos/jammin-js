<a name="PhysicsPart"></a>

## PhysicsPart
Part that will add the object to the physics engine.

**Kind**: global class  
**Todo**

- [ ] Objects with multiple layers of Physics object will probably
- [ ] This will not work if added as a child to another object. It

**Properties**

| Name | Type | Description |
| --- | --- | --- |
| linearVelocity | <code>THREE.Vector3</code> | Current linear velocity |
| angularVelocity | <code>THREE.Vector3</code> | Current angular velocity |


* [PhysicsPart](#PhysicsPart)
    * [.dirty([dirtyPos], [dirtyRot], [dirtyVel], [dirtyAngVel])](#PhysicsPart+dirty)
    * [.impulse(force, [pos])](#PhysicsPart+impulse)
    * [.getPhysicsParams()](#PhysicsPart+getPhysicsParams) ⇒ <code>object</code>

<a name="PhysicsPart+dirty"></a>

### physicsPart.dirty([dirtyPos], [dirtyRot], [dirtyVel], [dirtyAngVel])
Dirties this physics object

**Kind**: instance method of [<code>PhysicsPart</code>](#PhysicsPart)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [dirtyPos] | <code>boolean</code> | <code>true</code> | Dirty the position |
| [dirtyRot] | <code>boolean</code> | <code>true</code> | Dirty the rotation |
| [dirtyVel] | <code>boolean</code> | <code>true</code> | Dirty the linear velocity |
| [dirtyAngVel] | <code>boolean</code> | <code>true</code> | Dirty the angular velocity |

<a name="PhysicsPart+impulse"></a>

### physicsPart.impulse(force, [pos])
Adds a force to the object in the next physics frame

**Kind**: instance method of [<code>PhysicsPart</code>](#PhysicsPart)  

| Param | Type | Description |
| --- | --- | --- |
| force | <code>THREE.Vector3</code> | The force to apply, mass dependant |
| [pos] | <code>THREE.Vector3</code> | The position to apply it from in world coordinates. Will use the current position if undefined |

<a name="PhysicsPart+getPhysicsParams"></a>

### physicsPart.getPhysicsParams() ⇒ <code>object</code>
Get the physics parameters from the three.js/SimObject. Takes properties

**Kind**: instance method of [<code>PhysicsPart</code>](#PhysicsPart)  
**Returns**: <code>object</code> - physic parameters object. Can have any SIMPLE js properties