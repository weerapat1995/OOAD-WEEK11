# OOAD-WEEK11
## State Diagram


### Code
```
state "Card Slots" as cardslots
state "Enter Amount" as enteramount
state "Money Slots" as moneyslots
[*] -r-> cardslots : wait insert the card
cardslots -r-> Keypad : Keypad successfully
Keypad --> enteramount : Select amount money
enteramount -l-> moneyslots : accept money
moneyslots -l-> [*] : accept card
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/s1.png)

### Code
```
[*] -r-> Idle 
Idle : Monitor
Idle -r-> Alert : Call detected
Alert -l-> Idle : Call cleared
Alert : Start ringing\nStop ringing
Alert -u-> Calling : Answer the phone
Calling --> Idle : Call cleared
Calling : Stop ringing 
Calling -u-> Locking : 20 second
Locking : Stop ringing
Locking --> Idle : Call cleared
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/s2.png)

### Code
```
[*]-r->Off
Off : Shut down Cumputer 
Off-r->On :Switch turn on
On : Turn on Cumputer
On-d->Boot : Switch on complete
Boot : Loading System
Boot-l->Ready :Boot complete
Ready : wait command
Ready-u->Off : Switch turn off
Off-u->[*]
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/s3.png)

### Code
```
[*]-r-> Idle
Idle : Wait Setup
Idle -r-> Setup :Setup Complete
Setup : Setup Time
Setup --> Off :Setup Complete
Off : Turn Off Alarm
Off--> Setup :Restart Setup 
Off -l-> On : Mode On
On : Turn On Alarm
On -l-> Alert : Matching Time
Alert :Start Alert
Alert --> Off : Mode Off
Off -r-> [*]
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/s4.png)

### Code
```
[*]-r-> Off
Off-r->On : turn on
On-r->Number1 : turn on complete
Number1-d->Operand : Key number complete
Operand-d->Number2 : Key operand complete
Number2-d->Data : Key number complete and operate number complete
Data --> Off : turn off
Off --> [*]
Number1-->Reset : Reset data
Operand-->Reset : Reset data
Number2-->Reset : Reset data
Reset-->Number1 
Number1-->Off : turn off
Operand-->Off : turn off
Number2-->Off : turn off
Off : Turn off Calculator
On : Turn on Calculator
Number1 : Key Number
Number2 : Key Number
Operand : Key Operand
Reset : Reset data
Data : result data
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/s5.png)

## Activity Diagram

### Code
```
(*) --> Login
if "" then
-r-> Member
else
--> Register
--> Member
Member -r-> Website 
Website --> Logout
Logout --> (*)
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/a1.png)

### Code
```
(*) --> "Request Menu"
"Request Menu" -r-> "Choose Food"
if "" then
--> [Confirm = Yes] "Call Employee"
--> "Order Food"
--> (*)
else
----> [Comfirm = No] "Choose Food" 
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/a2.png)

```
(*) --> "Receive Order"
"Receive Order"-r-> "Check Order"
if "" then
--> [Quality = No] "Receive Order"
else
--> [Quality = Yes] "Keep Order"
--> (*)
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/a3.png)

### Code
```
(*) --> Search Booking
if "" then
---> [ID Booking Match = None] Search Booking
else
--> [ID Booking Match = have ] Show Data Booking
--> (*)
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/a4.png)

### Code
```
(*) --> Order
if "" then
---> [Book = No] Order
else
-->[Book = Yes] Price
-->Receive Money
-->(*)
```
### Diagram

![](https://github.com/weerapat1995/OOAD-WEEK11/blob/master/HOMEWORK/a5.png)
