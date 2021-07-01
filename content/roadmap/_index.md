---
title: "Roadmap"
featured_image: "/images/roadmap.svg"
---
## 1. A file format for genetic engineering

Genestorian will store the genetic engineering steps followed to generate new entities from existing ones. The problem is that, as of now, no open file format exists to store this information. Developing a file format to record genetic engineering steps will set the foundations of Genestorian, but will also allow you to share your cloning strategy with others in an unambiguous way, that can also be read by computers.

The plan is to use `.json` format, and to store the biological entities and the cloning steps in two different lists. Think about it like a family tree file, where you would store objects representing people in one list, and objects representing their relations in another list.
<details>
  <summary>Familiar with .json? Click here to see how the final format may look!</summary>

```
{
    "entities": [
        {
            "type": "Circular",
            "id": "pFA6a",
            "source": {...}
        },
        {...}
    ],
    "steps": [
        {
        "inputs": [{...},{...}],
        "output": {...},
        "method": {...},
        "proofs": [{...},{...}]
        },
        {...}
    ]
}
```
</details>

## 2. A web application to visualize and generate these files

That file format sounds interesting... But who wants to type all that? The next step is to build a web interface where you can generate this documentation in the browser.


None of the above software pieces, which are all essential for open reproducible science, exists as Open Source, and proprietary solutions do not cover the use-case of model organism research.
