## جعل كل شيء عشوائي

يمكنك بالحقيقة استخدام أرقام عشوائية لجعل البرنامج بأكمله يعمل مرارًا وتكرارًا ، مع تغيير النمط في كل مرة! سيبدو قليلاً كما فعلت شاشات التوقف في التسعينيات... وهو أمر ربما لن تتذكره ، ولكن اسأل أحد والديك!

تحتاج إلى بعض التغييرات لجعل هذا يحدث. أول واحد هو أنك تحتاج إلى تعيين متغيرين `زيادة`{:class="block3variables"} و `درجات`{:class="block3variables"} عشوائيًا بدلاً من طلبها من المستخدم. لذلك تحتاج إلى تغيير بعض كتل التعليمات البرمجية الخاصة بك.

--- task --- قم بإزالة الأسئلة من التعليمات البرمجية الخاصة بك، وقم بتحديثه لاستخدام أرقام عشوائية بدلاً من ذلك.

```blocks3
    عند نقر ⚑
    اجعل [خطوات v] مساويًا [0]
-   اسأل [كم عدد الخطوات التي يجب عليّ أن أنمو بها؟] وانتظر
+   اجعل [زيادة v] مساويًا (عدد عشوائي بين (1) و (10))
-   اسأل [كم درجة يجب أن استدر؟] وانتظر
+   اجعل [درجات v] مساويًا (عدد عشوائي بين (1) و (180))
    ارفع القلم
```

---/task ---

إذا قمت بتشغيل البرنامج الآن ، فستجد أنه يرسم نمطًا عشوائيًا ، ولكن مرة واحدة فقط. لماذا تعتقد ذلك؟

ذلك لأن الحلقة تعمل فقط حتى تصل إلى حافة المنصة.

--- task --- تحتاج إلى حلقة أخرى تعمل إلى الأبد (لذلك كتلة `كرر باستمرار`{:class="block3control"}!) خارج الحالية لابقائها تعمل مراراً وتكراراً. فقط اسحب واحدة من قسم **التحكم**، وإضاف جميع التعليمات البرمجية الأخرى فيها.

```blocks3
    عند نقر ⚑
+   كرِّر باستمرار 
        اجعل [خطوات v] مساويًا [0]
        اجعل [زيادة v] مساويًا (عدد عشوائي بين (1) و (10))
        اجعل [درجات v] مساويًا (عدد عشوائي بين (1) و (180))
        ارفع القلم
        اختفِ
        مسح الكل
        اذهب إلى الموضع س: (0) ص: (0)
        إجعل لون القلم مساوياً لـ [#4a6cd4]
        أنزل القلم
        كرِّر حتى <ملامس لـ [edge v] ؟> 
            تحرك (خطوات) خطوة
            استدر ↻ (درجات) درجة
            غيِّر [steps v] بمقدار (زيادة)
        end
    end
```

--- /task ---

الآن لديك حقا شيء رائع للنظر اليه!

ومع ذلك ، قد تلاحظ أنه ،بين الحين والآخر ، يرسم الكمبيوتر شيئًا يبدو سيئًا. هذا لأن بعض الأرقام لبعض هذه المتغيرات هي مجرد خيارات سيئة ، وبعض **مجموعات من تلك الأرقام** هي أيضا خيارات سيئة.

في البطاقة التالية، سوف تساعد الكمبيوتر على اختيار مجموعات جيدة فقط!