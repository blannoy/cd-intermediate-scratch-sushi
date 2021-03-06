## اجمل خطوط

الوقت لإضافة الوان! إلى الآن ، الخط الخاص بك هو لون واحد ، ولكن **القلم** لديه كتل يمكن أن تغير لونه. ومع كتلة **المشغل** الصحيحة، يمكنك حتى تغيير اللون عشوائيا!

كتلة تغيير لون **القلم** هي `تغيير لون القلم بمقدار`{:class="block3extensions"}:

```blocks3
    غيّر لون القلم بمقدار (10)
```

--- task --- اسحب واحدة من تلك الكتل وضعها داخل حلقة `كرر حتى`{:class="block3control"}, مثل هذا:

```blocks3
    كرِّر حتى <ملامس لـ [edge v] ؟> 
+       غيّر لون القلم بمقدار (10)
        تحرك (steps) خطوة
        استدر ↻ (degrees :: variables) درجة
        غيِّر [steps v] بمقدار (increase :: variables)
    end
```

---/task ---

هذا رائع ، لكن قابل للتنبؤ قليلاً. يمكنك جعله أكثر متعة قليلاً إذا أضفت رقمًا عشوائيًا إليه، بهذا يتغير اللون بشكل عشوائي.

--- task --- ضع كتلة **المشغل** العدد عشوائي في كتلة `غير القلم اللون بمقدار`{:class="block3extensions"} واختر بعض القيم لتكون بداخلها. أود ان أحاول `1` و `100` للبدأ.

```blocks3
    كرِّر حتى <ملامس لـ [edge v] ؟> 
+       غيّر لون القلم بمقدار (عدد عشوائي بين (1) و (100))
        تحرك (steps) خطوة
        استدر ↻ (degrees :: variables) درجة
        غيِّر [steps v] بمقدار (increase :: variables)
    end
```

--- /task ---

--- task --- حاول تشغيله مرة أخرى ، وشاهد قوس قزح عشوائي! --- /task ---