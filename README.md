<img src="https://user-images.githubusercontent.com/52724526/81895103-6d7dc180-95ec-11ea-8760-c08df1757440.png" width=300px>
 
# drawMap --- draw a chaotic attractor dynamically

Chaotic attractor of a difference equation is visualized. 

## Files

* pp.py: main routine
* pptools.py: some functions.
* in.json: sample input file. A JSON format. Describe parameters and a
definition of the ODE. 

## Requirements

* python 3.6 or later
    * numpy
    * matplotlib

## How to use
### to exec

    % python pp.py in.json

### mouse operation 

- A new initial values can be  given by clicking on the appropriate location
in the graph.
 
### key operation

- `s`: print the current status
- `w`: print the dictionary and dump it to `__ppout__.json` and publish
  a screenshot PDF file as `snapshot.pdf`.
- `p`: change the active parameter (default: 0, toggle)
- up and down arrows: increase/decrease the active parameter value
- `space`: clear transitions
- `q`: quit 
 
### to examine another map
 
 Open the setup file and change expressions on the ODE in this file.
 
 * `x[0]`, `x[1]`: state variables
 * `data.dict['params'][0]`, `data.dict['params'][1]`: parameters
 
### Example: Henon map
Replace the return sentence by the following codes:

    "func": [ 
        "1.0 - data.dict['params'][0] * x[0] * x[0] + x[1]", 
        "data.dict['params'][1] * x[0]"
    ]
 
CAUTONS: If this definition is not located in the end of the setup file,
you should add a comma right after a close bracket.

