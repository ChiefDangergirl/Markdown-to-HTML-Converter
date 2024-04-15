# FastAPI Markdown Converter

This is a FastAPI application that provides an endpoint for converting Markdown files to HTML and saving them as static pages. It also allows access to the saved static pages through another endpoint.

## Setup
### Clone the repository:

`git clone https://github.com/youruse`

### Navigate to the project directory:

`cd fastapi-markdown-converter`

### Install the required dependencies:

`pip install -r requirements.txt`

### Set up the environment variables:

    - Create a .env file in the root directory of the project.
    - Add the following line to the .env file, replacing your-api-key with your desired API key:

    `API_KEY=your-api-key`

### Start the FastAPI server:

`uvicorn main:app --reload`

# Usage
## Upload Markdown File

To convert a Markdown file to HTML and save it as a static page, send a POST request to the /upload_markdown/ endpoint with the Markdown file as form data and the API key as a header.

Example using curl:

`curl -X POST -H "X-API-Key: your-api-key" -F "file=@/path/to/your/markdown-file.md" http://localhost:8000/upload_markdown/`

## Access Static Page

To access a saved static page, use the /static/{file_name} endpoint, where {file_name} is the name of the saved HTML file.

Example:

`http://localhost:8000/static/your-file-name.html`

## API Documentation

After starting the FastAPI server, you can access the API documentation and test the endpoints using Swagger UI at:
`http://localhost:8000/docs`

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.