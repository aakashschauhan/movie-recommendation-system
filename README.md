# 🎬 Movie Recommendation System  

An AI-powered **Movie Recommendation System** built with **Python, Streamlit, and TMDB API**.  
The system recommends 5 similar movies based on content similarity (cosine similarity of movie metadata).  

🔗 **Live Demo**: [Streamlit App](https://movie-recommendation-system-aakash.streamlit.app/)  
📂 **Dataset**: Movies metadata and similarity matrix stored externally via Google Drive.  

---

## 🚀 Features  
- Recommends **5 similar movies** based on the selected movie.  
- Fetches **movie posters dynamically** from TMDB API.  
- Interactive **Streamlit UI** with movie thumbnails.  
- Uses **Cosine Similarity** on preprocessed tags for recommendations.  
- Lightweight deployment (large `.pkl` files excluded from repo).  

---

## 🛠️ Tech Stack  
- **Frontend**: [Streamlit](https://streamlit.io)  
- **Backend**: Python  
- **Libraries**: Pandas, NumPy, Scikit-learn, Pickle, Requests, gdown  
- **API**: [TMDB API](https://www.themoviedb.org/documentation/api)  
- **Deployment**: Streamlit Cloud  

---

## 📂 Project Structure  
```
movie-recommendation-system/
│
├── app.py                # Main Streamlit app
├── requirements.txt      # Dependencies
├── .gitignore            # Ignore large files (movies.pkl, similarity.pkl)
└── README.md             # Project documentation
```

---

## ⚡ Setup Instructions  

### 1️⃣ Clone Repository  
```bash
git clone https://github.com/aakashschauhan/movie-recommendation-system.git
cd movie-recommendation-system
```

### 2️⃣ Install Dependencies  
```bash
pip install -r requirements.txt
```

### 3️⃣ Add API Key  
Create a `.streamlit/secrets.toml` file locally:  
```toml
TMDB_API_KEY = "your_tmdb_api_key_here"
```

### 4️⃣ Download Pickle Files  
`movies.pkl` and `similarity.pkl` are stored in Google Drive and automatically downloaded using **gdown** at runtime.  
No manual action needed 🚀  

### 5️⃣ Run Locally  
```bash
streamlit run app.py
```

---

## 🌍 Deployment on Streamlit Cloud  
1. Push your repo to GitHub.  
2. Go to [Streamlit Cloud](https://share.streamlit.io).  
3. Connect your GitHub repo.  
4. Set `TMDB_API_KEY` in **App Secrets**.  
5. Deploy → Your app goes live 🎉  

---

## 🧠 How It Works  

1. **Data Preprocessing**  
   - Movie metadata is collected (title, genres, keywords, overview, cast, crew).  
   - A combined **tags** column is created.  

2. **Text Vectorization**  
   - Tags are converted into vectors using **CountVectorizer**.  

3. **Cosine Similarity**  
   - Pairwise cosine similarity is calculated between all movies.  
   - For a selected movie, top 5 most similar movies are chosen.  

4. **TMDB API Integration**  
   - Movie posters and details are fetched dynamically from TMDB API.  

---


## 🤝 Contributing  
Pull requests are welcome! For major changes, open an issue first to discuss.  

---

## 📜 License  
This project is open source under the [MIT License](LICENSE).  
