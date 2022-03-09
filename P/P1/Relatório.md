# Lab 1: Process Modulation

### *Grupo 601*

# Exercise 1.1

At first glace, it appears to describes the process of placing and confirming a shipping order, and it follows the following flow:

1. The first action that takes place is the "Receive Order"
2. After the order is received, it can be accepted or not
    -  If accepted
        -   The order is filled.
        - By filling the order, two processes will take place simultaneously (represented by the fork node)
        - It will be given a shipping order
        - An invoice will be issued, and this object will be processed, and will result in it being accepted
        - Once the shipping order and the payment flow are complete, they will be joined and proceed the flow
    - If rejected
        - Nothing happens
3. Both flows, acceptance or rejection, will eventually merge.
4. After the, merge has take place, the order will be closed.
5. Once the order is close, the activity is ended.


# Exercise 1.2

![ex1_2-diagram](1_2.png)

# Exercise 1.3

## a)
![ex1_3-diagram](1_3.png)

## b)

There are three main point in witch the activity flow can be improved, these are:

1. Cut the "middle man" the accreditation of the doctor, by enabling the doctor's information to be directly sent to the order.
2. Since the ARS need to request information necessary, to validate a Clinics candidate status, to the ERS, these process of validation could be directly tasked to the ERS itself, with no need of a "middle man".
3. The final improvement it to discard the paper methods and replace them by digital ones. It is time consuming to send the declarations in physical format, when it could be digitally signed and send by email.

Bellow there is a modulation of the improved activity flow.

![ex1_3-improved-diagram](1_3_improved.png)

## c)

|Total times per type of operation  | Current Model | Improved Model
|:-:|:-:|:-:|
|Information search|                |                   |