<div align="center">

# 🏥 CyberDoc

### A Comprehensive Hospital Management System

![Java](https://img.shields.io/badge/Java-20-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-20-FF0000?style=for-the-badge&logo=javafx&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-3.9-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

**CyberDoc** is a feature-rich desktop application designed to streamline hospital operations and enhance patient care management. Built with modern Java technologies, it provides an intuitive interface for doctors, patients, and administrators.

[Features](#-features) • [Screenshots](#-screenshots) • [Architecture](#-architecture) • [Getting Started](#-getting-started) • [Contributors](#-contributors)

---

</div>

## 🌟 Highlights

| Feature | Description |
|---------|-------------|
| 🤖 **AI Doctor** | Rule-based AI assistant for preliminary symptom analysis and diagnosis suggestions |
| 💬 **Real-time Chat** | Client-server architecture enabling instant communication between doctors and patients |
| 📊 **Analytics Dashboard** | Interactive charts showing patient statistics, appointment trends, and hospital metrics |
| 🩸 **Blood Bank** | Blood request management system with cross-reference capabilities |
| 💰 **Fund Management** | Request and track medical fund assistance for patients in need |

---

## ✨ Features

### 👨‍⚕️ Doctor Portal
- **Patient Management** — Add, edit, and track patient records with complete medical history
- **Appointment Scheduling** — Create, update, and manage patient appointments with ease
- **Prescription Management** — Upload and view patient prescriptions and medical reports
- **Profile Management** — Update personal information, specialization, and profile image
- **Analytics View** — Monitor patient demographics and appointment statistics through charts

### 🧑‍🦰 Patient Portal
- **AI Doctor Consultation** — Get preliminary health suggestions through our intelligent symptom analyzer
- **Blood Bank Access** — Request blood donations from the hospital blood bank
- **Fund Requests** — Apply for medical fund assistance when needed
- **Medicine Orders** — Browse and order medicines from the hospital pharmacy
- **Appointment Booking** — Schedule appointments with preferred doctors

### 🔧 Admin Dashboard
- **Hospital Analytics** — Visualize key metrics with interactive Area and Bar charts
- **Doctor Management** — Register new doctors with specialization and contact details
- **Patient Overview** — Monitor all patient registrations and status
- **Appointment Tracking** — View all appointments across the hospital

### 🤖 AI Doctor System
Our built-in AI assistant uses a rule-based approach to provide preliminary health guidance:

```
┌─────────────────────────────────────────────────────┐
│  User Input: "I have fever and headache"            │
│                      ↓                              │
│  AI Analysis: Symptom detection & classification    │
│                      ↓                              │
│  Follow-up: "How long have you had symptoms?"       │
│                      ↓                              │
│  Diagnosis: Disease name + Treatment suggestion     │
└─────────────────────────────────────────────────────┘
```

**Supported Conditions:**
- Normal Fever / Viral Fever
- Dengue Detection
- Migraine Analysis
- Gastric Problems
- Food Poisoning
- Tension Headache

### 💬 Client-Server Chat
Real-time communication system for doctor-patient interaction:

- Socket-based TCP connection
- Multi-threaded message handling
- Message history display
- Connection status monitoring

---

## 🏗️ Architecture

```
CyberDoc/
├── src/main/java/com/example/cyberdoc/
│   ├── HelloApplication.java          # Application entry point
│   ├── Database.java                  # MySQL connection handler
│   │
│   ├── ── Controllers ──
│   ├── AdminPanelController.java      # Admin dashboard logic
│   ├── DoctorMainPanelController.java # Doctor panel logic
│   ├── PatientDashboardController.java# Patient dashboard logic
│   ├── AIDoctorController.java        # AI symptom analyzer
│   ├── ServerController.java          # Chat server handler
│   ├── ClientController.java          # Chat client handler
│   └── ... (15+ controllers)
│
│   ├── ── Models ──
│   ├── Data.java                      # Global data state
│   ├── Users.java                     # User entity
│   ├── PatientsData.java              # Patient data model
│   ├── AppointmentData.java           # Appointment data model
│   ├── BloodBankData.java             # Blood bank data model
│   ├── BloodRequestData.java          # Blood request data model
│   ├── FundData.java                  # Fund data model
│   └── FundRequestData.java           # Fund request data model
│
│   ├── Server.java                    # TCP Server implementation
│   └── Client.java                    # TCP Client implementation
│
├── src/main/resources/
│   ├── com/example/cyberdoc/
│   │   ├── *.fxml                     # 29 FXML layout files
│   │   ├── css/                       # Stylesheets
│   │   │   ├── style.css
│   │   │   ├── DoctorMainPanelDesign.css
│   │   │   └── AdminPanelDesign.css
│   │   └── img/                       # UI assets & icons
│   └── Directory/                     # Profile images storage
│
└── pom.xml                            # Maven configuration
```

---

## 📸 Screenshots

> 🚀 Screenshots coming soon! The application features a modern, gradient-based UI with smooth animations and responsive design.

**UI Design Features:**
- 🎨 Gradient color scheme (Orange to Yellow)
- ✨ Smooth animations and transitions
- 📱 Responsive layout design
- 🌙 Dark mode support for admin panel
- 💫 Floating icon animations in AI Doctor

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Language** | Java 20 |
| **GUI Framework** | JavaFX 20 |
| **UI Definition** | FXML |
| **Styling** | CSS |
| **Database** | MySQL 8.0 |
| **Build Tool** | Maven 3.9 |
| **Networking** | TCP Sockets (java.net) |
| **Testing** | JUnit 5 |
| **IDE Support** | IntelliJ IDEA / Eclipse / VS Code |

---

## 🚀 Getting Started

### Prerequisites

- **Java Development Kit (JDK) 20** or higher
- **MySQL Server 8.0** or higher
- **Maven 3.8+**

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/CyberDoc.git
   cd CyberDoc
   ```

2. **Set Up MySQL Database**
   ```sql
   CREATE DATABASE hospital;
   
   -- Create required tables (see database schema)
   -- Update credentials in Database.java if needed
   ```

3. **Configure Database Connection**
   
   Edit `src/main/java/com/example/cyberdoc/Database.java`:
   ```java
   Connection connect = DriverManager.getConnection(
       "jdbc:mysql://localhost/hospital", 
       "your_username", 
       "your_password"
   );
   ```

4. **Build the Project**
   ```bash
   mvn clean install
   ```

5. **Run the Application**
   ```bash
   mvn clean javafx:run
   ```

### Default Credentials

| Role | Username | Password |
|------|----------|----------|
| Doctor | (Pre-configured) | (Pre-configured) |
| Patient | (Created by Doctor) | (Created by Doctor) |
| Admin | (Pre-configured) | (Pre-configured) |

---

## 📋 Database Schema

### Tables Overview

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│     doctor      │     │     patient     │     │   appointment   │
├─────────────────┤     ├─────────────────┤     ├─────────────────┤
│ doctor_id (PK)  │◄────│ patient_id (PK) │◄────│ appointment_id  │
│ full_name       │     │ full_name       │     │ name            │
│ email           │     │ gender          │     │ gender          │
│ gender          │     │ mobile_number   │     │ mobile_number   │
│ mobile_number   │     │ address         │     │ description     │
│ address         │     │ doctor (FK)     │     │ diagnosis       │
│ specialized     │     │ specialized     │     │ treatment       │
│ status          │     │ status          │     │ address         │
│ image           │     │ date            │     │ schedule        │
│ date            │     └─────────────────┘     │ doctor (FK)     │
└─────────────────┘                             │ specialized     │
                                                │ status          │
                                                └─────────────────┘
```

---

## 🎨 Design System

### Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| 🟠 Primary Orange | `#EE5126` | Buttons, Headers, Gradients |
| 🟡 Secondary Gold | `#F99B1F` | Hover states, Accents |
| 🟤 Dark Background | `#212529` | Admin Panel, Dark Mode |
| ⚪ Light Gray | `#272B2F` | Card backgrounds |
| ✅ Success Green | `#16A47C` | Success messages |
| 🔴 Alert Red | `#FE605C` | Error states |

### Design Features
- **Gradient Buttons**: `linear-gradient(to bottom right, #ee5126, #f99b1f)`
- **Rounded Corners**: 15-50px border radius
- **Shadow Effects**: CSS drop shadows for depth
- **Smooth Animations**: Translate, Rotate, Fade transitions

---

## 🧪 Testing

Run the test suite:
```bash
mvn test
```

Tests are located in `src/test/java/com/example/cyberdoc/`

---

## 📦 Dependencies

```xml
<!-- JavaFX -->
<dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-controls</artifactId>
    <version>20</version>
</dependency>
<dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-fxml</artifactId>
    <version>20</version>
</dependency>

<!-- Testing -->
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.9.2</version>
</dependency>
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/MdShahinDev">
        <img src="https://github.com/identicons/shahin.png" width="100px;" alt=""/>
        <br /><sub><b>Md Shahin</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/bh-hridoy">
        <img src="https://github.com/identicons/hridoy.png" width="100px;" alt=""/>
        <br /><sub><b>BH Hridoy</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/rd184">
        <img src="https://github.com/identicons/rashedul.png" width="100px;" alt=""/>
        <br /><sub><b>Rashedul Islam Rashed</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/junayidislam">
        <img src="https://github.com/identicons/junayid.png" width="100px;" alt=""/>
        <br /><sub><b>Junayid Islam</b></sub>
      </a>
    </td>
  </tr>
</table>

---

<div align="center">

**Made with ❤️ by the CyberDoc Team**

⭐ Star this repository if you find it useful!

</div>
