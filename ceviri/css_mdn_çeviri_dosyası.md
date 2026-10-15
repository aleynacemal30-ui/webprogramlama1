> **Uyarı:** Bu içerik, SCÜ Şarkışla UBYO Web Programlama I dersi kapsamında tamamen eğitim amaçlı çevrilmiş ve derlenmiştir. Orijinal dokümantasyon kaynakları (MDN Web Docs, Vue.js, Three.js vb.) kendi orijinal lisanslarına (CC-BY-SA, MIT) tabidir. Bu çalışmanın hiçbir ticari amacı yoktur.

# MDN Web Docs: CSS Temelleri (CSS Basics)
*Orijinal Kaynak: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics*

## CSS Nedir?
Tıpkı HTML gibi, CSS (Cascading Style Sheets - Basamaklı Stil Şablonları) de bir programlama dili değildir. Ayrıca bir işaretleme (markup) dili de değildir. CSS bir **stil (kural) dilidir**. HTML elemanlarına (element) belirli stiller uygulamamızı sağlar. 

Örneğin, HTML sayfasındaki tüm paragraf (`<p>`) elemanlarını seçip metin renklerini kırmızı yapmak istiyorsak, şu CSS kuralını yazarız:

```css
p {
  color: red;
}
```

## CSS Anatomisi
Bir CSS kural kümesinin (ruleset) yapısı şu şekildedir:

1. **Seçici (Selector):** Kural bloğunun başındaki HTML elemanının adıdır. Şekillendirilecek elemanları seçer (bu örnekte `p` elemanı). Başka bir elemanı şekillendirmek için seçiciyi değiştirmek yeterlidir.
2. **Bildirim (Declaration):** `color: red;` gibi, şekillendirmek istediğiniz elemanın hangi özelliğini (property) değiştireceğinizi belirten tekil kurallardır.
3. **Özellik (Property):** Bir HTML elemanını şekillendirebileceğiniz yollardır. (Örnekte `color` bir özelliktir.)
4. **Özellik Değeri (Property Value):** Özelliğin sağında, iki nokta üst üstenin ardından yer alan değerdir. Belirli bir özellik için birçok olası değerden birini seçer (örneğin kırmızı dışında `blue`, `green` gibi).

## Kutu Modeli (Box Model) Nedir?
CSS yazarken en çok fark edeceğiniz şeylerden biri, her şeyin kutular etrafında şekillenmesidir. CSS'te sayfa düzenini (layout) oluşturan her bir eleman aslında görünmez bir kutudur. Bu Kutu Modeli şu katmanlardan oluşur:

* **Padding (İç Boşluk):** İçeriğin etrafındaki boşluktur.
* **Border (Kenarlık):** Padding'in hemen dışında yer alan ve içeriği saran düz çizgidir.
* **Margin (Dış Boşluk):** Elementin etrafındaki boşluktur. Elementi diğer elemanlardan ayırır.

Kutu modeli kullanılarak, elemanların arka plan renkleri, kenarlıkları ve sayfadaki konumları (layout ve grid sistemleri aracılığıyla) kusursuz bir şekilde yönetilebilir.