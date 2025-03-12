# NTU-EE3021-lab1 (LED blinking and RTOS API)

## Members
- R12922A01 王廷郡
- R11944078 林資融


## Lab Requirements (From NTU Cool)
```
====basic problem====

Design a program with two tasks: Task_1 and Task_2. There are two different types of blinking for the LED2, while being controlled by two tasks, respectively. When one of blinking procedure is ongoing, the other should wait for blinking to avoid interference. Namely, you need to use a mutex to protect blinking procedures.

Hint: We need a semaphore and an interrupt service routine for Task_1. Task_2 need using another semphore and a timer for 10s periodically. 

Task_1: Press the button to trigger LED2 blinking (keep blinking in 5s with 1Hz frequency).

Hint: The EXTI interrupt handler detects the button press and then inform Task_1 via a binary semaphore to blink LED.

Task_2: LED2 blinks (keep blinking in 2s with 10Hz frequency) automatically every 10s.

Hint: The timer interrupt handler detects the timeup event and then inform Task_2 via another binary semaphore to blink LED.

=================

 

====option problem_A====

The difference from the basic problem is, you need to identify the long button press event (don't release the button over 1s). When detecting such event, Task_1 executes another blinking procedure (keep blinking in 5s with 10Hz frequency). There are two types of blinking chosen by Task_1 according to long press or normal press, so Task_1 should be informed by distinguishable messages from a queue rather than a binary semaphore.

===================

 

 

====option problem_B==== (optional personal report)

Students can choose content that is relevant to the class of this week, less repetitive with the assignment, and meaningful to conduct experiments on their own, and write a report on the experimental content and results.


```
