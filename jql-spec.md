### Basic Query

```json
 ["birds", "eq", "Canary"]
```

### In Array
```json
 ["birds", "eq", ["Canary", "Jay", "Robin"]]
```

### This AND That
```json
[
 ["birds", "eq", ["Canary", "Jay", "Robin"]],
 ["dogs", "eq", "Lab"]
]
```

### This OR That
```json
{
 "OR": [
  		["birds", "eq", ["Canary", "Jay", "Robin"]],
  		["dogs", "eq", "Lab"]
	]
}
```

### This AND (That OR TheOther)
```json
[
	["birds", "eq", ["Canary", "Jay", "Robin"]],
 	{
 		"OR": [
  			["birds", "eq", ["Canary", "Jay", "Robin"]],
  			["dogs", "eq", "Lab"]
		]
	}
]
```

### This AND That AND (TheOther OR Bob)
```json
[
	["birds", "eq", ["Canary", "Jay", "Robin"]],
	["dogs", "eq", "Lab"]
 	{
 		"OR": [
  			["birds", "eq", ["Canary", "Jay", "Robin"]],
  			["dogs", "eq", "Lab"]
		]
	}
]
```

### Complex Example
```json
 [
        ["mammals.A", "in", ["A", "B", "C"]],
        ["mammals.B", "in", "false"],
        {
            "OR": [
                ["birds.C", "nin", "true"],
                ["mammals.D", "in", "true"],
                ["mammals.E", "in", "true"],
                {
                    "OR": [
                        ["dogs.F", "in", "true"],
                        ["dogs.G", "in", "true"],
                        [
                            ["cats.H", "in", "true"],
                            ["cats.I", "in", "true"]
                        ]
                    ]
                }
            ]
        },
        ["dogs.J", "in", "true"]
]
```
