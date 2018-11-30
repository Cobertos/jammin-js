<a name="SimObjectLoader"></a>

## SimObjectLoader
Loads an obj/mtl object asynchronously along with it's partner

**Kind**: global class  

* [SimObjectLoader](#SimObjectLoader)
    * [.load(uri)](#SimObjectLoader+load) ⇒ <code>THREE.Object3D</code>
    * [.process(rootObj)](#SimObjectLoader+process)

<a name="SimObjectLoader+load"></a>

### simObjectLoader.load(uri) ⇒ <code>THREE.Object3D</code>
Actually loads and parses the .mtl and .obj files

**Kind**: instance method of [<code>SimObjectLoader</code>](#SimObjectLoader)  
**Returns**: <code>THREE.Object3D</code> - A THREE.Object3D with SimObjects

| Param | Type | Description |
| --- | --- | --- |
| uri | <code>string</code> | The url or path to load from |

<a name="SimObjectLoader+process"></a>

### simObjectLoader.process(rootObj)
Takes a loaded THREE.js object with special names that determine extra

**Kind**: instance method of [<code>SimObjectLoader</code>](#SimObjectLoader)  

| Param | Type | Description |
| --- | --- | --- |
| rootObj | <code>THREE.Object3D</code> | The root object to traverse and modify. |
