عملت 2 Pointer 
الـ left بيشير الي اول حرف في string
الـ right بيشير الي اخر حرف في string

اعتمدت علي swap بينهم من خلال متغير temp

يعني في حالة مثلا "ahmed"

في اول iteration في loop 
الـ temp هنحط فيه قيمة left اللي هيا 'a'
الـ left هنحط فيه قيمة right اللي هيا 'd'
وناخد من temp القيمة اللي حطيناها فيه اللي هيا 'a' نحطها في right

ونكرر العملية دي لحد ما نبدل a with d , h with e , m still in same location

---
**Time Complexity**

احنا مستخدمين 2 Pointer ماشيين عكس بعض 
يعني في كل iteration بنقرب من منتصف الـ string
يعني تقريبا هنحتاج  `n / 2` من العمليات
لكن في Big O بنهمل الثابت 1/2   ==> Time Complexity = O(n)

---
**Space Complexity**

إحنا **مش بنعمل Array جديدة**

عندنا فقط:

```
int left = 0;
int right = s.Length - 1;
char temp;
```

يعني مهما كان حجم الـ array كبير هنفضل نستخدم نفس عدد المتغيرات.
عشان كدا المساحة هتفضل ثابتة ==> Space Complexity = O(1)


![[Reverse String.jpg]]