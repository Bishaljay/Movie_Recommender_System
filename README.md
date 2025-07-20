# 🎬 Movie Recommender System

This is a simple **Content-Based Movie Recommender System** built with **Streamlit** and **Python**.

Given a movie you like, it recommends 5 similar movies and displays their posters using **The Movie Database (TMDb) API**.

---

## 🚀 Features

✅ Select a movie from a dropdown  
✅ Get 5 similar movie recommendations  
✅ View movie posters fetched dynamically from TMDb  
✅ Simple, interactive web app with **Streamlit**

---

## 📂 Project Structure

```

Movie\_Recommender\_System/
├── app.py                 # Streamlit application
├── movie\_list.pkl         # Pickled DataFrame with movie data
├── similarity.pkl         # Pickled similarity matrix
├── README.md              # Project readme (this file)

````

---

## 📊 Dataset
Got it!
Here’s your **📊 Dataset** section rewritten to match your **Movie Recommender System** instead of laptops:

---

## 📊 Dataset

The dataset contains information about various movies, including their titles, genres, overviews, keywords, cast, crew, and other metadata.
This information is used to build a **content-based recommender system** that suggests similar movies based on their features.

**Features include:**

* Title
* Genres
* Overview / Plot summary
* Keywords
* Cast & Crew information
* Movie ID (used to fetch posters from TMDb)
- Dataset source: [Github](https://github.com/Bishaljay/Movie_Recommender_System/blob/main/Datasets.zip)

## 🔧 Requirements

- Python 3.x  
- `streamlit`  
- `pandas`  
- `requests`  
- `pyngrok` (if running in Google Colab)  

Install them with:

```bash
pip install streamlit pandas requests pyngrok
````

---

## 🗝️ TMDb API

This app uses [The Movie Database (TMDb) API](https://www.themoviedb.org/documentation/api) to fetch movie posters.
Make sure you have a valid API key and replace it in `app.py`:

```python
api_key = "YOUR_TMDB_API_KEY"
```

---

## ✅ How to Run

**On your local machine:**

1. Clone the repo or download the files
2. Make sure `movie_list.pkl` and `similarity.pkl` are in the same folder as `app.py`
3. Open a terminal in the project directory
4. Run:

   ```bash
   streamlit run app.py
   ```
5. Open `http://localhost:8501` in your browser

---

**On Google Colab:**

To run in Colab, you must tunnel with `pyngrok`.
Example:

```python
!pip install streamlit pyngrok

from pyngrok import ngrok

# Replace with your ngrok auth token
ngrok.set_auth_token("YOUR_NGROK_AUTH_TOKEN")

!streamlit run app.py &

public_url = ngrok.connect(port=8501)
print(f"Your app is live at: {public_url}")
```

---

## 📌 Notes

* Make sure your pickled files (`movie_list.pkl`, `similarity.pkl`) are generated or provided.
* This project is for learning and demonstration.
* If you want to deploy it online, check out [Streamlit Community Cloud](https://streamlit.io/cloud).

---

## 🤝 Credits

* Built with [Streamlit](https://streamlit.io)
* Uses [TMDb API](https://www.themoviedb.org) for posters
