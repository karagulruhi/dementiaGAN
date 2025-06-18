📌 Hakkında
Bu proje, beyin MR görüntüleri üzerinden demans teşhisine yardımcı olmak amacıyla geliştirilmiş derin öğrenme tabanlı bir görüntü sınıflandırma sistemidir. Özellikle Moderate Demented gibi az temsil edilen sınıflarda veri dengesizliğini gidermek için, DCGAN (Deep Convolutional Generative Adversarial Network) kullanılarak sentetik görüntüler üretilmiştir.

Zenginleştirilmiş veri seti, başta VGG19 olmak üzere çeşitli evrişimli sinir ağları (CNN) ile eğitilmiştir. Amaç, MR görüntülerini şu dört klinik kategoriye doğru şekilde ayırabilmektir:

Non Demented

Very Mild Demented

Mild Demented

Moderate Demented

Ayrıca modelin karar mekanizmasını görselleştirmek için Grad-CAM ısı haritaları entegre edilmiştir. Bu sayede, modelin sınıflandırma sırasında odaklandığı beyin bölgeleri yorumlanabilir hale gelmiştir.

Proje, yapay zekâ destekli tıbbi görüntü analizi ile nörolojide erken teşhis ve karar destek sağlamayı hedefleyen bir akademik araştırma çalışmasıdır.
This project presents a deep learning-based visual classification system designed to assist in the diagnosis of dementia through brain MRI images. The core idea is to enhance the limited and imbalanced dataset using a DCGAN (Deep Convolutional Generative Adversarial Network) to generate synthetic brain images, especially for underrepresented dementia stages like Moderate Demented.

The augmented dataset is then used to train various convolutional neural networks (CNNs), with a particular focus on VGG19. The goal is to accurately classify MRI images into four clinical categories:

Non Demented

Very Mild Demented

Mild Demented

Moderate Demented

The system aims to provide a supportive tool for early and stage-specific diagnosis of Alzheimer’s and related cognitive disorders. Grad-CAM visualizations are also integrated to offer interpretable heatmaps, helping experts understand which brain regions the model focuses on during classification.

This project has been developed as part of an academic research initiative, with the goal of contributing to early diagnosis and decision support in neurology using AI-driven medical image analysis.
