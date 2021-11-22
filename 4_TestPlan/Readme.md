# TEST PLAN:

## Table no: High level test plan

| **Test ID** | **Description**                                              | **Exp I/P** | **Exp O/P** | **Actual Out** |**Type Of Test**  |    
|-------------|--------------------------------------------------------------|------------|-------------|----------------|------------------|
|  01      |verify the ATM card insertion slot is as per the specification|  valid ATM card|successfully inserted|presents information of card holder|Requirement based |
|  02       |verify the ATM machines accepts card and PIN details|  PIN number|screen for transaction options|Accepts the PIN and moves forward|Scenario based    |
|  03       |verify the error message by inserting an invalid card(expired card)|  invalid ATM card|invalid alert|Error message|Boundary based    |

## Table no: Low level test plan

| **Test ID** | **Description**                                              | **Exp IN** | **Exp OUT** | **Actual Out** |**Type Of Test**  |    
|-------------|--------------------------------------------------------------|------------|-------------|----------------|------------------|
|  01       |Cash withdraw| PIN number |Valid amout |Entered amout|Boundary based |
|  02       |Deposit amount| Account details |valid amount to deposit|Crediting amount in reqiured Account|Scenario based    |
|  03       |Balance check| PIN number |Account Balance|Account balance|Requirement based    |

