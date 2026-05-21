# Evaluasi Model LSTM dan BERT untuk Klasifikasi Emosi pada Dataset GoEmotions

Penelitian ini membandingkan performa model deep learning berbasis sequential dan transformer untuk tugas klasifikasi emosi pada teks menggunakan dataset GoEmotions. Model yang digunakan adalah Long Short-Term Memory (LSTM) dan Bidirectional Encoder Representations from Transformers (BERT).


## Dataset

Dataset yang digunakan adalah GoEmotions dari Google Research yang berisi berbagai kategori emosi pada teks berbahasa Inggris.

Pada penelitian ini, label emosi dipetakan ke dalam kategori emosi Ekman:

- Anger
- Disgust
- Fear
- Joy
- Sadness
- Surprise

Dataset dibagi menggunakan rasio bawaan GoEmotions:

- Train: ~80%
- Validation: ~10%
- Test: ~10%


## Preprocessing

Tahap preprocessing meliputi:

- Pembersihan teks
- Tokenisasi teks
- Pemetaan label GoEmotions ke kategori Ekman
- Konversi label menjadi multi-label vector
- Padding sequence untuk model LSTM


## Model Architecture

### LSTM

Model LSTM menggunakan embedding layer untuk merepresentasikan kata menjadi vektor numerik sebelum diproses secara sequential oleh layer LSTM. Output model diteruskan ke fully connected layer untuk menghasilkan prediksi probabilitas emosi.

### BERT

Model BERT menggunakan pre-trained transformer encoder dengan mekanisme self-attention untuk memahami konteks kata dalam kalimat secara dua arah sebelum menghasilkan prediksi klasifikasi emosi.


## Evaluation Metrics

Evaluasi model dilakukan menggunakan:

- Micro F1-score
- Macro F1-score
- Accuracy
- Exact Match Accuracy


## Results

| Metric | LSTM | BERT |
|---|---|---|
| Micro F1-score | 0.3567 | 0.7747 |
| Macro F1-score | 0.1685 | 0.6742 |
| Accuracy | 0.5712 | 0.9230 |
| Exact Match Accuracy | 0.0000 | 0.7520 |


## Conclusion

Hasil penelitian menunjukkan bahwa model BERT memberikan performa yang lebih baik dibandingkan model LSTM pada seluruh metrik evaluasi. Kemampuan contextual understanding dan self-attention pada BERT membantu model memahami hubungan antar kata secara lebih efektif dibandingkan model sequential tradisional seperti LSTM.


## Technologies Used

- Python
- PyTorch
- HuggingFace Transformers
- Scikit-learn
- Pandas
- NumPy
- Google Colab


## References

- GoEmotions Dataset (Google Research)
- BERT (Devlin et al., 2019)
- LSTM (Hochreiter & Schmidhuber, 1997)
- Transformer Architecture (Vaswani et al., 2017)


## MODELS and DATASET

[MODELS](https://drive.google.com/drive/folders/1DKtl6zllHkU5Vy56r2MLcxZXSbQu4-1G?usp=sharing)
[DATASET](https://drive.google.com/drive/folders/1DKtl6zllHkU5Vy56r2MLcxZXSbQu4-1G?usp=sharing](https://www.kaggle.com/datasets/debarshichanda/goemotions).
