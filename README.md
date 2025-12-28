LLm Destekli Akademik Asistan Ajanı (Llama-3)
Bu proje, akademik dökümanların (PDF) ve ders materyallerinin analizini otomatize eden bir yapay zeka asistanıdır.

Teknik Özellikler ve Optimizasyon

Dil Modeli: Llama-3-8B-Instruct.
Kuantizasyon: 4-bit NormalFloat4 (NF4) ile VRAM kullanımı %75-80 oranında azaltılmıştır.
Mimari: LangChain v0.3 modüler yapısı ve LCEL (LangChain Expression Language) kullanılarak şeffaf bir veri akışı sağlanmıştır.
Vektör Veritabanı: ChromaDB (L2 mesafesi metriği ile anlamsal benzerlik araması).
Embedding: Sentence-BERT (SBERT) ile 384 boyutlu yoğun vektör dönüşümü.
Arayüz: Gradio Web UI

Performans Verileri (Nicel Değerlendirme)

Doğruluk: 10 farklı teknik sorguda %90 başarı oranı.
Hız: NVIDIA T4 GPU üzerinde ortalama 4.5 - 12 saniye yanıt süresi.
F1 Skoru: Döküman içeriğiyle 0.85 anlamsal örtüşme skoru.
Kapsam: 9 ders slaytı ve 5 akademik makale (Transformer, RAG, GPT-3, Llama-3, ReAct).
Arayüz Erişimi
Google Colab üzerinde NVIDIA T4 GPU desteğiyle dinamik bir Gradio arayüzü üzerinden sunulmaktadır. Colab oturumları geçici olduğundan canlı linkler değişkenlik gösterebilir. Ancak proje mimarisi, modelin CPU üzerinde de optimize çalışabileceği şekilde (Kuantizasyon destekli) tasarlanmıştır. Gelecek çalışmalar kapsamında, sistemin Hugging Face Spaces platformuna taşınarak 7/24 kalıcı erişime açılması ve akademik camianın kullanımına sunulması hedeflenmektedir.
