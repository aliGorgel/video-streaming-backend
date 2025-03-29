# video-streaming-backend
This is a RESTful API backend project build with node.js express.js and mongoDB for a video streaming application.

---

This API supports:

- **Video Uploads**
- **Trending Videos**
- **Likes & Dislikes**
- **Comments System**
- **Playlists**
- **Session-based Authentication**

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
EMAIL_USER:...
EMAIL_PASSWORD:...
```

### Start the Server:
```bash
npm start
```

---

## API Endpoints

### Authentication
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
| DELETE | `/user/delete-user` | Delete user from database |

---

### Video Management
| Method | Endpoint | Description |
|--------|---------|-------------|
| GET | `/videos/all` | Fetch all videos |
| GET | `/videos/:videoId` | Get video by ID |
| GET | `/videos/trends` | Get trending videos (pagination supported) |
| GET | `/videos` | Get videos by category (params: `page`, `category`) |
| POST | `/videos/` | Upload a new video |
| POST | `/videos/like-video/:videoId` | Like a video |
| POST | `/videos/dislike-video/:videoId` | Dislike a video |
| POST | `/videos/increment-view-count/:videoId` | Increment video view count |
| DELETE | `/videos/:videoId` | Delete a video by ID |

---

### Playlist Management
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/playlists` | Create a new playlist |
| POST | `/playlists/:playlistId/:videoId` | Add a video to a playlist |
| PUT | `/playlists/:playlistId` | Update playlist name |
| GET | `/playlists/:playlistId` | Get playlist by ID |
| GET | `/playlists` | Fetch all playlists |
| DELETE | `/playlists/:playlistId/:videoId` | Remove a video from a playlist |
| DELETE | `/playlists/:playlistId` | Delete a playlist |

---

### Comment Management
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/comments` | Add a comment to a video |
| DELETE | `/comments/:id` | Delete a comment by ID |
| GET | `/comments/:id/:page` | Get all comments for a video |

---

## Technologies Used
- **Node.js**
- **Express.js**
- **MongoDB**
- **Multer**
- **Express-Session**
- **Mongoose**

---

## License
This project is licensed under the **MIT License**.

---

## Contributing
Feel free to fork this repository, submit issues, or make pull requests to enhance the project!


