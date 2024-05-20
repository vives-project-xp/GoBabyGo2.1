# engine tests
For testing the working of the diferent electric motors in the car, it is posible to measure the voltage on connectors from the mototrdrivers. in case of the forward and backward motion, this is the motor driver that was included in the original car. This motor drivers controles the 2 motors located in the back of the car.
# picture
Under here, u can see the expected values for each pin on the mototdriver and the actual value that was measured.
### expectations
tests|Motor|comments
:---------------------|:------|:----------------------------------------------
joystick forward | 12V | motors go forward
joystick backwards | -12V | motors go backwards
||
controller forward | 12V | motors go forward
controller backwards | -12V | motors go backwads

### measurements
tests|Motor|comments
:---------------------|:------|:----------------------------------------------
joystick forward | 12.78V | motors go forward
joystick backwards | -12.81V | motors go backwards
||
controller forward | 12.75V | motors go forward
controller backwards | -12.77V | motors go backwads

For the steering motion, we added an extra motordriver becaus this motion was normaly taken care of by using the steeringwheel. We use the L298N motordriver sinds this was already  used in the project 'GoBabyGo 2.1' and this works on 12V wich is provided by the car. By using this motordriver, there is a small voltagedrop on the outputconnector where the motor wil be connected. whan we make use of a relais, it is posible to combine the 2 motordrivers. since we did not receive the relais on time, it was not posible to take measurements of the the steeringmotion with the controller.
# picture
Under here, u can see the expected values for each pin on the mototdriver and the actual value that was measured.
### expectations
tests|Motor|comments
:---------------------|:------|:----------------------------------------------
joystick left | 7.4V | steer left
joystick right | -7.4V | steer right
||
controller left | 12V | steer left
controller right | -12V | steer right
### measurements
tests|Motor|comments
:---------------------|:------|:----------------------------------------------
joystick left | 8.1V | steer left
joystick right | -7.95V  | steer right
||
controller left | / | steer left
controller right | / | steer right

the reson why all the measurements are higher than expected is because of the battery. in theory, the battery should be 12V but when we measured this, it was actual 12.84V.
