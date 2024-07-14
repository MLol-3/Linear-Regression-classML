# Machine-Learning-ClassML
## แบบฝึกหัดเขียนโปรแกรมครั้งที่ 1 Linear Regression
1. เขียนโปรแกรมสำหรับสร้างแบบจำลองเชิงเส้นด้วยวิธีลดตามความชัน พร้อมทั้งแสดงฟังก์ชันค่าใช้จ่ายในรูปของคอนทัวร์และแสดงให้เห็นถึงขั้นตอนในการปรับพารามิเตอร์ (Lecture หน้าที่ 49)

2. เขียนโปรแกรมสำหรับแสดงผลกระทบต่อการทำงานของวิธีลดตามความชันและฟังก์ชันค่าใช้จ่าย เมื่อตัวแปร x หลายตัวมีค่าแตกต่างกันมาก และแสดงผลของการปรับปรุงประสิทธิภาพด้วยการทำให้เป็นมาตรฐาน (Lecture หน้าที่ 61)

3. เขียนโปรแกรมสำหรับแสดงผลของการปรับพารามิเตอร์การเรียนรู้ (Lecture หน้าที่ 66)

4. เขียนโปรแกรมสำหรับเปรียบเทียบผลลัพธ์ที่ได้จากวิธีสมการปรกติและวิธีลดตามความชัน (Lecture หน้าที่ 57 และ 59)

## แบบฝึกหัดเขียนโปรแกรมครั้งที่ 2 Generalization and Model Evaluation
1. เขียนโปรแกรมเพื่อทดสอบความเที่ยงตรง (Precision) และการทดสอบความแม่นยํา (Accuracy) ของวิธี Resubstitution, Holdout และ Cross Validation โดยใช้ข้อมูล height weight โดยให้ออกแบบการทดลองเอง 


2. หาค่าความเอนเอียงและความแปรปรวนด้วย analytical method และ simulation ของ 1.แบบจำลองค่าคงที่ 2.แบบจำลองเชิงเส้นและ 3.แบบจำลองเชิงเส้นผ่านจุดกำเนิด

    2.1 เมื่อกำหนดให้ฟังก์ชันเป้าหมายคือ sin(pi*x) และสุ่มข้อมูลด้วยการแจกแจงแบบเอกรูปออกมา 2 ตัวอย่างในช่วง [-1,1] (Lecture หน้า 18)

    2.2 เมื่อกำหนดให้ฟังก์ชันเป้าหมายคือ x^2 และสุ่มข้อมูลด้วยการแจกแจงแบบเอกรูปออกมา 2 ตัวอย่างในช่วง [-1,1] 

3. เขียนโปรแกรมสำหรับเส้นโค้งการเรียนรู้เปรียบเทียบระหว่างแบบจำลองค่าคงที่ แบบจำลองเชิงเส้น แบบจำลองเชิงเส้นผ่านจุดกำเนิด และทดลองเพิ่มเติมด้วยการใส่สัญญาณรบกวน (Lecture หน้า 35-37)

ป.ล. ให้ใช้ normal equation หรือ lib ในการสร้างแบบจำลอง ไม่แนะนำให้ใช้ gradient descent
https://en.wikipedia.org/wiki/Expected_value

## แบบฝึกหัดเขียนโปรแกรมครั้งที่ 3 Model Selection
1. ทดลองซ้ำและการปรับพารามิเตอร์ให้มากกว่าใน lecture หรือลอง generate date ที่แตกต่างจากที่เรียน

2. เขียนโปรแกรมสำหรับการทำ Nested Cross-Validation และออกแบบการทดลองเพื่อแสดงให้เห็นถึงความจำเป็นของการทำสองลูปแทนที่จะทำเพียงแค่ลูปเดียว
=======
# Linear Regression 📉

**Linear Regression** หรือ **การถดถอยเชิงเส้น** เป็นหนึ่งในวิธีการพื้นฐานและสำคัญที่ใช้ในการสร้างโมเดลสำหรับการทำนายค่าตัวแปรเชิงปริมาณ (regression analysis) โดยเป็นเทคนิคการเรียนรู้แบบมีผู้สอน (supervised learning) ที่มีจุดประสงค์เพื่อหาความสัมพันธ์เชิงเส้นระหว่างตัวแปรอิสระ (independent variables) และตัวแปรตาม (dependent variable)

## ขั้นตอนในการทำ Linear Regression
1. **Representation** - การแสดงตัวแปรและสมการของโมเดล
2. **Evaluation** - การประเมินผลลัพธ์และประสิทธิภาพของโมเดล
3. **Optimization** - การปรับแต่งโมเดลเพื่อให้ได้ค่าพารามิเตอร์ที่ดีที่สุด

## สูตรในการคำนวณ
สมการของ Linear Regression มีรูปแบบดังนี้:
\[ y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \ldots + \beta_n x_n \]
- \( y \) คือค่าตัวแปรตาม (dependent variable)
- \( \beta_0 \) คือค่าคงที่ (intercept)
- \( \beta_1, \beta_2, \ldots, \beta_n \) คือสัมประสิทธิ์ (coefficients) ของตัวแปรอิสระ (independent variables)
- \( x_1, x_2, \ldots, x_n \) คือตัวแปรอิสระ

## การประเมินผลลัพธ์
ใช้ค่าความคลาดเคลื่อน (error metrics) ต่างๆ ในการประเมินผลลัพธ์ของ Linear Regression  เช่น:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

## การทำ Optimization
การทำ Optimization ของ Linear Regression ใช้เทคนิคต่างๆ เช่น Gradient Descent เพื่อหาค่าพารามิเตอร์ที่เหมาะสมที่สุด

## Assignments

### [Assignment 01](https://github.com/MLol-3/Linear-Regression-classML/tree/2c8db0b670d1503d63f56d5f55d1b12ca0922def/Assignment1)
เริ่มต้นด้วยการสร้างโมเดล Linear Regression อย่างง่ายและการทำความเข้าใจพื้นฐานของการถดถอยเชิงเส้น

### [Assignment 02](https://github.com/MLol-3/Linear-Regression-classML/tree/2c8db0b670d1503d63f56d5f55d1b12ca0922def/Assignment2)
ศึกษาและนำเสนอวิธีการประเมินผลลัพธ์ของโมเดล รวมถึงการใช้ค่าความคลาดเคลื่อน (error metrics) ต่างๆ

### [Assignment 03](https://github.com/MLol-3/Linear-Regression-classML/tree/2c8db0b670d1503d63f56d5f55d1b12ca0922def/Assignment3)
การทำ Optimization โดยใช้เทคนิคต่างๆ เช่น Gradient Descent เพื่อหาค่าพารามิเตอร์ที่เหมาะสมที่สุด

### [Assignment 04](https://github.com/MLol-3/Linear-Regression-classML/tree/2c8db0b670d1503d63f56d5f55d1b12ca0922def/Assignment4)
การประยุกต์ใช้ Linear Regression ในปัญหาที่มีหลายตัวแปรอิสระ (Multiple Linear Regression) และการปรับปรุงโมเดลให้แม่นยำยิ่งขึ้น
>>>>>>> 0499c80 (prepare README for the next meeting)
