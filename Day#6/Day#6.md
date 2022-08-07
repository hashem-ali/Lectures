
ماهي مكتبة NumPy ؟
مقدمة عن مكتبة NumPy
- من المعروف أن لغة البايثون توفر العديد من المكتبات الرياضية ولكن هذه المكتبات تعتبر بسيطة وغير كافية لمعظم العمليات الحسابية في تحليل البيانات ومن هنا جاءت الحاجة لمكتبات توفر مزايا أفضل لإتمام العمليات الرياضية مثل مكتبة NumPy.
- تعتبر مكتبة NumPy من أهم المكتبات المستخدمة في الحوسبة العلمية (scientific computing) وتحليل البيانات وهي تعتبر الأساس الذي تم بناء العديد من المكتبات الرياضية عليه مثل مكتبة pandas حيث تم تطوير هذه المكتبة بالاعتماد على المفاهيم الخاصة بمكتبة NumPy لذا فإن تعلم المفاهيم الأساسية في هذه المكتبة مهم عند استخدام المكتبات الرياضية الأخرى.
- مكتبة NumPy هي مكتبة مفتوحة المصدر تم تطويرها من قبل Travis Oliphant في عام 2006.


مميزات مكتبة NumPy
- مكتبة NumPy تعتبر الأكثر استخدامًا لحساب المصفوفات متعددة الأبعاد والمصفوفات الكبيرة (multidimensional arrays and large arrays).
- تحتوي العديد من functions التي تتيح إجراء عمليات على المصفوفات بطريقة أكثر كفاءة وفعالية.
- إجراء عمليات حسابية عالية المستوى (high-level mathematical calculations).


مفاهيم أساسية

قبل التعرف على المصفوفات التابعة لمكتبة NumPy توجد لدينا أشكال مختلفة من وحدات التخزين وهي كالتالي:

- 
![Scalar, vector, matrix, tensor | Credit: refactored.ai](https://i.pinimg.com/originals/80/c0/b1/80c0b157636aa8cb4b4e56180b8ab8e7.png)



أشكال المصفوفات في مكتبة NumPy


![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640342435524_Screen+Shot+1443-05-18+at+11.51.18+PM.png)

![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640342718403_Screen+Shot+1443-05-20+at+1.44.23+PM.png)



ماهو ndarray object:

- تعتمد مكتبة NumPy على كائن ndarray object وهو اختصار لكلمة N-dimensional array، هذا الكائن يعتبر مصفوفة متجانسة ومتعددة الأبعاد (multidimensional homogeneous array) وعدد العناصر فيها محدد مسبقا. نقصد ب(متجانسة) أي أن جميع العناصر فيها من نفس النوع (type) ونفس الحجم (size).
- يعتبر حجم NumPy arrays ثابت، أي بمجرد تحديد الحجم وقت الإنشاء فلن نستطيع تغيير ذلك بعكس Python lists التي يمكن تغيير حجمها.

تحميل مكتبة NumPy
يمكنك تحميل مكتبة عن طريق استخدام أحد الأمرين:

    conda install numpy # if you have conda distribution
    pip install numpy   # if you don't have conda distribution

ملاحظة: إذا قمت بتنزيل برنامج Anaconda لن تحتاج لهذه الخطوة لأن هذه المكتبات تكون مثبتة بشكل تلقائي على جهازك.

استدعاء مكتبة NumPy

    import numpy as np

إنشاء Array عن طريق مكتبة NumPy

    a = np.array([1, 2, 3])

إنشاء List في Python

    b = [1,2,3]
    type(a)
    type(b)

نلاحظ أن a من نوع `list`، أما b من نوع `numpy.ndarray`.

خصائص ndarray

أي كائن ndarray object يحمل عدة خصائص وهي كالتالي:

| الخاصية          | الوصف                                                                                                                                          |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| ndarray.size     | يحدد حجم المصفوفة وهو يشير لعدد العناصر في المصفوفة (حاصل ضرب عناصر shape).                                                                    |
| ndarray.shape    | يحدد عدد الأبعاد والعناصر بالمصفوفة عن طريق tuple يتكون من أرقام تحدد حجم كل بعد. على سبيل المثال: (n, m) يرمز n لعدد الصفوف و m لعدد الأعمدة. |
| ndarray.ndim     | يحدد عدد الأبعاد للمصفوفة  axes (dimensions).                                                                                                  |
| ndarray.itemsize | حجم  bytes في كل عنصر في المصفوفة.                                                                                                             |
| ndarray.dtype    | يحدد نوع البيانات حيث أن كل كائن ndarray object مرتبط بنوع واحد من البيانات.                                                                   |
| ndarray.data     | يشير إلى buffer الذي يحتوي العناصر الحقيقية في المصفوفة.                                                                                       |

لعرض نوع بيانات المصفوفة : 

    a.dtype

لعرض عدد أبعاد المصفوفة:

    a.ndim

لعرض حجم المصفوفة : 

    a.size

لعرض شكل المصفوفة: 

    a.shape

لعرض حجم  bytes في عناصر المصفوفة.

    print(a.itemsize) #It defines the size in bytes of each item in the array

لعرض buffer الذي يحتوي العناصر الحقيقية في المصفوفة.

    print(a.data)

مثال على المصفوفات من نوع 2D.

    b = np.array([[1.3, 2.4],[0.3, 4.1]])
    print('type = ', b.dtype)
    print('number of dimensions = ', b.ndim)
    print('shape = ', b.shape)
    print('size = ', b.size)
    print(b.itemsize)
    print(b.data)

لطباعة المصفوفة:

    b



أنواع البيانات المدعومة في NumPy
| الوصف                                                                             | نوع البيانات |
| --------------------------------------------------------------------------------- | ------------ |
| Boolean (true or false) stored as a byte                                          | bool_        |
| Default integer type (same as C long; normally either int64 or int32)             | int_         |
| Identical to C int (normally int32 or int64)                                      | intc         |
| Integer used for indexing (same as C size_t; normally either int32 or int64)      | intp         |
| Byte (–128 to 127)                                                                | int8         |
| Integer (–32768 to 32767)                                                         | int16        |
| Integer (–2147483648 to 2147483647)                                               | int32        |
| Integer (–9223372036854775808 to 9223372036854775807)                             | int64        |
| Unsigned integer (0 to 255)                                                       | uint8        |
| Unsigned integer (0 to 65535)                                                     | uint16       |
| Unsigned integer (0 to 4294967295)                                                | uint32       |
| Unsigned integer (0 to 18446744073709551615)                                      | uint64       |
| Shorthand for float64                                                             | float_       |
| Half precision float: sign bit, 5-bit exponent, 10-bit mantissa                   | float16      |
| Single precision float: sign bit, 8-bit exponent, 23-bit mantissa                 | float32      |
| Double precision float: sign bit, 11-bit exponent, 52-bit mantissa                | float64      |
| Shorthand for complex128                                                          | complex_     |
| Complex number, represented by two 32-bit floats (real and imaginary compon ents) | complex64    |
| Complex number, represented by two 64-bit floats (real and imaginary components)  | complex128   |

إنشاء مصفوفة تحتوي على بيانات من نوع String.

    g = np.array([['a', 'b'],['c', 'd']])
    g
    print(g.dtype)
    print(g.dtype.name)

إنشاء مصفوفة تحتوي على بيانات من نوع complex

    f = np.array([[1, 2, 3],[4, 5, 6]], dtype=complex)
    f

لتحويل المصفوفة لنوع بيانات آخر.

    n = np.array([['1', '2'],['3', '4']])
    n.astype(int)
إنشاء المصفوفة

 هناك عدة طرق لإنشاء NumPy arrays ومنها التالي:

- أولا: التحويل من Python structures مثل: (lists and tuples) عن طريق دالة ()array.

مثال على إنشاء مصفوفة من نوع List.

    c = np.array([[1, 2, 3],[4, 5, 6]])
    c

مثال على إنشاء مصفوفة من نوع Tuple.

    d = np.array(((1, 2, 3),(4, 5, 6)))
    d

مثال على إنشاء مصفوفة من نوع Tuple و List.

    e = np.array([(1, 2, 3), [4, 5, 6], (7, 8, 9)])
    e
-  ثانيا: دوال Intrinsic NumPy array creation functions مثل: (arange, ones, zeros).

مثال على إنشاء مصفوفة تحتوي جميع بياناتها على صفر.

    # a two-dimensional array 3x3
    np.zeros((3, 3))

مثال على إنشاء مصفوفة تحتوي جميع بياناتها على واحد.

    np.ones((3, 3))

مثال على إنشاء مصفوفة تحتوي على مجموعة متسلسلة من البيانات باستخدام دالة arange.

    np.arange(0, 10)
    np.arange(4, 10)
    np.arange(0, 12, 3) #(start, end, gap)
    np.arange(0, 6, 0.6)

مثال على إنشاء مصفوفة تحتوي على مجموعة متسلسلة من البيانات باستخدام دالة linspace.

    np.linspace(0,10,5)


> ملاحظة: الفرق بين arange و linspace هو أن مخرجات دالة arange لا تشمل القيمة النهائية بينما دالة linspace تشمل القيمة النهائية.
> 

مثال على إنشاء مصفوفة باستخدام دالة random.

    np.random.random(3) # The numbers obtained will vary with every run

مثال على إنشاء multidimensional array باستخدام دالة random.

    np.random.rand((3,3))

مثال على إنشاء مصفوفة تحتوي متغيرات من نوع int باستخدام دالة random.

    np.random.randint(2, size=10) # random 10 integers (from 0 to 1)
    np.random.randint(5, size=(2, 4)) # random 2*4 array (from 0 to 4)

يمكن أيضا إنشاء المصفوفات عن طريق دوال أخرى مثل:

    np.full((2,2),7) #(shape, fill_value)
    np.full((4, 4), [1, 2, 3, 4])
    np.eye(2) # 2-D array with ones on the diagonal and zeros elsewhere
    np.empty([2, 2], dtype=int) #(shape, dtype)
- ثالثا: عن طريق (Replicating, joining, mutating) للمصفوفة الموجودة.



تغيير شكل المصفوفة (Shape Manipulation)

مثال مصفوفة بشكل one-dimensional arrays.

    a = np.arange(0, 12)

لتغيير المصفوفة السابقة إلى شكل two-dimensional arrays نستخدم دالة reshape أو خاصية shape.

    a.reshape(3, 4)
    a.shape = (3, 4)


العمليات على المصفوفات
- العمليات الرياضية (Arithmetic Operators).
![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640365959065_Screen+Shot+1443-05-20+at+7.32.51+PM.png)

    a = np.arange(4)
    a+4
    a*2
    b = np.arange(4,8)
    a + b
    np.add(a, b) 
    a - b
    np.subtract(a,b)
    a * b
    np.multiply(a, b)
    a / b
    np.divide(a,b)



- ضرب المصفوفات (The Matrix Product).
    A = np.arange(0, 9).reshape(3, 3)
    B = np.ones((3, 3))
    A * B
    A.dot(B)
    np.dot(A,B)
    np.dot(B,A)


![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640365976131_Screen+Shot+1443-05-20+at+7.33.20+PM.png)

- عمليات (Increment and Decrement)


    a = np.arange(4)
    a += 1
    a -= 1
    a += 4
    a *= 2
- دوال ( Universal Functions (ufunc))
    a = np.arange(1, 5)
    np.sqrt(a)
    np.log(a)
    np.sin(a)
    np.exp(a)


- دوال (Aggregate Functions)
    a = np.array([3.3, 4.5, 1.2, 5.7, 0.3])
    a.sum()
    a.min()
    a.max()
    a.mean()
    a.std()




التعامل مع (Indexing, Slicing, and Iterating):
![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640367181477_Screen+Shot+1443-05-20+at+8.32.29+PM.png)

![](https://paper-attachments.dropbox.com/s_AE4C77E05A65BBD92AC0FE0838D02B46B216A7EB9BE1EE55872847C4D7390BFE_1640367206280_Screen+Shot+1443-05-20+at+8.33.16+PM.png)

أولا: Indexing
    a = np.arange(10, 16)
    a
    a[4]
    print(a[-1])
    print(a[-6])
    a[[1, 3, 4]] # two square brackets [[]]
    A = np.arange(10, 19).reshape((3, 3))
    A[1, 2]
    A[2, 0]
    A[2][0]
ثانيا: Slicing
    a = np.arange(10, 16)
    a[1:5] #[start index, final index]
    a[1:5:2]  #[start index, final index, gap]
    a[1:5:3]
    a[::2] #[start index =0, final index = maximum index, gap = 2]
    a[::3] #[start index =0, final index = maximum index, gap = 3]
    a[:5:2] #[start index =0, final index = 5, gap = 2]
    a[:5:] #[start index =0, final index = 5, gap = 1]
    # two-dimensional array
    A = np.arange(10, 19).reshape((3, 3))
    A[0,:] #[row=0 , column=all]
    A[:,0] #[row=all , column=0]
    A[0:2, 0:2]
    # not contiguous indexes >> specify an array of indexes.
    A[[0,2], 0:2]


ثالثا: Iterating

استخدام loop في Python

    for i in a:
        print(i)

استخدام loop في Python مع two-dimensional array

    for row in A:
        for item in row:
            print(item)
    
    for item in A.flat:
        print(item)

استخدام loop في Numpy



    # three arguments: the aggregate function, the axis on which to apply the iteration, and the array
    # axis = 0(columns), axis = 1(rows)
    np.apply_along_axis(np.mean, axis=0, arr=A)
    
    np.apply_along_axis(np.mean, axis=1, arr=A)
    
    def f2(x):
        return x/2
    
    np.apply_along_axis(f2, axis=1, arr=A)



مصادر إضافية:
- مكتبة Numpy.

https://numpy.org/doc/stable/user/absolute_beginners.html

- معلومات إضافية عن أنواع البيانات.

https://numpy.org/doc/stable/reference/arrays.dtypes.html#arrays-dtypes

- ملخص مكتبة Numpy ا NumPy Cheat Sheet.

http://datacamp-community-prod.s3.amazonaws.com/ba1fe95a-8b70-4d2f-95b0-bc954e9071b0


