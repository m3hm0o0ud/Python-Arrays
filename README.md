# Python-Arrays

### المصفوفات (Arrays) في بايثون مع أمثلة كاملة

**ملاحظة:** بايثون لا تحتوي على نوع بيانات مدمج للمصفوفات كما في بعض اللغات الأخرى مثل Java أو C++. ولكن يمكن استخدام **القوائم (Lists)** كبديل للمصفوفات نظرًا لمرونتها وسهولة استخدامها.

### ما هي المصفوفة (Array)؟

المصفوفة هي متغير خاص يمكنه تخزين **مجموعة من القيم** تحت اسم واحد، ويمكنك الوصول إلى هذه القيم عن طريق الفهرس (index).

#### مثال:

بدلاً من تخزين أسماء السيارات في متغيرات منفصلة:

```python
car1 = "Ford"
car2 = "Volvo"
car3 = "BMW"
```

يمكنك استخدام قائمة لتخزينها جميعًا في متغير واحد:

```python
cars = ["Ford", "Volvo", "BMW"]
```

### الوصول إلى عناصر المصفوفة

يمكنك الوصول إلى أي عنصر في المصفوفة باستخدام الفهرس الخاص به. يبدأ الفهرس في بايثون من 0.

#### مثال كامل:

```python
cars = ["Ford", "Volvo", "BMW"]

# الوصول إلى العنصر الأول
first_car = cars[0]
print("العنصر الأول هو:", first_car)

# الوصول إلى العنصر الثاني
second_car = cars[1]
print("العنصر الثاني هو:", second_car)

# الوصول إلى العنصر الثالث
third_car = cars[2]
print("العنصر الثالث هو:", third_car)
```

**الناتج:**

```
العنصر الأول هو: Ford
العنصر الثاني هو: Volvo
العنصر الثالث هو: BMW
```

### تعديل عناصر المصفوفة

يمكنك تغيير قيمة أي عنصر في المصفوفة بتعيين قيمة جديدة للفهرس المقابل.

#### مثال كامل:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل التعديل:", cars)

# تعديل العنصر الأول
cars[0] = "Toyota"

print("بعد التعديل:", cars)
```

**الناتج:**

```
قبل التعديل: ['Ford', 'Volvo', 'BMW']
بعد التعديل: ['Toyota', 'Volvo', 'BMW']
```

### معرفة طول المصفوفة

يمكنك استخدام الدالة `len()` لمعرفة عدد العناصر الموجودة في المصفوفة.

#### مثال كامل:

```python
cars = ["Ford", "Volvo", "BMW"]

length = len(cars)
print("عدد العناصر في المصفوفة هو:", length)
```

**الناتج:**

```
عدد العناصر في المصفوفة هو: 3
```

### التكرار عبر عناصر المصفوفة

يمكنك استخدام حلقة `for` للتنقل عبر جميع العناصر في المصفوفة.

#### مثال كامل:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قائمة السيارات:")
for car in cars:
    print(car)
```

**الناتج:**

```
قائمة السيارات:
Ford
Volvo
BMW
```

### إضافة عناصر إلى المصفوفة

يمكنك إضافة عنصر جديد إلى نهاية المصفوفة باستخدام الدالة `append()`.

#### مثال كامل:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل الإضافة:", cars)

# إضافة عنصر جديد
cars.append("Honda")

print("بعد الإضافة:", cars)
```

**الناتج:**

```
قبل الإضافة: ['Ford', 'Volvo', 'BMW']
بعد الإضافة: ['Ford', 'Volvo', 'BMW', 'Honda']
```

### إزالة عناصر من المصفوفة

يمكنك إزالة عنصر من المصفوفة باستخدام الدوال `pop()` أو `remove()`.

#### استخدام `pop()` لحذف عنصر بواسطة الفهرس:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل الحذف:", cars)

# حذف العنصر الثاني (الفهرس 1)
cars.pop(1)

print("بعد الحذف باستخدام pop:", cars)
```

**الناتج:**

```
قبل الحذف: ['Ford', 'Volvo', 'BMW']
بعد الحذف باستخدام pop: ['Ford', 'BMW']
```

#### استخدام `remove()` لحذف عنصر بواسطة القيمة:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل الحذف:", cars)

# حذف العنصر الذي قيمته "Volvo"
cars.remove("Volvo")

print("بعد الحذف باستخدام remove:", cars)
```

**الناتج:**

```
قبل الحذف: ['Ford', 'Volvo', 'BMW']
بعد الحذف باستخدام remove: ['Ford', 'BMW']
```

### طرق أخرى للتعامل مع المصفوفات (القوائم)

#### `insert()` لإضافة عنصر في موقع محدد:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل الإدخال:", cars)

# إدخال عنصر جديد في الفهرس 1
cars.insert(1, "Audi")

print("بعد الإدخال:", cars)
```

**الناتج:**

```
قبل الإدخال: ['Ford', 'Volvo', 'BMW']
بعد الإدخال: ['Ford', 'Audi', 'Volvo', 'BMW']
```

#### `clear()` لإزالة جميع العناصر:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل التفريغ:", cars)

# تفريغ القائمة
cars.clear()

print("بعد التفريغ:", cars)
```

**الناتج:**

```
قبل التفريغ: ['Ford', 'Volvo', 'BMW']
بعد التفريغ: []
```

#### `sort()` لترتيب العناصر:

```python
cars = ["BMW", "Ford", "Audi", "Volvo"]

print("قبل الترتيب:", cars)

# ترتيب القائمة تصاعديًا
cars.sort()

print("بعد الترتيب:", cars)
```

**الناتج:**

```
قبل الترتيب: ['BMW', 'Ford', 'Audi', 'Volvo']
بعد الترتيب: ['Audi', 'BMW', 'Ford', 'Volvo']
```

#### `reverse()` لعكس ترتيب العناصر:

```python
cars = ["Ford", "Volvo", "BMW"]

print("قبل العكس:", cars)

# عكس ترتيب القائمة
cars.reverse()

print("بعد العكس:", cars)
```

**الناتج:**

```
قبل العكس: ['Ford', 'Volvo', 'BMW']
بعد العكس: ['BMW', 'Volvo', 'Ford']
```

### مثال عملي شامل

لنجمع ما تعلمناه في مثال واحد:

```python
# إنشاء قائمة فارغة للطلاب
students = []

# إضافة طلاب إلى القائمة
students.append("أحمد")
students.append("سارة")
students.append("محمد")

print("قائمة الطلاب بعد الإضافة:")
for student in students:
    print(student)

# إدخال طالب في موقع معين
students.insert(1, "ليلى")

print("\nقائمة الطلاب بعد الإدخال:")
for student in students:
    print(student)

# حذف طالب معين
students.remove("سارة")

print("\nقائمة الطلاب بعد الحذف:")
for student in students:
    print(student)

# ترتيب قائمة الطلاب
students.sort()

print("\nقائمة الطلاب بعد الترتيب:")
for student in students:
    print(student)

# عكس ترتيب القائمة
students.reverse()

print("\nقائمة الطلاب بعد العكس:")
for student in students:
    print(student)

# معرفة عدد الطلاب
num_students = len(students)
print(f"\nعدد الطلاب الحالي: {num_students}")
```

**الناتج:**

```
قائمة الطلاب بعد الإضافة:
أحمد
سارة
محمد

قائمة الطلاب بعد الإدخال:
أحمد
ليلى
سارة
محمد

قائمة الطلاب بعد الحذف:
أحمد
ليلى
محمد

قائمة الطلاب بعد الترتيب:
أحمد
محمد
ليلى

قائمة الطلاب بعد العكس:
ليلى
محمد
أحمد

عدد الطلاب الحالي: 3
```

### الخلاصة

- **القوائم (Lists)** في بايثون هي بنية بيانات مرنة وقوية يمكن استخدامها كمصفوفات.
- يمكنك تخزين أنواع بيانات مختلفة في القائمة الواحدة.
- القوائم تدعم العديد من العمليات مثل الإضافة، الحذف، التعديل، الترتيب، والعكس.
- باستخدام القوائم، يمكنك إدارة مجموعات البيانات بسهولة وفعالية في بايثون.

### ملاحظة حول المكتبات الخارجية

إذا كنت تحتاج إلى التعامل مع مصفوفات كبيرة الحجم أو متعددة الأبعاد بكفاءة عالية، يمكنك استخدام مكتبة **NumPy**. توفر NumPy نوع بيانات **ndarray** الذي يدعم المصفوفات متعددة الأبعاد والعمليات الحسابية عالية الأداء.

#### مثال باستخدام NumPy:

```python
import numpy as np

# إنشاء مصفوفة باستخدام NumPy
arr = np.array([1, 2, 3, 4, 5])

print("المصفوفة:", arr)
print("نوع البيانات:", type(arr))
```

**الناتج:**

```
المصفوفة: [1 2 3 4 5]
نوع البيانات: <class 'numpy.ndarray'>
```

**ملحوظة:** لاستخدام NumPy، يجب عليك تثبيتها أولاً باستخدام الأمر `pip install numpy`.
