<a name="SimObjectInheritor"></a>

## SimObjectInheritor ⇐ <code>THREE.Object3D</code>
The actual class created by `SimObject()`, inherits from

**Kind**: global class  
**Extends**: <code>THREE.Object3D</code>  

* [SimObjectInheritor](#SimObjectInheritor) ⇐ <code>THREE.Object3D</code>
    * [new SimObjectInheritor(...Vararg)](#new_SimObjectInheritor_new)
    * _instance_
        * [.scene](#SimObjectInheritor+scene)
        * [.finishConstruction()](#SimObjectInheritor+finishConstruction)
        * [._partApply(func, args)](#SimObjectInheritor+_partApply)
        * [.add()](#SimObjectInheritor+add) ⇒ <code>undefined</code>
        * [.remove()](#SimObjectInheritor+remove) ⇒ <code>undefined</code>
    * _static_
        * [.finishDefinition()](#SimObjectInheritor.finishDefinition)
        * [._partApplyStatic(func, args)](#SimObjectInheritor._partApplyStatic)

<a name="new_SimObjectInheritor_new"></a>

### new SimObjectInheritor(...Vararg)

| Param | Type | Description |
| --- | --- | --- |
| ...Vararg | <code>any</code> | of args to pass to THREE.js constructor |

<a name="SimObjectInheritor+scene"></a>

### simObjectInheritor.scene
**Kind**: instance property of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| Root | [<code>SimScene</code>](#SimScene) | scene this object is attached to, if any |

<a name="SimObjectInheritor+finishConstruction"></a>

### simObjectInheritor.finishConstruction()
You **MUST** call this after construction finishes to properly setup

**Kind**: instance method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  
**Todo**

- [ ] Add an assert if this isn't called
- [ ] Is the `setTimeout` above enough?
- [ ] Remove duplication of `_partClss` functionality

<a name="SimObjectInheritor+_partApply"></a>

### simObjectInheritor.\_partApply(func, args)
For every mixed in part, calls `part[func].apply(this, args)` allowing

**Kind**: instance method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  

| Param | Type | Description |
| --- | --- | --- |
| func | <code>string</code> | Function name to call |
| args | <code>Array.&lt;any&gt;</code> | Arguments to call with |

<a name="SimObjectInheritor+add"></a>

### simObjectInheritor.add() ⇒ <code>undefined</code>
**Kind**: instance method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  
**Returns**: <code>undefined</code> - Nothing  

| Param | Type | Description |
| --- | --- | --- |
| ...objs | <code>THREE.Object3D</code> \| [<code>SimObject</code>](#SimObject) | Objects to add |

<a name="SimObjectInheritor+remove"></a>

### simObjectInheritor.remove() ⇒ <code>undefined</code>
**Kind**: instance method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  
**Returns**: <code>undefined</code> - Nothing  
**Todo**

- [ ] You might have issues removing things added in add()


| Param | Type | Description |
| --- | --- | --- |
| ...objs | <code>THREE.Object3D</code> \| [<code>SimObject</code>](#SimObject) | Objects |

<a name="SimObjectInheritor.finishDefinition"></a>

### SimObjectInheritor.finishDefinition()
You **MUST** call this after the class is defined if one of your

**Kind**: static method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  
**Todo**

- [ ] Enforce this with an assert

<a name="SimObjectInheritor._partApplyStatic"></a>

### SimObjectInheritor.\_partApplyStatic(func, args)
For every mixed in part class, calls `partCls[func].apply(this, args)`

**Kind**: static method of [<code>SimObjectInheritor</code>](#SimObjectInheritor)  

| Param | Type | Description |
| --- | --- | --- |
| func | <code>string</code> | Function name to call |
| args | <code>Array.&lt;any&gt;</code> | Arguments to call with |
