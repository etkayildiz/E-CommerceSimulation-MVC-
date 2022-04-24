# E-Commerce-Simulation

E-CommerceSimulation-API-WinUI Repository'deki BankaAPI, KargoAPI, DepoAPI, MagazaWinUI, KargoWinUI projeleri ile birlikte çalışır.

DesignPatterns = SingletonPattern, StrategyPattern

ArchitecturePattern = NTier

Bu proje belirli API ve WindowsForm uygulamaları ile birlikte çalışan, bilgisayar ürünleri satışı yapan bir web sitesinin simülasyonudur. Proje Initilization ile belirli ürünler oluşturulmuş şekilde çalışır. Kullanıcı, siteye üye olmadan siteye giriş yapıp ürünleri sepete ekleyebilir fakat satın alma aşamasında üye olması gerekir. Üyelik gerçekleştiğinde kullanıcıya aktivasyon maili gönderilir ve linke tıklanmadan üyeliği aktifleşmez. Üyelik işlemi tamamlandığında kullanıcı sepete attığı ürünlerin satın alımını gerçekleştirebilir. Satın alma aşamasında girilen kart bilgileri BankaAPI'a gider ve buradan successStatuseCode döndüğünde DepoAPI'a gider depodan da olumlu dönüş olduğunda KargoAPI'a adres bilgileri yollanır ve sipariş tamamlanır. Kullanıcıya, sipariş tutarı ve kargo takip numarasını bildiren mail sistem tarafından gönderilir. Sitenin kargo takip bölümünden bu takip no ile kargo takibi gerçekleştirilir. Aynı zamanda KargoWinUI'da kargo şirketi elemanının yaptığı güncellemeler(Dağıtıma çıktı - Kargo teslim edildi vb.) kullanıcı tarafından görülebilir. Kargo elemanı teslim edildi bilgisi girdiğinde, kullanıcıya bilgilendirme maili sistem tarafından gönderilir. MagazaWinUI sayesinde mağazada yapılan satışlarda kayıt altına alınıp DepoAPI'dan stok düşer. DepoAPI'da stoğu azalan ürünlerin bilgisi, depo sorumlusuna sistem tarafından mail gönderilir.

Admin rolüne sahip bir yetkili giriş yaptığında, categoryCRUD, productCRUD ve yetkilendirme işlemlerinin yapıldığı admin paneli açılır. Sitedeki bize ulaşın kısmından kullanıcılar tarafından yazılan destek talepleri, teknik destek sorumlusunun mailine düşer.
