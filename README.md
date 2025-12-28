Şifreli Ağ Trafiği Sınıflandırma Projesi
Bu proje, şifreli ağ trafik akışlarını (YouTube, Spotify, Zoom vb.) makine öğrenmesi algoritmaları kullanarak sınıflandırmak için geliştirilmiştir.

Veri Seti
Projede kullanılan yüksek boyutlu PCAP veri setine aşağıdaki bağlantıdan ulaşabilirsiniz:

Veri seti: "xx" linkinde

İndirdiğiniz verileri projenin ana dizininde data/ klasörü altına, kategori isimlerine sahip alt klasörler (örneğin: data/video/, data/web/) şeklinde yerleştirmeniz gerekmektedir.

Kütüphane Bağımlılıkları
Proje Python 3.9+ sürümü ile uyumludur. Gerekli kütüphaneleri aşağıdaki komutla yükleyebilirsiniz:
pip install scapy pandas numpy scikit-learn matplotlib seaborn joblib

Kurulum ve Çalıştırma
Depoyu Klonlayın: Proje dosyalarını yerel makinenize indirin.

Verileri Hazırlayın: Yukarıdaki linkten indirdiğiniz verileri data/ klasörüne yerleştirin.

Programı Başlatın: Özellik çıkarımı, model eğitimi ve test süreçlerini başlatmak için ana betiği çalıştırın:
python main.py

İşlem Adımları
Özellik Çıkarımı: Scapy kullanılarak PCAP dosyalarından zaman ve boyut tabanlı 12 temel istatistiksel özellik çıkarılır.

Eğitim: Veri seti %80 eğitim, %20 test olarak bölünerek 9 farklı algoritma ile eğitilir.

Sonuç: Modellerin başarı metrikleri (Accuracy, F1-Score) karşılaştırılır ve en iyi model .joblib formatında kaydedilir.
