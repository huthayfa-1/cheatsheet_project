# Tech Cheatsheet

A modern, feature-rich Django web application for creating and managing technical cheatsheets with an intuitive VS Code-inspired interface.

![Django](https://img.shields.io/badge/Django-4.2.25-green.svg)
![Python](https://img.shields.io/badge/Python-3.13-blue.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Features

### 🎯 Core Functionality
- **Topic Management**: Create and organize cheatsheets by topics
- **Flashcard System**: Each entry has a summary (front) and detailed content (back) with 3D flip animation
- **Markdown Support**: Write notes with full Markdown syntax including:
  - Code syntax highlighting (via Highlight.js)
  - Mathematical equations (via KaTeX)
  - Diagrams (via Mermaid)
- **User Authentication**: Secure registration and login system
- **Personal Workspace**: Each user has their own private cheatsheets

### 🎨 User Interface
- **VS Code-Style Layout**: 
  - Activity Bar (48px vertical icon bar)
  - Collapsible Sidebar with topic navigation
  - Main content area
- **Dark/Light Mode**: Theme toggle with localStorage persistence
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Keyboard Shortcuts**: 
  - `Ctrl+B` - Toggle sidebar
- **Immersive CSS**: Extensively commented styles for learning

### 🔧 Technical Features
- Clean, modular template architecture
- Context processors for global data
- CSS variables for theming
- Vanilla JavaScript (no heavy frameworks)
- Static file management
- SQLite database

## 📸 Screenshots

### Login Page
![Login](screenshots/login.png)

### Topic List
![Topic List](screenshots/topic_list.png)

### Entries List (Flashcards)
![Entries List](screenshots/Entries_list.png)

### Add Entry
![Add Entry](screenshots/add_entry.png)

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/huthayfa-1/cheatsheet_project.git
   cd cheatsheet_project
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Open your browser**
   Navigate to `http://127.0.0.1:8000/`

## 📁 Project Structure

```
cheatsheet_project/
├── config/                    # Project configuration
│   ├── settings.py           # Django settings
│   ├── urls.py               # URL configuration
│   └── context_processors.py # Custom context processors
├── sheets/                    # Main app
│   ├── models.py             # Topic and Entry models
│   ├── views.py              # View logic
│   ├── forms.py              # Entry and Topic forms
│   ├── urls.py               # App URLs
│   ├── static/
│   │   └── sheets/
│   │       └── styles.css    # Comprehensive stylesheet
│   ├── templates/
│   │   └── sheets/
│   │       ├── base.html     # Base template
│   │       ├── sidebar.html  # Modular sidebar
│   │       ├── topic_list.html
│   │       ├── topic_detail.html
│   │       └── ...           # Other templates
│   └── templatetags/
│       └── markdown_extras.py # Custom Markdown filter
├── users/                     # Authentication app
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── registration/
├── manage.py
├── requirements.txt
└── README.md
```

## 🎓 Usage

### Creating a Topic
1. Click "New Topic" in the sidebar
2. Enter a title for your topic
3. Click "Add Topic"

### Adding Entries (Flashcards)
1. Navigate to a topic
2. Click "Add New Entry"
3. Fill in:
   - **Title**: Entry name
   - **Summary**: Quick notes (shown on front of card)
   - **Content**: Detailed information (shown on back)
4. Use Markdown for formatting

### Markdown Examples

**Code blocks:**
\`\`\`python
def hello_world():
    print("Hello, World!")
\`\`\`

**Math equations:**
```
$E = mc^2$
$$\int_{0}^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}$$
```

**Mermaid diagrams:**
\`\`\`mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
\`\`\`

## 🎨 Customization

### Changing Theme Colors
Edit CSS variables in `sheets/static/sheets/styles.css`:

```css
:root {
    --primary: #4a9eff;
    --bg: #0b1220;
    /* ... more variables */
}
```

### Adding Activity Bar Icons
Edit `sheets/templates/sheets/base.html`:

```html
<button class="activity-bar-item" id="your-feature" aria-label="Feature">
    <span class="activity-icon">🔍</span>
</button>
```

## 🛠️ Technologies Used

- **Backend**: Django 4.2.25
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Database**: SQLite (development)
- **Markdown Processing**: Python Markdown, Bleach
- **Syntax Highlighting**: Highlight.js
- **Math Rendering**: KaTeX
- **Diagrams**: Mermaid.js

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👤 Author

**Huthayfa Abdulrauf Mohammad Derham**
- GitHub: [@huthayfa-1](https://github.com/huthayfa-1)

## 🙏 Acknowledgments

- Inspired by VS Code's interface design
- Built as a learning project for Django and modern web development

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

**Happy Learning! 📚**
