## tests joystick

tests|M1 pin 1|M1 pin2|M2 pin1|M2 pin2|M3 pin 1|M3 pin2|comments
:-----------|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:------------------------------------------------------
forward|  |  |  |  |  |  |  
backward|  |  |  |  |  |  |  
left| _ | _ | _ | _ | _ | _ | _ 
right| _ | _ | _ | _ | _ | _ | _ 

## expectations

tests|M1 pin 1|M1 pin2|M2 pin1|M2 pin2|M3 pin 1|M3 pin2|comments
:-----------|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:------------------------------------------------------
forward| 12V | 0V | 0V | 12V | / | / | drive forward
backward| 0V | 12V | 12V | 0V | / | / | driver backwards
left| / | / | / | / | 12V | 0V | steer to the left
right| / | / | / | / | 0V | 12V | steer to the right 
