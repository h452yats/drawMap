# drawMap

* pp.py --- main routine
* ppfunc.py --- a function definiton. Change this appropriately.
* pptools.py --- some functions.
* in.json --- sample input file.

# to exec

    % python pp.py in.json
 
 # to examine another map
 
 Edit `ppfunc.py` and change expressions in this file.
 
 * `x[0]`, `x[1]`: state variables
 * `data.dict['params'][0]`, `data.dict['params'][1]`: parameters
 
 ## to examine Henon map
  
    return [ 
        1.0 - data.dict['params'][0] * x[0] * x[0] + x[1], 
        data.dict['params'][1] * x[0] 
    ]
 
 
    
