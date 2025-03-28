# video-streaming-backend
A RESTful API backend built with Node.js, Express.js, and MongoDB for a YouTube-like video streaming application. Supports video uploads, user authentication, comments, likes, trending videos, and playlist management.

---

This API supports:

- **Video Uploads** (File uploads using Multer)
- **Trending Videos** (Trending algorithm implementation)
- **Likes & Dislikes** (User interactions)
- **Comments System** (Adding and managing comments)
- **Playlists** (Users can create video playlists)
- **Session-based Authentication** (User authentication using Express sessions)

---

## Installation

### Clone the Repository:
```bash
git clone https://github.com/aliGorgel/video-streaming-backend.git
cd video-streaming-backend
```

### Install Dependencies:
```bash
npm install
```

### Create a `.env` file and Add the Following Variables:
```plaintext
PORT=...
MONGO_URI=...
SESSION_SECRET=...
```

### Start the Server:
```bash
npm start
```

---

## API Endpoints

### Authentication (Auth)
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/auth/signup` | Register a new user |
| POST | `/auth/login` | User login |
| POST | `/auth/logout` | User logout |
| POST | `/auth/forgot-password` | Request a password reset |
| POST | `/auth/reset-password` | Reset password with token |

---

### User Management
| Method | Endpoint | Description |
|--------|---------|-------------|
| GET | `/user/profile` | Retrieve user profile details |
| PUT | `/user/update-user` | Update username and password |
| PUT | `/user/update-role` | Change user role (admin, premium, etc.) |
| POST | `/user/upload-profile` | Upload or update profile image |

---

### Video Management
| Method | Endpoint | Description |
|--------|---------|-------------|
| GET | `/videos/all` | Fetch all videos |
| GET | `/videos/:id` | Get video by ID |
| GET | `/videos/trends` | Get trending videos (pagination supported) |
| GET | `/videos` | Get videos by category (params: `page`, `category`) |
| POST | `/videos/` | Upload a new video |
| POST | `/videos/like-video/:id` | Like a video |
| POST | `/videos/dislike-video/:id` | Dislike a video |
| POST | `/videos/increment-view-count/:id` | Increment video view count |
| DELETE | `/videos/:id` | Delete a video by ID |

---

### Playlists
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/playlists` | Create a new playlist |
| POST | `/playlists/:playlistId/:videoId` | Add a video to a playlist |
| PUT | `/playlists/:id` | Update playlist name |
| GET | `/playlists/:id` | Get playlist by ID |
| GET | `/playlists` | Fetch all playlists |
| DELETE | `/playlists/:playlistId/:videoId` | Remove a video from a playlist |
| DELETE | `/playlists/:id` | Delete a playlist |

---

### Comments
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/comments` | Add a comment to a video |
| DELETE | `/comments/:id` | Delete a comment by ID |
| GET | `/comments/:id` | Get all comments for a video |

---

## Technologies Used
- **Node.js** (Backend runtime environment)
- **Express.js** (RESTful API framework)
- **MongoDB** (Database)
- **Multer** (File uploading middleware)
- **Express-Session** (Session-based authentication)
- **Mongoose** (MongoDB Object Data Modeling)

---

## License
This project is licensed under the **MIT License**.

---

## Contributing
Feel free to fork this repository, submit issues, or make pull requests to enhance the project!


