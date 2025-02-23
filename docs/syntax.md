# Language Syntax Specification

## 1. Operators

### 1.1 End of Line Operator
- **Symbol:** `~`
- **Description:** Marks the end of a statement.
- **Example:**
  ```
  L int-chan: num :> 10~
  kyaa! num~
  ```

### 1.2 Code Block Operators
- **Symbols:** `<` (Start), `>` (End)
- **Description:** Defines the start and end of code blocks.
- **Example:**
  ```
  nani? ^^bool condition^^ <
      kyaa! "Condition met"~
  >
  ```

### 1.3 Subscript Operator
- **Symbol:** `{}`
- **Description:** Used for array and buffer sizes.
- **Example:**
  ```
  ch{20} name~
  ```

### 1.4 Assignment Operator
- **Symbol:** `:>`
- **Description:** Assigns values to variables.
- **Example:**
  ```
  L int-chan: value :> 42~
  ```

### 1.5 Argument Brackets
- **Symbol:** `^^args^^`
- **Description:** Defines function parameters.
- **Example:**
  ```
  F: greet ^^ch{20} name^^ <
      kyaa! name~
  >
  ```

### 1.6 Arithmetic Operators
- **Addition:** `(+)`
- **Subtraction:** `(-)`
- **Multiplication:** `(*)`
- **Division:** `(/)`

### 1.7 Logical Operators
- **AND:** `(&&)` or `(AND)`
- **OR:** `(||)` or `(OR)`

---

## 2. Control Flow

### 2.1 Conditional Statements

#### If Statement
- **Syntax:** `:D`
- **Example:**
  ```
  :D ^^ int-chan i.greater^^ 21 ^^ ^^ <
      kyaa! "Is greater"~
  >
  ```

#### Else If Statement
- **Syntax:** `o.O`
- **Example:**
  ```
  o.O ^^ int-chan i.less^^ 21 ^^ ^^ <
      kyaa! "Is Less"~
  >
  ```

#### Else Statement
- **Syntax:** `D:`
- **Example:**
  ```
  D: <
      kyaa! "Error"~
  >
  ```

### 2.2 Looping Constructs

#### For Loop
- **Syntax:** `nande?`
- **Example:**
  ```
  nande? ^^int-chan i :> 0; i.less 10; i :> i (+) 1^^ <
      kyaa! i~
  >
  ```

#### For-Each Loop
- **Syntax:** `nandesuka?`
- **Example:**
  ```
  nandesuka? ^^ch item in list^^ <
      kyaa! item~
  >
  ```

#### While Loop
- **Syntax:** `nani?`
- **Example:**
  ```
  nani? ^^bool condition^^ <
      kyaa! "Looping..."~
  >
  ```

#### Do-While Loop
- **Syntax:** `nani-nani?`
- **Example:**
  ```
  nani-nani? <
      kyaa! "Executed at least once"~
  > ^^bool condition^^
  ```

### 2.3 Loop Control
- **Continue:** `ganbatte!`
- **Break:** `yamete!`
- **Return:** `yatta!`

---

## 3. Data Types

| Type | Keyword |
|-------|----------|
| Integer | `int` |
| Short Integer | `int-chan` |
| Long Integer | `int-san` |
| Floating Point | `floaty` |
| Boolean | `bool` |
| Character | `ch` |
| String | _TBA_ |

### 3.1 Boolean Values
- **True:** `hai`
- **False:** `iie`

---

## 4. Variable Declaration

### 4.1 Non-Mutable Variable
- **Syntax:** `L`
- **Example:**
  ```
  L int-chan: papaj :> 2137~
  ```

### 4.2 Mutable Variable
- **Syntax:** `V`
- **Example:**
  ```
  V int-chan: papaj :> 2137~
  ```

---

## 5. Object-Oriented Features

### 5.1 Class Declaration
- **Syntax:** `C:`
- **Example:**
  ```
  C: Papaj <
      int value~
      ch{20} name~
  >
  ```

---

## 6. Functions

### 6.1 Function Declaration
- **Syntax:** `F:`
- **Example:**
  ```
  F: dup2137a ^^int-chan age, ch{20} name^^ <
      yatta! age, name~
  >
  ```

---

## 7. Input/Output

### 7.1 Print Statement
- **Syntax:** `kyaa!`
- **Example:**
  ```
  kyaa! "Hello, world!"~
  ```

---

## 8. Error Handling

### 8.1 Try-Catch Mechanism

#### Try Block
- **Syntax:** `ara!`
- **Example:**
  ```
  ara! <
      kyaa! "Trying something risky"~
  >
  ```

#### Except Block
- **Syntax:** `baka!`
- **Example:**
  ```
  baka! <
      kyaa! "An error occurred!"~
  >
  ```

