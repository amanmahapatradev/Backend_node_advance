set ur base for the part 3 ->

until the current work finishes 

readFileSync ->

Blocking
Start operation -> Main Thread Waits -> Operation completes -> JS Continues

readFile ->

NonBlocking 
Start operation -> Detagate Work -> [1.Main Thread continues , 2.Operation completes] -> 2 -> Callback Runs
