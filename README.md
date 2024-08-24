# Video/Audio Downloader App

This is a simple web application that allows users to download videos or extract audio from YouTube links. The app is built using Node.js, Express, and front-end technologies like HTML, CSS, and Bootstrap.

## Features

- **Video Downloading:** Users can download videos in various resolutions (e.g., 144p, 240p, 360p, 720p, 1080p).
- **Audio Extraction:** Users can extract and download audio in MP3 format from video links.
- **Responsive Design:** The UI is fully responsive, providing an optimal viewing experience on any device.

## Directory Structure

video-downloader-app/
│
├── backend/
│   ├── routes/
│   │   └── download.js           # API route handling video/audio downloading
│   ├── app.js                    # Express app setup and server configuration
│   ├── package.json              # Node.js project configuration and dependencies
│   └── package-lock.json         # Auto-generated file for locking dependency versions
│
├── frontend/
│   └── index.html                # Frontend HTML file with the app's user interface
│
└── README.md                     # Project documentation

## Prerequisites

- **Node.js** (v14 or later)
- **npm** (v6 or later)

## Getting Started

### 1. Clone the Repository

git clone https://github.com/your-username/video-downloader-app.git
cd video-downloader-app

### 2. Install Dependencies

Navigate to the `backend/` directory and install the necessary dependencies:

cd backend
npm install

### 3. Run the Application

Start the backend server:


node app.js

The server will start on `http://localhost:5000`.

### 4. Access the Application

Open your browser and go to `http://localhost:5000` to use the app.

## API Documentation

### POST `/api/download/video`

**Description:** Downloads a video or extracts audio from a given YouTube URL based on the selected format.

**Request Body:**

- `url` (string): The YouTube video URL.
- `format` (string): The desired format for download. Options include video resolutions (`144p`, `240p`, `360p`, `720p`, `1080p`) and `audioonly` for MP3 extraction.

**Example Request:**

{
  "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "format": "360p"
}

**Response:**

- **Success:** Streams the requested video or audio file as a downloadable attachment.
- **Error:** Returns a JSON error message if the URL is invalid or the download fails.

**Example Error Response:**


{
  "error": "Invalid URL"
}


## Frontend Structure

- **HTML/CSS:** The frontend is built with a simple structure using Bootstrap for responsiveness.
- **JavaScript:** Handles form submissions and triggers API requests to the backend.

### Key UI Elements:

- **Video/Audio Downloader:** Header of the app.
- **Input Field:** Users can paste the video URL here.
- **Format Dropdown:** A dropdown to select the video format or audio extraction.
- **Clear Button:** Clears the input field.
- **Download Buttons:** Two buttons to download the video or extract audio.

## Technologies Used

- **Frontend:** HTML, CSS, Bootstrap
- **Backend:** Node.js, Express, `ytdl-core`, `ffmpeg-static`, `fluent-ffmpeg`

## Future Enhancements

- **Multiple Platform Support:** Extend support to other video platforms like Vimeo, Dailymotion, etc.
- **User Authentication:** Add user login and save download history.
- **Progress Indicator:** Show download progress to the user.
- **Advanced Error Handling:** Improve error messages and validation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue if you have any suggestions or improvements.

## Contact

For any questions or inquiries, please contact [your-email@example.com].


### Customization
- **Clone URL:** Replace the GitHub repository URL with your own.
- **Contact Information:** Add your email address.
- **License:** If you choose a different license, update the License section accordingly.

This README should give clear instructions to anyone who wants to understand, use, or contribute to your project. Let me know if you need any changes!