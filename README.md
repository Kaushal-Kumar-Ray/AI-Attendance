# AI-Attendance
A web-based AI Attendance System that uses face recognition (LBPH) to automatically register students and mark attendance in real time.
The system provides a browser-based interface, live webcam capture, automatic model training, and admin-style dashboards for attendance monitoring.

📌 Key Features

🎥 Web-based Face Registration

Register students using browser webcam

Automatic face capture (30 samples per student)

Dataset generated dynamically

🧠 Face Recognition using OpenCV (LBPH)

Local model training

Reliable for small-to-medium datasets

Optimized for low-resource systems

🕒 Automatic Attendance Marking

Real-time face recognition

Attendance marked once per day

Prevents duplicate entries

📊 Admin Dashboard

Total students

Present today

Absent today

Live updates via LAN

👥 Students Page

Present / Absent status

Clean tabular view

📋 Attendance Records

Full attendance history

CSV download support

🌐 LAN Demo Support

Dashboard accessible from multiple devices on same network

No internet or cloud required

🛠️ Tech Stack
Layer	Technology
Backend	Python, Flask
AI / ML	OpenCV (LBPH Face Recognizer)
Frontend	HTML, CSS, JavaScript
Data Storage	CSV files + local folders
Camera Access	Browser getUserMedia()
OS	Linux (Ubuntu)
📁 Project Structure
AI_Attendance/
├── backend/
│   ├── app.py            # Flask web application
│   └── train.py          # Face recognition training script
│
├── templates/
│   ├── base.html
│   ├── home.html
│   ├── register.html
│   ├── attendance.html
│   ├── students.html
│   └── records.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── register.js
│       └── attendance.js
│
├── dataset/              # Captured face images
├── trainer/              # Trained model files
│   ├── face_trainer.yml
│   └── labels.pkl
│
├── students.csv
├── attendance.csv
└── README.md

⚙️ Setup Instructions
1️⃣ Create Virtual Environment
python3 -m venv ~/envs/ml
source ~/envs/ml/bin/activate

2️⃣ Install Dependencies
pip install opencv-contrib-python flask numpy


⚠️ opencv-contrib-python is required for cv2.face.LBPHFaceRecognizer

▶️ Run the Application
python backend/app.py


Open in browser:

http://127.0.0.1:5000

🧪 How to Use
🔹 Register Student

Go to Register page

Enter Student ID and Name

Start camera capture

Capture completes automatically

Click Save & Train Model

🔹 Mark Attendance

Go to Attendance page

Look at the camera

Attendance is marked automatically

🔹 View Records

Students Page → Present / Absent status

Records Page → Full attendance history

Download CSV if required

🌐 LAN Demo Mode

Run Flask in LAN mode:

app.run(host="0.0.0.0", port=5000, debug=True)


Access from another device (same Wi-Fi):

http://<your-ip>:5000


📌 Camera access works only on localhost due to browser security policies.
Other devices can view dashboards and records.

🧠 Design Notes

Training is decoupled from runtime recognition

Model retraining is required when:

new student is added

student ID or name is changed

CSV files are treated as registries with defensive parsing

No cloud dependency — fully local system

🎓 Academic Relevance

This project demonstrates:

Practical application of Computer Vision

ML lifecycle (data → training → inference)

Web-based system integration

Real-world software design principles

Suitable for:

Minor / Major Projects

AI & ML coursework

Computer Vision demonstrations

🚀 Future Enhancements

Admin login system

Model status indicator

Attendance analytics & charts

Cloud deployment (optional)

Face embedding-based recognition

👨‍💻 Author

Kaushal Kumar Ray
B.Tech CSE (AI & ML)
Minor Project – Semester IV
