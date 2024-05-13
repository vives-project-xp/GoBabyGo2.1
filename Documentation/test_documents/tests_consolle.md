#tests console

tests|M1 pin 1|M1 pin2|M2 pin1|M2 pin2|comments
:-----------|:-------:|:-------:|:-------:|:-------:|:------------------------------------------------------
forward| _ | _ | _ | _ | _ 
backward| _ | _ | _ | _ | _ 
left| _ | _ | _ | _ | _ 
right| _ | _ | _ | _ | _
| | | | | | |
| | | | | | |
joystick forward - controller backwards | 0V | 12.78V | _ | _ | _ |
jostick backwards - controller forward | 12.81V | 0V | _ | _ | _ 
joystick left - controller right | _ | _ | 0V | 8.1V | _ 
joystick right - controller left | _ | _ | 7.95V | 0V | _ 

## expectationsq

tests|M1 pin 1|M1 pin2|M2 pin1|M2 pin2|comments
:-----------|:-------:|:-------:|:-------:|:-------:|:------------------------------------------------------
forward| 0V | 12V | / | / | drive forward
backward| 12V | 0V | / | / | driver backwards
left| / | / | / | / | 12V | 0V | steer to the left
right| / | / | / | / | 0V | 12V | steer to the right 
| | | | | | |
| | | | | | |
joystick forward - controller backwards | 12V | 0V | / | / | driver backwards
jostick backwards - controller forward | 0V | 12V | / | / | driver forward
joystick left - controller right | / | / | 0V | 12V | steer to the right
joystick right - controller left | / | / | 12V | 0V | steer to the left
