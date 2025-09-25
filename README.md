# Intel-image-classification

## 📌 Projenin Amacı
Bu projenin amacı, **Intel Image Classification** veri seti kullanılarak farklı doğal sahne görüntülerini (örneğin: dağ, orman, şehir, deniz, binalar vb.) doğru bir şekilde sınıflandırabilen bir derin öğrenme modeli geliştirmektir. Görüntü sınıflandırması, bilgisayarla görme alanında yaygın olarak kullanılan önemli bir problemdir ve bu çalışma, temel bir CNN mimarisi ile birlikte farklı yöntemlerin denenmesini kapsamaktadır.

## 📂 Veri Seti Hakkında
Proje kapsamında **[Intel Image Classification Dataset](https://www.kaggle.com/datasets/puneet6060/intel-image-classification/data)** kullanılmıştır.  
Veri seti 6 farklı sınıfa ait toplamda **25.000+** renklendirilmiş görüntü içermektedir.  
Sınıflar şunlardır:
- Buidings (Binalar)
- Forest (Orman)
- Glacier (Buzul)
- Mountain (Dağ)
- Sea (Deniz)
- Street (Sokak)

Her bir görüntü **150x150 piksel** boyutuna getirilerek modele verilmiştir.

## 🛠 Kullanılan Yöntemler
- **Python (TensorFlow & Keras)** kullanılarak derin öğrenme modeli oluşturuldu.
- Veri ön işleme kapsamında:
  - Görseller yeniden boyutlandırıldı.
  - Normalizasyon uygulandı.
  - Eğitim verilerine veri artırma (data augmentation) teknikleri uygulandı.
- Model mimarisi:
  - CNN tabanlı katmanlar (Conv2D, MaxPooling2D, Dropout, Dense)
  - Aktivasyon fonksiyonu olarak ReLU ve çıkış katmanında Softmax
- Eğitim süreci:
  - Adam optimizer
  - Categorical Crossentropy loss
  - Erken durdurma (EarlyStopping) ile aşırı öğrenmenin önlenmesi
- Transfer Learning:
  - Hazır model olarak EfficientNetB0 modelinin kullanılması
  - 

## 📊 Elde Edilen Sonuçlar
- Modelin **Accuracy**: 0.81
- Modelin **Val Accuracy**: 0.82
- Test verisi üzerinde yapılan değerlendirmede modelin sınıflandırma başarısı **başarılı bir şekilde** elde edilmiştir.
- Efficient modelinin **Accuracy**:0.91
- Efficient modelinin **Val Accuracy**:0.92
## 🔗 Kaggle Notebook
Projenin detaylı kodlarına ve çıktılara ulaşmak için Kaggle notebook linkine göz atabilirsiniz:  

👉 https://www.kaggle.com/code/emirkaya1040/intel-image-classification

---
