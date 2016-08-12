
```
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
