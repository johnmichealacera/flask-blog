# Flask Blog Application

A simple Flask web application with modern UI components built using Tailwind CSS and Flowbite.

## Features

- **Modern UI**: Clean and responsive design using Tailwind CSS
- **Component Library**: Integration with Flowbite for pre-built UI components
- **Multiple Pages**: Home page and form page with different layouts
- **Responsive Design**: Mobile-friendly interface
- **404 Error Page**: Custom error handling with styled 404 page

## Project Structure

```
flask-blog/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── tailwind.config.js     # Tailwind CSS configuration
├── templates/            # HTML templates
│   ├── index.html        # Home page template
│   └── form.html         # Form page template
└── static/              # Static assets
    ├── dist/            # Compiled CSS (Tailwind output)
    └── src/             # Source files
```

## Technologies Used

- **Backend**: Flask 3.0.2
- **Frontend**: Tailwind CSS with Flowbite components
- **Server**: Gunicorn (for production)
- **Styling**: Custom CSS compiled from Tailwind

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd flask-blog
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Install Node.js dependencies** (for Tailwind CSS)
   ```bash
   npm install
   ```

5. **Build Tailwind CSS**
   ```bash
   npm run build  # or npx tailwindcss -i ./static/src/input.css -o ./static/dist/css/output.css --watch
   ```

## Running the Application

### Development Mode
```bash
python app.py
```

The application will be available at `http://localhost:5000`

### Production Mode
```bash
gunicorn app:app
```

## Available Routes

- `/` or `/index` - Home page with navigation and 404 error styling
- `/form` - Form page with login form and card components

## Development

### Tailwind CSS Setup

The project uses Tailwind CSS with Flowbite components. To modify styles:

1. Edit CSS files in `static/src/`
2. Run the Tailwind build command to compile changes
3. The compiled CSS will be available in `static/dist/css/output.css`

### Adding New Pages

1. Create a new HTML template in the `templates/` directory
2. Add a new route in `app.py`
3. Use the existing Tailwind classes and Flowbite components for consistency

## Dependencies

- **Flask 3.0.2**: Web framework
- **Werkzeug 3.0.1**: WSGI utilities
- **Gunicorn**: WSGI HTTP server for production

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test the application
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Future Enhancements

- Add database integration for blog posts
- Implement user authentication
- Add blog post creation and editing functionality
- Include comment system
- Add search functionality
- Implement pagination for blog posts
