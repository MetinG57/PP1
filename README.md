# PP1

## Goal
All PPn practical exercises share a common purpose: to help you demonstrate—step by step—that you followed and understood the content presented in the weekly lectures. This ongoing feedback loop allows me, as your lecturer, to monitor your personal progress.

In this first exercise, your goal is to demonstrate an understanding of digital computation: specifically, how to map elements of an input set to an output set. We'll begin with simple mappings and gradually increase the difficulty.

**Important:** Start a stopwatch when you begin and work uninterruptedly for 90 minutes. Once time is up, stop immediately and document the point where you had to pause.

---

## Workflow
Each exercise will follow the same basic workflow:

1. **Fork** the repository
2. **Modify and Commit** your solution
3. **Submit your link for Review**

### Step 1: Fork the Repository
A fork is a personal copy of this repository under your own GitHub account. You can edit and manage it freely. Even if you make mistakes, you can always restart or revisit your progress.

To fork this repository:

1. Create a GitHub account (you may use your university email).
2. Open this project in your browser.
3. Click the `Fork` button in the top-right corner:

   ![Fork-Button](./assets/fork.png)

---

4. Scroll down in the dialog and click `Create fork`:

   ![Create fork-Button](./assets/create_fork.png)

---

### Step 2: Modify and Commit
A **commit** is a saved snapshot of your work.

1. Navigate to the `README.md` file.
2. Click the pencil icon to edit the file:

   ![Pencil-Button](./assets/pencil.png)

---

3. Use the built-in editor to make changes.
4. Click `Commit changes` when done:

   ![Commit-Button](./assets/commit_button.png)

---

Add a meaningful comment about what you did and how long it took.

### Step 3: Submit for Review
If you get stuck, visit the discussions forum:
[https://github.com/MaxClerkwell/PP1/discussions](https://github.com/MaxClerkwell/PP1/discussions)

When you have finished working, in Moodle, click "Add solution" and submit the link to your repository.

---

## Tasks

### Task 1: Mapping Symbols to Binary
Fill out the following table, mapping decimal numbers `0` through `15` to their binary representations:

| Decimal | Binary Representation |
|---------|------------------------|
| 0       | 0000                   |
| 1       | 0001                   |
| 2       | 0010                   |
| 3       | 0011                   |
| 4       | 0100                   |
| 5       | 0101                   |
| 6       | 0110                   |
| 7       | 0111                   |
| 8       | 1000                   |
| 9       | 1001                   |
| 10      | 1010                   |
| 11      | 1011                   |
| 12      | 1100                   |
| 13      | 1101                   |
| 14      | 1110                   |
| 15      | 1111                   |


**How many binary digits (bits) are needed?**
Explain how to calculate the number of bits required: 4 bits werden benötigt, da 2^n=16 wobei n=4 ;  16 da die Anzahl werte 16 sind (0 bis 15)
->Um herauszufinden, wie viele Bits man braucht, schaut man, wie viele verschiedene Werte man darstellen will. Dann nimmt man die kleinste Zweierpotenz (also 2 hoch irgendwas), die mindestens so groß ist wie diese Anzahl. Der Exponent zeigt dann, wie viele Bits man braucht.

Es gibt mehrere Möglichkeiten (hier Divisionsrestverfahren) 
<details>
<summary>  Beispiel: 13:2=6 Rest 1
                     6:2=3  Rest 0
                     3:2=1  Rest 1
                     1:2=0  Rest 1     //   Jetzt liest man die Reste von unten nach oben: 
         13(10) = 1101(2) </summary>
Erase this text and write your answer here!
</details>

---

### Task 2: Mapping Binary to Binary
Digital processors implement **logical functions** using **logic gates** like NAND, AND, OR, etc.
These functions map binary input sets (voltages) to binary outputs.

Refer to the truth table of a 1-bit full adder:

| C<sub>in</sub> | B | A | Sum (S) | C<sub>out</sub> |
|--------------|---|---|---------|-----------------|
| 0            | 0 | 0 | 0       | 0               |
| 0            | 0 | 1 | 1       | 0               |
| 0            | 1 | 0 | 1       | 0               |
| 0            | 1 | 1 | 0       | 1               |
| 1            | 0 | 0 | 1       | 0               |
| 1            | 0 | 1 | 0       | 1               |
| 1            | 1 | 0 | 0       | 1               |
| 1            | 1 | 1 | 1       | 1               |

> Simulate this adder using NAND gates:
[Full Adder NAND CircuitVerse Project](https://circuitverse.org/users/305021/projects/full-adder-nand-990621f6-993b-4676-a1b5-2a31aae451ce)

#### Your Task
Create a truth table for a **2-bit adder** without carry-in. What are the possible inputs and outputs?

| B1 | B0 | A1 | A0 | Q2 | Q1 | Q0 | 
|----|----|----|----|----|----|----|
| 0  | 0  | 0  | 0  |  0 |  0 |  0 |
| 0  | 0  | 0  | 1  |  0 |  0 |  1 |
| 0  | 0  | 1  | 0  |  0 |  1 |  0 |
| 0  | 0  | 1  | 1  |  0 |  1 |  1 |
| 0  | 1  | 0  | 0  |  0 |  0 |  1 |
| 0  | 1  | 0  | 1  |  0 |  1 |  0 |
| 0  | 1  | 1  | 0  |  0 |  1 |  1 |
| 0  | 1  | 1  | 1  |  1 |  0 |  0 |
| 1  | 0  | 0  | 0  |  0 |  1 |  0 |
| 1  | 0  | 0  | 1  |  0 |  1 |  1 |
| 1  | 0  | 1  | 0  |  1 |  0 |  0 |
| 1  | 0  | 1  | 1  |  1 |  0 |  1 |
| 1  | 1  | 0  | 0  |  0 |  1 |  1 |
| 1  | 1  | 0  | 1  |  1 |  0 |  0 |
| 1  | 1  | 1  | 0  |  1 |  0 |  1 |
| 1  | 1  | 1  | 1  |  1 |  1 |  0 |

Eingaänge: 16 Kombinationen
Ausgänge : 7 Kombinationen (Q2 - Q0)



### Task 3: Boolean Equations via Karnaugh Maps
Use the [K-Map method](https://github.com/STEMgraph/4b957490-badf-4264-b9f2-1b5aa370f36e) to derive Boolean equations for each output bit in your 2-bit adder.

1. Fill out Karnaugh Maps -> Ich konnte die Aufgabe leider nicht lösen, da unklar ist, ob die Übung im Link oder die im Task gemeint ist – beide behandeln unterschiedliche Themen. Zudem konnte ich nach dem Klick auf „commit changes“ nichts mehr bearbeiten, da der Stift deaktiviert wurde.
2. Write down an equation for each cell marked `1`
3. Combine them using OR gates
4. Minimize the equations

Q0

| B  | A  |    |    |    |
|----|----|----|----|----|
|    | 00 | 01 | 11 |  10|
| 00 | 0  | 1  | 1  |  0 |
| 01 | 1  | 0  | 0  |  1 |
| 11 | 1  | 0  | 0  |  1 |
| 10 | 0  | 1  | 1  |  0 |


Q1

| B  | A  |    |    |    |
|----|----|----|----|----|
|    | 00 | 01 | 11 |  10|
| 00 | 0  | 0  | 1  |  1 |
| 01 | 0  | 1  | 0  |  1 |
| 11 | 1  | 0  | 1  |  0 |
| 10 | 1  | 1  | 0  |  0 |


Q2

| B  | A  |    |    |    |
|----|----|----|----|----|
|    | 00 | 01 | 11 |  10|
| 00 | 0  | 0  | 0  |  0 |
| 01 | 0  | 0  | 1  |  0 |
| 11 | 0  | 1  | 1  |  1 |
| 10 | 0  | 0  | 1  |  1 |



<details>
<summary>The final functions</summary>

Q<sub>0</sub> = A0 v B0

Q<sub>1</sub> = (A1 v B1) v (A0 + B0)

C<sub>out</sub> = Um ehrlich zu sein habe ich die 90 Minuten hier schon überschritten gehabt, habe die Aufgabe aber noch zu Ende gemacht. 
</details>

---

### Task 4: Circuit Implementation
Using your Boolean equations, build a logic network in [CircuitVerse](https://circuitverse.org) that implements at least one bit of the adder.

<details>
<summary>Your solution</summary>
A share link to your solution goes here: <a href=".................">Link!</a>
</details>

---

**Remember:** Stop working after 90 minutes and record where you stopped!

