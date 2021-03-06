# Input and Output
เรื่องแรกที่เราจะเรียนเป็นสี่งแรกในการเรียนการเขียนโปรแกรม นั่นก็คือเรื่องการ Input และ Output ของโปรแกรม<br>
Input และ Output เป็นเรื่องสำคัญต่อการทำโปรแกรม เพราะหากว่าเราไม่มี input หรือ output เราก็จะไม่รู้ว่าจะให้โปรแกรมทำอะไร แล้วได้ผลลัพท์อะไร<br>
ดังนั้น ทุกโปรแกรมจึงควรมีทั้ง Input และ Output เสมอ

## การรับ Input
Input หมายถึงสิ่งที่ได้รัับเข้ามา ในที่นี้คือโปรแกรมนั้นจะรับค่าอะไรมาซักอย่าง เพื่อที่จะให้นำไปใช้ในโปรแกรมของจริง<br>
โดยในภาษา Python นั้นจะใช้ฟังก์ชัน `input()` เพื่อทำการรับ input เข้ามาสู่ระบบ

::: warning
การรับ input() นั้น ข้อมูล (input) ทุกอย่างจะถูกเปลี่ยนไปเป็นประเภท string ทั้งหมด

ถ้าหากต้องการเปลี่ยนประเภทของ input เป็นอย่างต่างๆ (เช่น float, boolean, integer) ก็จำเป็นที่จะต้องทำการ data type casting โดยจะสอนวิธีการเปลี่ยนประเภทตัวแปรในขั้นตอนต่อๆไป
:::

ตัวอย่างการรับ input ในภาษา Python
```python
input()
```

แต่รับมาแล้ว ใครจะจำค่าที่ได้รับ input มาหล่ะ<br>
ดังนั้นจึงต้องมีตัวแปร (variable) เพื่อมาจัดเก็บข้อมูลนั้น

ตัวอย่างเช่น
```python
kumamon = input()
```

โดยในโค้ดด้านบนนั้น ตัวแปร `kumamon` ก็จะมีค่าที่ได้รับมาเป็น input อยู่

::: warning
การรับ input นั้น จะรับค่าตั้งแต่ตัวอักษรแรก จนสุดบรรทัด

นั่นหมายความว่า หากมีการให้ input มาหลายบรรทัด ก็จะรับ input มาเพียงบรรทัดแรกเท่านั้น
:::

## การส่ง output
Output นั้นหมายถึงการเอาอะไรออกไป<br>
โดยปกติแล้ว การส่ง output นั้น ก็จะมี 2 ประเภทหลักๆ นั่นคือ
1. แสดง output ออกบนหน้าจอ
2. โยน output ไปยังฟังกชันอื่น (เป็นการ return หรือเรียกฟังกชันอื่น)

::: tip
ใน lecture นี้จะสอนเพียงการแสดง output ออกบนหน้าจอเท่านั้น<br>
หากว่าต้องการศึกษา output ประเภทโยนให้ฟังก์ชันอื่นๆ สามารถเข้าไปดูได้ที่ lecture ถัดไป (เรื่อง Functions)
:::

### วิธีแสดง output
สามารถใช้ฟังก์ชัน `print()` เพื่อให้แสดงผลลัพท์บนหน้าจอผลลัพท์

ตัวอย่างเช่น
```python
print("Hello, my name is Kumamon")
```

หากเอาโปรแกรมไปรันแล้ว น้องๆก็จะเห็น string ที่เขียนว่า "Hello, my name is Kumamon" บนหน้าจอ console ของ Python

การแสดง output นั้น ไม่จำเป็นที่จะต้องเป็น string (แบบตัวอย่างด้านบน) เสมอไป<br>
น้องสามารถให้โปรแกรมแสดงผลลัพท์ (ค่า) ที่อยู่ภายในตัวแปรก็ได้

ตัวอย่างเช่น
```python
player1 = "Kumamon"
print(player1)
```

ในโค้ดด้านบนนั้น บ่งบอกถึงการเก็บ string ที่เขียนว่า "Kumamon" ลงบนตัวแปร `player1` และก็ได้ทำการ `print()` ตัวแปรนั้นออกมาเพื่อแสดงบนหน้าจอ

::: warning Checkpoint
ให้ลองฝึกการเขียนโปรแกรม โดยการให้รับ input เข้ามา แล้วแสดง output เลยทันที

ลองทำดูก่อนนะครับ อย่าเพิ่งดูคำตอบ อิอิ

**เฉลย**<br>
```python
var1 = input()
print(var1)
```
:::

## Data Type
Data Type หมายความว่า ประเภทของข้อมูลที่จัดเก็บ ซึ่ง Python นั้นก็จะทำการจัดเก็บให้น้องเอง (แหงหล่ะ) แต่น้องก็จำเป็นที่จะต้องรู้ ว่าจะทำอะไรกับมันดี หรือทำอะไรกับมันได้

ประเภทของค่าตัวแปรนั้น มี**หลักๆ** อยู่ 4 ประเภท นั่นคือ
| Data Type 	| Data ที่จะจัดเก็บจริง 	| ตัวอย่าง data       	|
|-----------	|------------------	|-------------------	|
| String    	| ตัวอักษร           	| "kumamon" "1112"  	|
| Boolean   	| ค่าจริงหรือเท็จ      	| True False        	|
| Float     	| ค่าที่มีจุดทศนิยม      	| 1.00 1.112 -0.999 	|
| Integer   	| จำนวนเต็ม         	| 1 0 -555          	|

และยังมีประเภทอื่นๆ อีกมากมาย<br>
ไปอ่านเอาเองเนอะ [https://docs.python.org/3.7/library/datatypes.html](https://docs.python.org/3.7/library/datatypes.html)

### Check ประเภทของตัวแปร
บางครั้งเราอาจจะลืมประเภทของตัวแปรได้ (เนื่องจากเรื่องสมงสมองมันก็จะไหม้ๆหน่อย เลยลืม) ก็สามารถเช็คได้โดยการใช้ฟังก์ชัน `type()`

ตัวอย่างการใช้งาน
```python
type(var1)
```

ตัวอย่างเช่น
```python
var = "Hello"
type(var) # Returns <class 'str'>

var = "1234"
type(var) # Returns <class 'str'>

var = 1234
type(var) # Returns <class 'int'>

var = 1234.56
type(var) # Returns <class 'float'>

var = True
type(var) # Returns <class 'bool'>
```

ในการทดลองที่ 2 และ 3 จะเห็นได้ว่า "1234" และ 1234 นั้นมีประเภทข้อมูลไม่เหมือนกัน<br>
จะสังเกตุได้ว่า พี่มงได้ใส่ "" เข้าไปด้วย แสดงถึงว่า พี่ให้มันเป็นตัวอักษรทั่วๆไป ไม่ใช่ตัวเลขที่สามารถเอาไปคำนวณได้

## Data Type Casting
จากในเรื่องเกี่ยวกับการรับ input มานั้น พี่มงได้บอกไว้ว่า

"input() จะรับมาเป็นประเภท string ทั้งหมดเลย"

เนื่องจากว่าหากว่าจะเป็นประเภทอื่น ที่ไม่ใช่ string ตัว Data Type ที่เป็น string ก็เก็บได้หมดเลย

เช่น
```python
var = input() # แล้วพี่มงก็ใส่ค่า "Hello World" เข้ามา
print(var) # ผลลัพทืก็จะออกมาเป็น "Hello World"

var = input() # แล้วพี่มงก็ใส่ค่า 1112 เข้ามา
print(var) # ผลลัพทืก็จะออกมาเป็น "1112"

var = input() # แล้วพี่มงก็ใส่ค่า True เข้ามา
print(var) # ผลลัพทืก็จะออกมาเป็น "True"

var = input() # แล้วพี่มงก็ใส่ค่า 11.12 เข้ามา
print(var) # ผลลัพทืก็จะออกมาเป็น "11.12"
```

แล้วพี่คะ หนูอยากใช้ integer อ่ะ เพราะอยากให้เอาค่าตัวแปร var1 มาคูณกับ var2
```python
var1 = input()
var2 = input()
var3 = var1 * var2
print(var3)
```

แล้วทำไมมัน error คะ

พี่มงจะบอกว่า เนื่องจาก input() ที่รับมา ยังเป็นประเภท string อยู่ ไม่ใช่ตัวเลข การเอามาคูณกันจึงเป็นไปไม่ได้ ทำให้เกิด error

### วิธีการแปลง
ภายใน python นั้นก็จะมีการแปลงเป็น data type อื่นๆ ดังนี้
| Data Type 	| วิธีการแปลง 	|
|-----------	|-----------	|
| String    	| string()  	|
| Boolean   	| bool()      |
| Float     	| float()   	|
| Integer   	| int()     	|

**โดย Python จะพยายามเก็บข้อมูลและแปลงประเภทข้อมูลให้อัตโนมัติ หากมีความจำเป็น**

ตัวอย่างเช่น (การแปลง string ไปเป็น integer)
```python
var = "1112"
var = int(var)
print(var) # ก็จะได้ผลลัพท์เป็น 1112
```

ตัวอย่างที่ 2 (การเปลี่ยน float ไปเป็น integer)
```python
var = 11.12
var = int(var)
print(var) # ก็จะได้ผลลัพท์เป็น 11
```

และการใช้กับ `input()` ก็สามารถทำแบบนี้ได้เลย
```python
var1 = int(input())
var1 = bool(input())
var1 = float(input())
```

และเนื่องจากมี data type มีมากกว่า 4 ประเภท ตามที่พี่มงได้อธิบายไว้<br>
การแปลงประเภทข้อมูลชนิดอื่นๆ จะอยู่ใน lecture ถัดๆไปนะจ๊ะ

::: warning Challenge
น้องๆ ลองทดสอบดูครับ ตัวอย่างเช่น

```python
var1 = 1112
var2 = 0.1112
var3 = var1 + var2
```

พี่มงจึงได้อยากรู้ว่า `var3` นั้นได้จัดเก็บเป็นข้อมูลประเภทใด โดยการใช้ `type()` และก็ได้ผลบอกว่ามันคือประเภท float<br>
จึงถามน้องๆว่า var3 ทำไมจึงจัดเก็บไปเป็นประเภท float ครับ?
:::

---

## Arithmetic Operator
Arithmetic = อะไรซักอย่างที่มันเกี่ยวกับคณิตศาสตร์<br>
Arithmetic Operator = การทำสี่งต่างๆ กับตัวแปร เพื่อเอาไว้คำนวณเลขโดยเฉพาะ

ตัวอย่างประเภท Arithmetic Operator
| **Symbol**  | +     | -        | *        | /       | //             | %       | **       |
| ----------- | ----- | -------- | -------- | ------- | -------------- | ------- | -------- |
| **Name**    | Add   | Subtract | Multiply | Divide  | Floor Division | Modulus | Exponent |
| **Example** | 2+3   | 2-3      | 2*3      | 2/3     | 2//3           | 2&3     | 2**3     |
| **Results** | 5     | -1       | 6        | 0.66666 | 0              | 2       | 8        |

น้องๆอาจจะยังเห็น floor division และ modulus มาก่อนเลย พี่มงจะสอนแบบรวบรัดให้นะครับ

#### Floor Division
เป็นการทำการหาร แล้วค่อย **ปัดเศษลงไปเป็นเลขจำนวนเต็ม**

#### Modulus
เป็นการหาร เพื่อ **เอาแค่เศษของการหาร**

ตัวอย่าง
```python
value_a = 2
value_b = 3

print(value_a + value_b)    # แลดงค่าออกมาเป็น 5
print(value_a - value_b)    # แลดงค่าออกมาเป็น -1
print(value_a * value_b)    # แลดงค่าออกมาเป็น 6
print(value_a / value_b)    # แลดงค่าออกมาเป็น 0.666666...... (ไปเรื่อยๆ)
print(value_a // value_b)   # แลดงค่าออกมาเป็น 0
print(value_a % value_b)    # แลดงค่าออกมาเป็น 2
print(value_a ** value_b)   # แลดงค่าออกมาเป็น 8
```

::: warning
อย่าลืมว่าน้องๆจะต้องแปลงเป็นตัวเลขซะก่อนที่จะเล่นอะไรพวกนี้เนอะ

แล้วถ้าพี่ไม่เปลี่ยนหล่ะ เช่น `"2" + "2"` หรือ `2 + "2"` จะได้อะไรเอ่ย จะเฉลยคำตอบ lecture ที่เกี่ยวกับ String นะครับ
:::

### Order of Operations
ด้วยจากว่า หากมีสมการแบบนี้ `112 + 215 * 482 - 54 / 4782` แล้วคอมจะรู้หมือไร่ ว่าจะต้องคำนวณอย่างไร และน้องจะรู้หมือไร่ ว่ามันจะได้ผลลัพท์ยังไง<br>
ดังนั้น Python จึงใช้กฎ PEMDAS เพื่อเป็นการเรียงลำดับของการคำนวณคณิตศาสตร์ครับ<br>
[http://study.com/academy/lesson/what-is-pemdas-definition-rule-examples.html](http://study.com/academy/lesson/what-is-pemdas-definition-rule-examples.html)

| **P**           | **E**           | **M**              | **D**        | **A**        | **S**          |
| --------------- | --------------- | ------------------ | ------------ | ------------ | -------------- |
| **P**arenthesis | **E**xponential | **M**ultiplication | **D**ivision | **A**ddition | **S**utraction |
| ()              | **              | *                  | /            | +            | -              |

นั่นคือจะเรื่มทำในวงเล็บก่อน (Parenthesis) แล้วค่อยทำเลขยกกำลัง (Exponent) ตามด้วยคูณ (Multiply) หาร (Divide) บวก (Add) ลบ (Subtract) ตามลำดับ

หากน้องๆ ยังไม่แม่นการคำนวณเลขแบบนี้ ก็สามารถศึกษาต่อได้จาก Khan Academy นะครับ : [https://www.khanacademy.org/math/pre-algebra/pre-algebra-arith-prop/pre-algebra-order-of-operations/v/introduction-to-order-of-operations](https://www.khanacademy.org/math/pre-algebra/pre-algebra-arith-prop/pre-algebra-order-of-operations/v/introduction-to-order-of-operations)
