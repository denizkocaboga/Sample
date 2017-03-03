Gecikme için kusura bakmayın. Daha önce telefonda da dediğim gibi. Geçen hafta şehir dışındaydım bu yüzden projeye ancak çarşamba günü başlayabildim. Bundan dolayı aşağıda ki istekleri de henüz bitiremedim. Ancak bugün her halükarda bunlarıda ekleyip yayınlayacağım ve size de bilgisini vereceğim. İster. İsterseniz bakarsınız. Ben şimdiden yapacaklarımı yazıyorum buraya.

  a. Logging: 
      NLog kullanacağım. Log'u text dosyasında tutacağım. Config ayarlarından her gün yeni bir dosya oluşturmasını sağlayacağım. 
      Her request InfoLog'a kaydedilecek. 
      Excepionlar ErrorLoga'a kaydedilecek.
      
  b. ExceptionHandling : 
      SampleException isminde bir sınıf yaratıp, bundan da BusinessException ve DevException(ismi farklı olabilir) türeteceğim.       
      Kod içinde duruma göre ya bu exception'lardan yeni exception'lar türeteceğim ya da bu exception tiplerini fırlatacağım.
      Exception mesajına direk açıklamayı yazmayacağım. Bunun yerine keyword yazacağım. Örn;NotUpdated_PleaseCheckYourFileType.      
      Controller tarafında PostSharp ile Aspect Oriented bir mimarı kuracağım. 
      Fırlattığım exceptionların mesajlarına yazdığım keywordleri yakaladığım yerde ilgili dildeki Resource.resx'den açıklamayı alacağım.
      Yakaldığım Exception'ları ErrorLog tipinde Nlog'a kaydedeceğim. 
      BusinessException'lar localize edilip kullanıcıya gösterilecek. Ve loga atılacak.
      DevException'lar için kullanıcıya genel bir hata mesajı gösterilecek. Belki detay tuşu koyarım. log'a bakmadan hata görülebilir olur.
        
  c. Unit test : 
  NUnit kullanacağım. ElasticSearch sınıflarını DI yaptığım için mock edilebilir olacak. Bu sayede Repository'de test edilebilir olacak.
  
  d. Kolay Çalıştırılabilir Olması : 
  Veri tabanı olarak ElasticSearch kullandım. Hem talebinize en uygun teknolojinin bu olduğunu düşünüyorum hem de görüşmemizde kullandığınızı söylemiştiniz.
  Ancak ElasticSearch projeye gömülü değil. Vaktim olmadı onu yapmaya. Dediğim gibi onu da yapacağım.
  Bundan dolayı projeyi çalıştırabilmek için localinize elastic kurmanız gerekiyor. 
 
 
