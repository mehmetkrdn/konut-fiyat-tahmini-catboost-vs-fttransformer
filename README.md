# 🏠 Ames Housing Price Prediction

## 📊 Linear Regression Baseline Model

Bu projede **Ames Housing** veri seti kullanılarak ev fiyat tahmini için bir **baseline regresyon modeli** oluşturulmuştur. Amaç, daha gelişmiş modeller (`CatBoost`, `FT-Transformer` vb.) öncesinde referans bir performans elde etmektir.

---

### 📁 Proje Aşaması
Bu notebook: `02_modeling_evaluation.ipynb`

**Bu aşamada:**
* **Ön işlenmiş veri** kullanılmıştır.
* **Linear Regression** modeli kurulmuştur.
* Model performansı **validation** ve **cross-validation** ile değerlendirilmiştir.

---

### ⚙️ Kullanılan Yöntemler

1.  **Train / Validation Split**
    * Veri **%80 eğitim** ve **%20 doğrulama** olarak ayrılmıştır.
    * ➡️ *Modelin gerçek performansını görmek için kullanılmıştır.*
2.  **Linear Regression**
    * Temel doğrusal regresyon modeli uygulanmıştır.
    * ➡️ *Diğer modeller için baseline oluşturur.*
3.  **K-Fold Cross Validation (5-Fold)**
    * Model farklı veri bölünmelerinde test edilmiştir.
    * ➡️ *Daha güvenilir performans ölçümü sağlar.*
4.  **Evaluation Metrics**
    * Aşağıdaki metrikler kullanılmıştır:
        * `MAE` (Mean Absolute Error)
        * `RMSE` (Root Mean Squared Error)
        * `R² Score`
    * ➡️ *Model performansını farklı açılardan değerlendirmek için kullanılmıştır.*

---

### 📊 Model Sonuçları

| Model | MAE | RMSE | R² |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | `0.0883` | `0.1260` | `0.9149` |
| **Linear Regression (CV)** | `0.0889` | `0.1496` | `0.8435` |

---

### 📌 Sonuç Analizi
* **Linear Regression** modeli validation setinde yüksek **R² (~0.91)** elde etmiştir.
* Cross-validation sonucunda performans biraz düşmüştür **(R² ~0.84)**.
* Bu durum modelin bazı veri bölünmelerine duyarlı olabileceğini gösterir.
* ➡️ Bu nedenle daha güçlü modellerle karşılaştırma yapılması gereklidir.

---

### 🚀 Sonraki Adımlar
Bu baseline modelden sonra:
* `CatBoost` modeli eklenecek.
* `FT-Transformer` modeli kurulacak.
* Tüm modeller karşılaştırılacak.

**Amaç:** Tabular veri için klasik ve modern yöntemlerin performans karşılaştırması.

---

### 📦 Kullanılan Teknolojiler
* `Python`
* `Pandas`
* `NumPy`
* `Scikit-learn`
