Pemrosesan Teks: iTunes API (Scraping, Preprocessing, Feature Engineering, Clustering)

Anggota
- Eifellyne Putri Widayanto (011)
- Vania Felicia Gita Wulandari (058)

Deskripsi

Satu notebook yang menjalankan alur pemrosesan teks dari awal sampai akhir pada judul lagu:

1. **Web scraping dan API:** Billboard Hot 100 (HTML) dan iTunes Search API (JSON, artis Taylor Swift).
2. **Text preprocessing:** hapus HTML, hashtag, URL, tanda baca, emoji; lowercase; stemming; hapus stopword.
3. **Feature engineering:** One Hot, Bag of Words, TF-IDF, Word2Vec (CBOW), FastText (Skip-Gram). Fitur dibuat dari 20 judul lagu iTunes.
4. **Text clustering:** KMeans dan Hierarchical (Ward) pada fitur TF-IDF, dilengkapi silhouette score, wordcloud tiap cluster, dan analisis.

Library: `requests`, `beautifulsoup4`, `pandas`, `nltk`, `scikit-learn`, `gensim`, `umap-learn`, `plotly`, `wordcloud`, `demoji`.

Hasil singkat

- Feature engineering: kosakata 42 kata, matriks sparse 94,64% berisi nol.
- Clustering (k = 4): silhouette sekitar 0,03 untuk KMeans maupun Hierarchical, artinya cluster hampir tidak terpisah. Judul yang berbagi kata (*Taylor's Version*) selalu mengelompok bersama.
- Keterbatasan: data hanya 20 judul pendek (1 sampai 4 kata), sehingga struktur topik tidak terbentuk jelas. Data teks yang lebih banyak dan lebih panjang akan memberi hasil yang lebih bermakna.
