*****************************************************************************
* (C) Copyright 2020 Texas Instruments Incorporated. All rights reserved.                                            
*****************************************************************************
** This model is designed as an aid for customers of Texas Instruments.                                             
** TI and its licensors and suppliers make no warranties, either expressed                                           
** or implied, with respect to this model, including the warranties of                                                    
** merchantability or fitness for a particular purpose. The model is                                                      
** provided solely on an "as is" basis. The entire risk as to its quality                                                    
** and performance is with the customer.                                                                                         
*****************************************************************************

The Pspice model provided herewith can be used to simulate behavior of TI GaN in a given electrical environment to understand its operation. This model is not intended to provide estimation of power losses in the device. The model includes integrated gate driver, certain protection features and buck-boost converter for generating +5V and Vneg voltages. Additional information about what is included in this model is provided below for the reference of the user:

1. Rds,on: Fixed ON resistance has been used; RDS,on variation with temperature is not modeled. 
2. Coss: Fixed capacitance is used in the model. Non-linear capacitance varying as a function of voltage is not modeled.
3. Slew rate adjustment: A fixed resistor value (10kohm to 200kohm) has to be externally added between Rdrv pin and GND pin to set the FET’s drain-to-source slew rate during turn-on. The programming of slew rate by connecting Rdrv pin directly to either GND or LDO5V is not enabled in this model and such a configuration may result in convergence errors.
4. Fault protection: Dual Overcurrent protection and UVLO protection (for Vdd, Vneg and LDO5V pins) are integrated in the model. However, overtemperature fault is not included in the model.


 