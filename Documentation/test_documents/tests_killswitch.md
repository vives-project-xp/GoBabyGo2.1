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


## test killswitch

test|killswitch state|results|comments
:----------------|:----------------:|:----------------:|:----------------
forward| 0 | 0 | Is disabled
backward| 0 | 0 | Is disabled
left| 0 | 1 | Still works
right| 0 | 1| Still works
| | |
| | |
forward| 1 | 1| Drive forward
backward| 1 | 1 | Drive backwards
left| 1 | 1 | Steer left
right| 1 | 1 | Steer right

## Extra Comments:

No matter what state the kill switch is in the left or right steering still works.
This is no problem as you can't move forward or backward so you can't move at all when the switch isn't active.
