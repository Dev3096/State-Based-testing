# Problem Statement 
## State-Based-testing

## GasPump Component
The GasPump component is a state-based component used to control a simple gas pump, 
allowing users to pay for gas by cash or credit card. The component supports the following operations:

Activate (int a): The gas pump is activated, and 'a' represents the price of the gas.

Start(): Start the transaction.

Credit(): Pay for gas by a credit card.

Reject(): The credit card is rejected.

Cancel(): Cancel the transaction.

Approved(): The credit card is approved.

Cash(int c): Pay for gas by cash, where 'c' represents prepaid cash.

StartPump(): Start pumping gas.

PumpGallon(): Dispose one gallon of gas.

Stop(): Stop pumping gas.

Transition Pairing Testing

The transition pairing testing criterion aims to design test cases that cover all identified transition pairs. Below is a set of test cases to satisfy this criterion:

Test Case #1

Actions: Activate(5), Start(), Credit(), Approved(), StartPump(), PumpGallon(), Stop()
Executed Transitions: T1, T2, T3, T6, T10, T8, T11

Test Case #2

Actions: Activate(4), Start(), Cash(5), StartPump(), PumpGallon(), PumpGallon()
Executed Transitions: T1, T2, T5, T10, T8, T9
## Default Transition Testing
The default transition testing criterion aims to design test cases that execute all identified default transitions. Below is a set of test cases to satisfy this criterion:

Test Case #1

Actions: Activate(0), Start(), Reject(), StartPump(), PumpGallon(), Stop()
Executed Default Transition: T4 (Default transition in state S3)
Test Case #2

Actions: Activate(6), Start(), Credit(), Approved(), StartPump(), PumpGallon()
Executed Default Transition: T7 (Default transition in state S6)
Please note that these sample test cases cover various transition pairs and default transitions based on the provided EFSM model for the GasPump component.

More test cases are mentoned in the excel file above. 
