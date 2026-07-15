# 🌍 Travel Memory - MERN Stack Application Deployment on AWS

## 📖 Project Overview

Travel Memory is a full-stack MERN (MongoDB, Express.js, React.js, Node.js) application that enables users to create, manage, update, and share their travel experiences.

This project demonstrates the deployment of a MERN application on AWS using a highly available architecture with multiple EC2 instances, Application Load Balancers, Nginx Reverse Proxy, MongoDB Atlas, and Cloudflare DNS.

---

# 🚀 Features

* Create travel memories
* View all travel experiences
* Update existing memories
* Delete travel memories
* Responsive React frontend
* RESTful API backend
* MongoDB Atlas integration
* High Availability deployment
* Load Balancing using AWS ALB

---

# 🛠️ Technology Stack

## Frontend

* React.js
* JavaScript
* HTML5
* CSS3

## Backend

* Node.js
* Express.js

## Database

* MongoDB Atlas

## Cloud & DevOps

* Amazon EC2
* Application Load Balancer (ALB)
* Nginx Reverse Proxy
* Cloudflare DNS
* Git & GitHub

---

# 🏗️ AWS Architecture

```text
                    Internet
                        │
                 Cloudflare DNS
                        │
          ┌────────────────────────┐
          │ Frontend Load Balancer │
          └────────────────────────┘
                 │             │
        Frontend EC2     Frontend Replica

          ┌────────────────────────┐
          │ Backend Load Balancer  │
          └────────────────────────┘
                 │             │
         Backend EC2      Backend Replica
                 │
           MongoDB Atlas
```

---

# 📂 Project Structure

```text
TravelMemory/
│
├── backend/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── package.json
│   └── index.js
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── build/
│
├── snapshots/
├── README.md
└── LICENSE
```

---

# ⚙️ Backend Environment Variables

Create a `.env` file inside the **backend** folder.

```env
MONGO_URI=ENTER_YOUR_MONGODB_CONNECTION_STRING
PORT=3001
```

---

# ⚙️ Frontend Environment Variables

Create a `.env` file inside the **frontend** folder.

```env
REACT_APP_BACKEND_URL=http://localhost:3001
```

> **Note:** Update the backend URL according to your deployment. For AWS deployment, replace `localhost` with your backend Load Balancer DNS name or custom domain.

---

# 🗄️ Sample Data

Use the following JSON object to create a sample travel memory.

```json
{
  "tripName": "Incredible India",
  "startDateOfJourney": "19-03-2022",
  "endDateOfJourney": "27-03-2022",
  "nameOfHotels": "Hotel Namaste, Backpackers Club",
  "placesVisited": "Delhi, Kolkata, Chennai, Mumbai",
  "totalCost": 800000,
  "tripType": "leisure",
  "experience": "Lorem Ipsum...",
  "image": "https://t3.ftcdn.net/jpg/03/04/85/26/360_F_304852693_nSOn9KvUgafgvZ6wM0CNaULYUa7xXBkA.jpg",
  "shortDescription": "India is a wonderful country with rich culture and good people.",
  "featured": true
}
```

---

# ▶️ Running the Backend

```bash
cd backend
npm install
node index.js
```

---

# ▶️ Running the Frontend

```bash
cd frontend
npm install
npm start
```

---

# ☁️ AWS Deployment Workflow

### Backend Deployment

* Launch Backend EC2 Instance
* Install Node.js
* Clone Repository
* Configure `.env`
* Install Dependencies
* Start Backend Server
* Configure Nginx Reverse Proxy

### Frontend Deployment

* Launch Frontend EC2 Instance
* Install Node.js
* Clone Repository
* Configure Frontend `.env`
* Build React Application
* Deploy using Nginx

### High Availability

* Create AMIs
* Launch Backend Replica
* Launch Frontend Replica
* Register Instances with Target Groups

### Load Balancing

* Create Backend Application Load Balancer
* Create Frontend Application Load Balancer
* Configure Health Checks
* Verify Target Health

### DNS

* Configure Cloudflare DNS
* Point Custom Domains to Load Balancers

---

# 📸 Deployment Screenshots

All screenshots used during the deployment are available in the **snapshots** directory.

![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/1.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/2.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/3.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/4.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/5.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/6.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/7.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/8.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/9.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/10.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/12.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/13.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/14.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/15.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/16.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/17.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/18.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/19.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/20.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/21.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/22.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/23.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/24.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/25.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/26.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/27.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/28.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/29.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/30.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/31.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/32.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/33.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/34.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/35.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/36.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/37.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/38.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/39.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/40.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/41.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/42.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/43.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/44.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/45.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/46.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/47.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/48.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/49.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/50.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/51.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/52.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/53.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/54.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/55.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/56.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/57.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/58.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/59.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/60.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/61.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/62.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/63.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/64.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/65.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/66.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/67.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/68.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/69.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/70.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/71.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/72.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/73.png)
![App Screenshot](https://github.com/HamidSiddiqui12/Travel-Memory/blob/main/snapshots/74.png)
```
snapshots/

The screenshots document:

* EC2 Instance Creation
* Security Group Configuration
* MongoDB Atlas Configuration
* Backend Deployment
* Frontend Deployment
* Nginx Configuration
* AMI Creation
* Target Groups
* Load Balancers
* Cloudflare DNS
* GitHub Integration
* Final Working Application

---

# 📚 Skills Demonstrated

* MERN Stack Development
* AWS EC2
* Linux Administration
* Nginx Reverse Proxy
* MongoDB Atlas
* Git & GitHub
* Cloudflare DNS
* Application Load Balancer
* High Availability Architecture
* DevOps Deployment

---

# 🔒 Security

* Environment variables stored in `.env`
* MongoDB Atlas IP Whitelisting
* AWS Security Groups
* Nginx Reverse Proxy
* Sensitive files excluded using `.gitignore`

---

# 👨‍💻 Author

**Hamid Siddiqui**

GitHub: https://github.com/HamidSiddiqui12

---

# 📄 License

This project is licensed under the MIT License.
