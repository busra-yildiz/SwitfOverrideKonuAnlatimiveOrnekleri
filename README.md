# SwitfOverrideKonuAnlatimiveOrnekleri
Swift programlama dilinde "override" kelimesi, bir alt sınıfın (subclass) üst sınıfın (superclass) bir üyesini değiştirerek veya genişleterek 
kullanmasını ifade eder. Bu genellikle miras alma (inheritance) konseptiyle ilgilidir, yani bir sınıf, başka bir sınıftan özelliklerini ve 
davranışlarını devralabilir.

İşte Swift'te "override" kullanımının temel prensipleri:

Inheritance (Miras Alma): Bir sınıf, başka bir sınıftan miras alabilir. Miras alınan sınıfa "üst sınıf" veya "temel sınıf" denir ve miras alan 
sınıfa "alt sınıf" veya "alt sınıf" denir.
Override Sözcüğü: Alt sınıf, üst sınıfın bir üyesini (örneğin, bir metodu veya bir özelliği) kullanırken "override" anahtar kelimesini kullanarak
bu üyeyi değiştirebilir veya genişletebilir.
Override İşlevi: Bir metodu override ettiğinizde, alt sınıfın sürümü üst sınıfın sürümünü geçersiz kılar ve alt sınıfın kendi özgün uygulamasını sağlar.
Örnek bir kullanım:
class UstSinif {
    func yazdir() {
        print("Üst sınıfın metodu")
    }
}

class AltSinif: UstSinif {
    override func yazdir() {
        print("Alt sınıfın metodu")
    }
}

let ustSinifInstance = UstSinif()
let altSinifInstance = AltSinif()

ustSinifInstance.yazdir() // "Üst sınıfın metodu" çıktısını verir.
altSinifInstance.yazdir() // "Alt sınıfın metodu" çıktısını verir.

Yukarıdaki örnekte, AltSinif sınıfı UstSinif sınıfının yazdir metodunu override eder ve kendi uygulamasını sağlar. Bu nedenle altSinifInstance ile 
çağrıldığında "Alt sınıfın metodu" çıktısı alınır.

"override" kullanmak, sınıf hiyerarşileri içinde davranışı değiştirmek veya özelleştirmek için güçlü bir yol sağlar. Ancak, override kullanırken
dikkatli olmalısınız, çünkü yanlışlıkla yanlış davranışlara veya hatalara neden olabilir
