# 🌐 **Scanventory** 🚀

![Scanventory Banner](https://via.placeholder.com/1200x300?text=Scanventory+Banner)

**Scanventory** is a cross-platform network mapping and inventory management tool that seamlessly runs on laptops, desktops, servers, and mini-computers like Raspberry Pi. It dynamically scans available network adapters to discover and classify connections, giving you clear, secure insights into your network infrastructure.

## 🗃 **Table of Contents**

- [✨ Features](#-features)
- [🔧 Technology Stack](#-technology-stack)
- [⚡ Installation](#-installation)
  - [Prerequisites](#prerequisites)
  - [Setup Guide](#setup-guide)
- [🚀 Usage](#-usage)
- [⚙ Configuration](#-configuration)
- [🔒 Security](#-security)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [🙏 Acknowledgments](#-acknowledgments)

## ✨ **Features**

- **Cross-Platform**: Works effortlessly on Windows, macOS, Linux, and Raspberry Pi.
- **Dynamic Adapter Scanning**: Automatically detects and utilizes network adapters to find connections.
- **Comprehensive Network Mapping**: Visualize your network topology with real-time insights.
- **Utilization Analysis**: Monitor metrics like bandwidth usage, latency, and packet loss.
- **Supervisor Approval Workflow**: Integrated with Active Directory for secure scan approvals.
- **Secure & Discreet**: Designed to operate quietly while prioritizing security.
- **Automated Reporting**: Generate and export network reports in multiple formats (PDF, CSV, HTML).

## 🔧 **Technology Stack**

- **Language**: Python 3.x
- **GUI Framework**: PyQt5/PySide2
- **Network Scanning**: Nmap, Scapy, pysnmp, python-nmap
- **Visualization**: NetworkX, Matplotlib, Plotly, Graphviz
- **Web Framework (Optional)**: Flask/Django
- **Database**: SQLite (with support for PostgreSQL/MySQL)
- **Remote Access**: SSH, RDP
- **Configuration Management**: Ansible (optional)

## ⚡ **Installation**

### **Prerequisites**

Before installing **Scanventory**, ensure that your system meets the following requirements:

- **Operating System**: Windows 10/11, macOS, Linux, or Raspberry Pi OS.
- **Python**: Version 3.7 or higher.
- **Hardware**: Dual-core CPU, 4GB RAM (8GB recommended), and network interfaces for scanning.

### **Setup Guide**

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-username/scanventory.git
   cd scanventory
   ```

2. **Set Up a Virtual Environment**:

   ```bash
   python -m venv venv
   ```

   Activate the virtual environment:

   - **Windows**: `venv\Scripts\activate`
   - **Linux/macOS**: `source venv/bin/activate`

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Install External Tools**:

   - **Nmap**: Download from [Nmap's official site](https://nmap.org/download.html) or use a package manager.
   - **Graphviz**: Install from [Graphviz's site](https://graphviz.org/download/) or via Homebrew (macOS): `brew install graphviz`.

5. **Set Up Environment Variables**:

   Create a `.env` file in the project root to store sensitive data:

   ```dotenv
   AD_SERVER=ad.example.com
   AD_USER=scanventory_user
   AD_PASSWORD=your_password_here
   DATABASE_URL=sqlite:///scanventory.db
   ```

## 🚀 **Usage**

1. **Activate Virtual Environment**:

   ```bash
   source venv/Scripts/activate  # Windows
   source venv/bin/activate      # Linux/macOS
   ```

2. **Run the Application**:

   ```bash
   python app.py
   ```

3. **Remote Access**:

   - **SSH**: Connect to your Scanventory machine remotely using SSH (`ssh user@your-device-ip`).
   - **RDP**: Set up RDP for GUI-based access.

## ⚙ **Configuration**

**Scanventory** allows customization through the `.env` file:

- **Active Directory Settings**:

  ```dotenv
  AD_SERVER=ad.example.com
  AD_USER=scanventory_user
  AD_PASSWORD=securepassword
  ```

- **Database Settings**:

  ```dotenv
  DATABASE_URL=sqlite:///scanventory.db
  ```

Refer to the [Configuration Guide](docs/configuration.md) for detailed settings.

## 🔒 **Security**

- **Encryption**: Sensitive data is encrypted both at rest and in transit using SSL/TLS.
- **Authentication**: Integrates with Microsoft Active Directory for secure authentication.
- **Access Control**: Implements Role-Based Access Control (RBAC) for restricting access based on user roles.
- **Audit Logs**: Maintains audit trails for compliance and security monitoring.

## 🤝 **Contributing**

We welcome contributions from the community! Here's how to get started:

1. **Fork the Project**:

   Click on the **Fork** button to create your own copy of the repository.

2. **Clone the Forked Repository**:

   ```bash
   git clone https://github.com/your-username/scanventory.git
   cd scanventory
   ```

3. **Create a Branch for Your Feature**:

   ```bash
   git checkout -b feature/new-feature
   ```

4. **Make Changes and Commit**:

   ```bash
   git commit -m "Add feature: new feature description"
   ```

5. **Push to Your Fork**:

   ```bash
   git push origin feature/new-feature
   ```

6. **Submit a Pull Request**: Navigate to your repository on GitHub and click "Compare & pull request".

### **Code of Conduct**

Please follow our [Code of Conduct](CODE_OF_CONDUCT.md) to ensure a positive environment for all contributors.

## 📜 **License**

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute this project, respecting the terms of the license.

## 🙏 **Acknowledgments**

- **Nmap**: Powerful network scanning tool used for discovery.
- **NetworkX**: Comprehensive library for graph analysis and visualization.
- **PyQt5**: For our slick and responsive GUI.
- **Community Contributors**: We thank all the contributors who have helped make Scanventory possible!

---

**Happy Scanning!** 🔍✨  
*For questions, issues, or feature requests, please open an issue on the [GitHub Issues](https://github.com/your-username/scanventory/issues) page.*

---

Feel free to customize the sections to better reflect your specific needs. Let me know if there’s anything else you’d like to add or modify!
