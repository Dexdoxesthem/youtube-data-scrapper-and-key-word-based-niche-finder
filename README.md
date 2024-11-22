# youtube-data-scrapper-and-key-word-based-niche-finder
# YouTube Comment Analysis Tool

This project uses the YouTube Data API to fetch and analyze comments from multiple YouTube videos. It includes features to identify specific types of commenters (e.g., senior students) based on keywords and visualize the results in a bar chart.

---

## **Features**
- Fetch comments from multiple YouTube videos using their video IDs.
- Identify comments based on specific keywords to filter targeted users (e.g., senior students).
- Generate a DataFrame for easy analysis of comments and authors.
- Visualize top commenters using a bar chart.

---

## **Requirements**
### **1. Python Libraries**
Install the required libraries using pip:
```bash
pip install google-api-python-client pandas matplotlib seaborn
```

### **2. YouTube API Key**
- Obtain an API key from the [Google Cloud Console](https://console.cloud.google.com/).
- Enable the **YouTube Data API v3** for your project.

---

## **How to Use**
### **1. Clone or Download the Repository**
Clone the repository using:
```bash
git clone https://github.com/<your-username>/YouTube-Comment-Analysis.git
cd YouTube-Comment-Analysis
```

### **2. Set Your YouTube API Key**
Replace the `api_key` variable in the script with your YouTube API key:
```python
api_key = "YOUR_API_KEY_HERE"
```

### **3. Add Video IDs**
Replace the `video_ids` list with the YouTube video IDs you want to analyze:
```python
video_ids = ["VIDEO_ID1", "VIDEO_ID2", "VIDEO_ID3"]
```

### **4. Run the Script**
Run the script to fetch comments, filter them by keywords, and visualize the results:
```bash
python main.py
```

---

## **How the Code Works**
### **1. Fetch Comments**
- The script uses the `commentThreads` endpoint of the YouTube Data API to fetch comments for each video in the `video_ids` list.

### **2. Identify Specific Comments**
- A predefined list of keywords is used to filter comments matching specific criteria (e.g., senior students asking about advanced topics).

### **3. Visualization**
- The script generates a bar chart showing the top 10 commenters based on the filtered data.

---

## **Example Output**
### **Console Output**
Displays the first few rows of fetched comments:
```
              author                             comment  is_senior_student
0      John Doe           Please upload another video!                 True
1  Jane Smith           I loved this advanced math topic!                 True
2   Random User         Great video on audit basics!                      True
```

### **Bar Chart**
A bar chart visualizing the top commenters:
- X-axis: Author names
- Y-axis: Number of comments

---

## **Error Handling**
- The script skips videos with errors (e.g., comments disabled or private videos) and logs the issue for each video.
- If no comments are fetched, the script exits gracefully with a message.

---

## **Future Improvements**
- Add support for more complex filtering (e.g., sentiment analysis of comments).
- Include time-based trends in comments to track engagement over time.
- Extend functionality to analyze video metadata (e.g., likes, views, and upload date).

---

## **Contributing**
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Acknowledgments**
- [Google Developers](https://developers.google.com/) for the YouTube Data API documentation.
- Python community for the incredible libraries used in this project.

---

Feel free to reach out with suggestions, issues, or feedback. 😊
