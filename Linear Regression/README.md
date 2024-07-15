# Linear Regression 📉

**Linear Regression** หรือ **การถดถอยเชิงเส้น** เป็นหนึ่งในวิธีการพื้นฐานและสำคัญที่ใช้ในการสร้างโมเดลสำหรับการทำนายค่าตัวแปรเชิงปริมาณ (regression analysis) โดยเป็นเทคนิคการเรียนรู้แบบมีผู้สอน (supervised learning) ที่มีจุดประสงค์เพื่อหาความสัมพันธ์เชิงเส้นระหว่างตัวแปรอิสระ (independent variables) และตัวแปรตาม (dependent variable)

## ขั้นตอนในการทำ Linear Regression
1. **Representation** - การแสดงตัวแปรและสมการของโมเดล
2. **Evaluation** - การประเมินผลลัพธ์และประสิทธิภาพของโมเดล
3. **Optimization** - การปรับแต่งโมเดลเพื่อให้ได้ค่าพารามิเตอร์ที่ดีที่สุด

## สูตรในการคำนวณ
สมการของ Linear Regression มีรูปแบบดังนี้:
\[ $y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \ldots + \beta_n x_n $\]
- \($ y $\) คือค่าตัวแปรตาม (dependent variable)
- \($ \beta_0 $\) คือค่าคงที่ (intercept)
- \($ \beta_1, \beta_2, \ldots, \beta_n $\) คือสัมประสิทธิ์ (coefficients) ของตัวแปรอิสระ (independent variables)
- \($ x_1, x_2, \ldots, x_n $\) คือตัวแปรอิสระ

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

