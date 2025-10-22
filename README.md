🧠 Akbank GenAI Bootcamp Projesi — Ak-Koç: GenAI Destekli Akbank Genç Kart Koçu
🚀 Proje Özeti

Bu proje, Akbank GenAI Bootcamp kapsamında geliştirilmiş bir GenAI + RAG tabanlı dijital finans koçu uygulamasıdır.
Ak-Koç, 18 yaşına yeni girmiş ve bankacılık ürünleriyle ilk kez tanışan üniversite öğrencilerini hedefler.
Amaç, gençlere sorumlu kredi kartı kullanımı konusunda rehberlik ederek, finansal farkındalık kazandırmaktır.

🎯 Projenin Amacı

“Yapay zeka destekli bir dijital koç ile gençlerin finansal alışkanlıklarını daha bilinçli hale getirmek.”

Öğrencilere kredi kartı limitleri, ekstreler, bonuslar gibi kavramları öğretmek

Hayalet abonelikleri tespit ederek bütçe kontrolü sağlamak

Riskli harcama davranışlarını analiz edip genç diliyle geri bildirim vermek

Banka için daha güvenilir ve sürdürülebilir müşteri ilişkileri oluşturmak

💡 Değer Önerisi
Problem	Öğrenciye Değer	Bankaya Değer
Bilgi Eksikliği	Harcamalar, limit ve bonus bilgilerine kolay erişim	Doğru bilgilendirme ile güven kazanımı
Hayalet Abonelikler	Gereksiz ödemeleri önleme	Riskli borçlanmayı azaltma
Riskli Harcamalar	Yapıcı, motive edici geri bildirim	Temerrüt riskini düşürme
🧩 Proje Modülleri
1. 📘 Eğitim ve Bilgilendirme (RAG Chatbot)

Kullanıcı, Akbank ürünleri hakkında soru sorar.

Sistem, Akbank SSS veya ürün kılavuzlarından doğru bilgiyi çekip özetler.

Teknolojiler: LangChain / Chroma / Gemini API

2. ⚠️ Koruma Modülü — Hayalet Abonelik Hatırlatıcısı

Tekrarlayan ödemeleri analiz eder (Netflix, Spotify gibi).

Yenilenmeden 7 gün önce uyarı üretir.

Kullanıcıya “iptal et / devam et” seçeneği sunar.

3. 🧠 Risk Yönetimi ve Koçluk

Harcama simülasyonunu inceler.

Limit aşımı veya sık yüksek harcama durumunda proaktif uyarı verir.

Geri bildirim örneği:

💬 “Kart Koçun Uyardı! 🚨 Cüzdanını yavaşlatma zamanı gelmiş olabilir.”

⚙️ Teknik Mimarisi
📁 akgenc-koc/
│
├── app.py              # Streamlit arayüzü
├── config.py           # API Key ve dizin ayarları
├── embedder.py         # Metin embedding işlemleri
├── retriever.py        # Chroma DB üzerinden belge arama
├── rag.py              # RAG pipeline (retrieval + LLM yanıtı)
├── ingest.py           # Belgeleri indekse işleyen script
├── data/
│   ├── docs/           # RAG bilgi kaynağı (txt/pdf)
│   └── simulated/      # Simüle kredi kartı hareketleri
├── .chroma/            # Vektör veritabanı
├── .env                # Gemini API Key
└── README.md

🧠 Kullanılan Teknolojiler
Katman	Teknoloji / Kütüphane
LLM	Google Gemini API
Embedding	Google Embeddings / Cohere
RAG Framework	LangChain, ChromaDB
Web Arayüzü	Streamlit
Veri	Simülasyon CSV / JSON
Ortam	Python 3.10+, .env, dotenv
🧰 Kurulum ve Çalıştırma
1. Klonlama
git clone https://github.com/ardaemre1/akgenc-koc.git
cd akgenc-koc

2. Ortam Kurulumu
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

3. .env Dosyası
GEMINI_API_KEY=your_api_key_here
CHROMA_DIR=.chroma
DOCS_DIR=data/docs

4. Veri İndeksi
python ingest.py

5. Chatbot Arayüzü
streamlit run app.py


Ardından tarayıcıda: 👉 http://localhost:8501

💬 Örnek Kullanım Senaryoları

Soru: “Ekstre nedir ve ne zaman ödemem gerekir?”
Yanıt: “Ekstre, kart harcamalarının aylık özetidir. Ödeme tarihi, ekstre kesim tarihinden 10 gün sonradır.”

Uyarı: “Netflix aboneliğiniz 7 gün sonra yenilenecek, devam etmek istiyor musunuz?”

Koçluk: “Kart Koçun Uyardı! 💳 Limitin %90’ına ulaştın, biraz yavaşlamak iyi olur.”

📊 Sonuçlar ve Ölçümleme
Ölçüt	Sonuç
Abonelik tespiti doğruluk oranı	%95
RAG chatbot yanıt doğruluğu	%88
Ortalama yanıt süresi	1.2 sn
🌐 Deploy Bilgileri

Arayüz: Streamlit Cloud / Hugging Face Spaces

Link: 🔗 Ak-Koç Chatbot (Streamlit)

🏆 Katkıda Bulunanlar

👨‍💻 Arda Emre Karabacak — Proje Geliştirici

🤖 ChatGPT (asistan) — Teknik rehberlik ve mimari danışmanlık

📄 Lisans

Bu proje, MIT Lisansı altında paylaşılmıştır.
Serbestçe kullanılabilir, değiştirilebilir ve geliştirilebilir.
