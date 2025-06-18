🧠 Synthetic Data Generation with DCGAN
One of the key challenges in medical image classification—particularly in dementia staging—is the imbalance and scarcity of data for certain classes. In our case, the Moderate Demented category was significantly underrepresented, making it difficult for convolutional neural networks to learn discriminative features and generalize well across all classes.

To address this issue, we implemented a Deep Convolutional Generative Adversarial Network (DCGAN) to generate synthetic brain MRI images. DCGAN consists of two adversarial networks—a generator and a discriminator—that are trained simultaneously. The generator learns to create realistic-looking MRI images from random noise, while the discriminator learns to distinguish between real and fake images. Through iterative training, the generator improves its capability to produce high-fidelity images that mimic the statistical patterns of the original class.

Key steps in our augmentation process include:

Data Preparation: The original Moderate Demented images were preprocessed (resized, normalized) and used to train the DCGAN.

Training the DCGAN: The generator and discriminator were trained over multiple epochs using binary cross-entropy loss and Adam optimizer. Visual quality of generated samples was monitored throughout.

Synthetic Sample Generation: After training, hundreds of synthetic MRI images were generated for the underrepresented class.

Integration into the Dataset: These generated images were combined with the original dataset, leading to a more balanced training set.

Model Retraining: The VGG19 classifier was retrained using this enriched dataset, showing improved accuracy and better sensitivity for minority classes.

This approach not only mitigated the effects of class imbalance but also demonstrated the potential of GANs in enhancing medical datasets without requiring expensive or ethically sensitive real data collection processes.


🧠 DCGAN ile Sentetik Veri Üretimi
Tıbbi görüntü sınıflandırmasında, özellikle demans evrelerini ayırt etmede en büyük zorluklardan biri, bazı sınıflar için verinin yetersiz ve dengesiz olmasıdır. Bu çalışmada, Moderate Demented sınıfındaki görüntülerin azlığı, derin öğrenme modellerinin bu evreyi öğrenmesini zorlaştırmıştır.

Bu sorunu çözmek için DCGAN (Deep Convolutional Generative Adversarial Network) tabanlı bir sentetik görüntü üretim süreci uygulanmıştır. DCGAN, birbirine karşı çalışan iki sinir ağından oluşur: üreteç (generator) ve ayırt edici (discriminator). Üreteç, rastgele gürültüden gerçekçi beyin MR görüntüleri üretmeye çalışırken; ayırt edici, bu görüntülerin sahte olup olmadığını anlamaya çalışır. Bu rekabetçi yapı sayesinde zamanla gerçeğe oldukça yakın yeni görüntüler üretilmiştir.

Sentetik veri artırımı şu adımlarla gerçekleştirilmiştir:

Veri Hazırlığı: Orijinal Moderate Demented görüntüleri ön işleme tabi tutuldu (yeniden boyutlandırma, normalizasyon) ve DCGAN eğitimi için kullanıldı.

DCGAN Eğitimi: Üreteç ve ayırt edici ağlar, Binary Cross-Entropy kaybı ve Adam optimizasyonuyla birçok epoch boyunca eğitildi. Görüntülerin kalitesi düzenli olarak takip edildi.

Sentetik Görüntü Üretimi: Eğitim sonrasında, az temsil edilen sınıf için yüzlerce yeni MR görüntüsü üretildi.

Veri Setine Entegrasyon: Bu görüntüler orijinal veriyle birleştirildi ve eğitim seti dengelendi.

Model Yeniden Eğitimi: Zenginleştirilmiş veri setiyle VGG19 modeli tekrar eğitildi ve özellikle azınlık sınıflarındaki başarı oranı gözle görülür biçimde arttı.

Bu yaklaşım, yalnızca sınıf dengesizliğini azaltmakla kalmamış, aynı zamanda etik veya mali nedenlerle zor elde edilen tıbbi verilerin GAN’lar aracılığıyla üretilebileceğini de göstermiştir.
