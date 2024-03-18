## test killswitch

test|killswitch state|results|comments
:----------------|:----------------:|:----------------:|:----------------
forward| 0 | _ | _
backward| 0 | _ | _
left| 0 | _ | _
right| 0 | _ | _
| | |
| | |
forward| 1 | _ | _
backward| 1 | _ | _
left| 1 | _ | _
right| 1 | _ | _

## expectations

test|killswitch state|results|comments
:----------------|:----------------:|:----------------:|:----------------
forward| 0 | 0 | do nothing
backward| 0 | 0 | do nothing
left| 0 | 1 | steer to the left
right| 0 | 1 | steer to the right
| | |
| | |
forward| 1 | 1 | driver forward
backward| 1 | 1 | driver backwards
left| 1 | 1 | steer to the left
right| 1 | 1 | steer to the right
