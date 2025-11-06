# Thining-analysis-with-YOLO

Proje, meşcerelerin sıklık sınıflandırmasını YOLOv11 derin öğrenme modeli ile gerçekleştirerek yangın öncesi sıklık bakımını optimize etmeyi hedeflemektedir.

## Dataset
Projenin veri seti, Uydu görüntülerinden ve Google Earth simülatörlerinden  fotoğraf ve videolar ile oluşturulmuştur. Google Earth Engine (GEE) platformunda ön işleme tabi tutulmuştur. 
Veriler; meşcere sıklık sınıfları kuralları gereğince Orman Bakanlığı tarafından yayınlanan tebliğlere bağlı olarak belirlenmiştir.

• Normal Kapalı: Ağaç tepeleri arasında boşluk bulunmaması ya da tepelerin birbirine
değmesi hali (Tepe kapalılığı %71 ve daha fazla)
• Orta Kapalı: Ağaç tepeleri arasında en fazla bir tepe girecek şekilde boşlukların
bulunması hali (Tepe kapalılığı %41 -70 arasında)
• Gevşek Kapalı: Ağaç tepeleri arasında 3-4 tepe girecek şekilde boşlukların bulunması
hali (Tepe kapalılığı %11 -40 arasında)
• Boşluklu Kapalı: Ağaç tepelerinin birbirinden bağımsız olması ve ağaçlar arasında fazla
mesafe bulunması (Tepe kapalılığı %1- %10 arasında)

<img width="800" height="228" alt="image" src="https://github.com/user-attachments/assets/aaa3f600-d171-44d6-b8f3-680536e42935" />

Bakanlığın belirlediği sınıf kurallarına göre elde edilen görüntüler Roboflow Annotate ile manuel olarak etiketlenerek veri seti oluşturulmuştur.

## Training

