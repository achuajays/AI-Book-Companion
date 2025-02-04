# 📚 AI Book Companion

AI Book Companion is an intelligent book recommendation system that combines the power of Google Play Books search with AI-powered personalized recommendations. Built with Streamlit, it offers an intuitive interface for discovering books tailored to your preferences.

![AI Book Companion](banner.png)

## 🌟 Features

- **Smart Search**: Search through millions of books from Google Play Books
- **AI-Powered Recommendations**: Get personalized book suggestions based on your preferences
- **Rich Book Information**: View detailed book information including:
  - Title and Author
  - Price and Rating
  - Category
  - Description
  - Cover Image
  - Direct links to Google Play Books
- **User-Friendly Interface**: Clean, responsive design with easy navigation
- **Docker Support**: Easy deployment using Docker

## 🚀 Quick Start

### Using Docker

1. Clone the repository:
```bash
git clone https://github.com/achuajays/AI-Book-Companion.git
cd AI-Book-Companion
```

2. Build the Docker image:
```bash
docker build --tag ai_book_companion:latest .
```

3. Run the container:
```bash
docker run -d --name ai_book_companion -p 8501:8501 ai_book_companion:latest
```

4. Access the application at `http://localhost:8501`

### Manual Installation

1. Clone the repository:
```bash
git clone https://github.com/achuajays/AI-Book-Companion.git
cd AI-Book-Companion
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the project root with:
```
SERPAPI_KEY=your_serpapi_key
GROQ=your_groq_api_key
```

5. Run the application:
```bash
streamlit run app.py
```


```

## 🔧 Configuration

The application uses two main API services:

1. **SerpAPI**: For fetching book data from Google Play Books
2. **Groq AI**: For generating personalized book recommendations

You'll need to obtain API keys from both services:
- SerpAPI: [Get API Key](https://serpapi.com/)
- Groq: [Get API Key](https://console.groq.com/)

## 🎯 Usage

1. Enter your book search query in the sidebar
2. (Optional) Provide your preferences for personalized recommendations
3. Click "Search Books" to see results
4. Browse through the book cards
5. Click on book titles to visit their Google Play Books page
6. Expand descriptions to read more about each book

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔍 Troubleshooting

### Common Issues

1. **API Keys Not Working**
   - Verify your API keys are correctly set in the `.env` file
   - Check if you have remaining API credits

2. **Docker Container Issues**
   - Ensure port 8501 is not in use
   - Check Docker logs: `docker logs ai_book_companion`

3. **Search Not Returning Results**
   - Verify your internet connection
   - Check if SerpAPI is operational
   - Try different search terms

### Docker Commands

```bash
# Stop container
docker stop ai_book_companion

# Remove container
docker rm ai_book_companion

# View logs
docker logs ai_book_companion

# Access container shell
docker exec -it ai_book_companion /bin/bash
```

## 📞 Support

For support, please:
1. Check the [Issues](https://github.com/achuajays/AI-Book-Companion/issues) page
2. Create a new issue if your problem isn't already listed
3. Include relevant details:
   - Error messages
   - Steps to reproduce
   - Environment details

## 🙏 Acknowledgments

- [Streamlit](https://streamlit.io/) for the web framework
- [SerpAPI](https://serpapi.com/) for Google Play Books data
- [Groq](https://groq.com/) for AI recommendations

## 🔮 Future Improvements

- Add user authentication
- Implement book lists/collections
- Add more book sources
- Enhance AI recommendations
- Add social sharing features
- Implement caching for faster results
