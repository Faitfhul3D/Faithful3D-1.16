# How to make entity models ?

- Install Optifine, (just in case)
- Choose an entity from this list : https://github.com/sp614x/optifine/blob/master/OptiFineDoc/doc/cem_model.txt \n(those that are not in it will not be editable)
- Make a 'entity_name.jpem' like this one :

```json
{
  "texture": "skeleton",			  # default texture (used for parts not mentioned below)
  "credit": "Made with Blockbench by Juknum",     # just what you want (can be unused)
  "textureSize": [48,32],			  # size of the default texture [width,height]
  "shadowSize": 0.75,                             # shadow of the entity
  "models":                                       
  [						  # models made with BlockBench
    {
      "model": "skeleton_head.jpm",
      "part": "head",                             # you need to specifie this part in accordance with the list of the entity
	  "attach": true,                         # if false : replace the default model
      "translate": [ 8, 0, -8],
      "rotate": [0, 0, 0]
    },
    {
      "model": "skeleton_body.jpm",
      "part": "body", 
      "attach": true,
      "translate": [ 8, 12, -8],
      "rotate": [0, 0, 0]
    }
  ]
}
```

Then create `skeleton_head.jpm` and `skeleton_body.jpm` with BlockBench, at the end it looks like this :
```json
{
	"texture": "skeleton_head",
	"textureSize": [128, 64],
	"credit": "Made with Blockbench by Juknum",
	"boxes": [
		{
			"coordinates": [-12, -1, 4, 8, 1, 1],
			"uvNorth": [20, 34, 36, 36],
			"uvEast": [0, 0, 0, 0],
			"uvSouth": [20, 34, 36, 36],
			"uvWest": [0, 0, 0, 0],
			"uvUp": [20, 34, 36, 36],
			"uvDown": [38, 16, 54, 18]
		},
		{
			"coordinates": [-5, -2, 4, 1, 1, 1],
			"uvNorth": [34, 32, 36, 34],
			"uvEast": [0, 0, 0, 0],
			"uvSouth": [34, 32, 36, 34],
			"uvWest": [0, 0, 0, 0],
			"uvUp": [0, 0, 0, 0],
			"uvDown": [0, 0, 0, 0]
		}
	]
}
```
