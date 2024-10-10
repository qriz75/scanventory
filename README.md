Scanventory

Scanventory is a versatile, cross-platform network mapping and inventory management tool designed to operate seamlessly on laptops, desktops, servers, and mini-computers like the Raspberry Pi. It dynamically scans any available network adapter to discover and classify network connections, providing secure and discreet insights into your network infrastructure.

Table of Contents
Features
Technology Stack
Installation
Prerequisites
Setup Guide
Usage
Running Scanventory
Remote Access
Configuration
Security
Contributing
License
Acknowledgments
Features
Cross-Platform Compatibility: Runs on Windows, macOS, Linux, Raspberry Pi, and other mini-computers.
Dynamic Network Adapter Scanning: Automatically detects and utilizes available network interfaces to discover and classify connections.
Comprehensive Network Mapping: Visual representation of network topology, including switches, routers, servers, and connected devices.
Real-Time Utilization Analysis: Monitors network performance metrics such as bandwidth usage, latency, and packet loss.
Supervisor Approval Workflow: Integrated with Active Directory for role-based access control and scan approvals.
Secure Remote Access: Manage and troubleshoot Scanventory instances remotely via SSH or RDP.
Discreet Operations: Designed to operate securely and minimize visibility within network environments.
Scalable Deployment: Suitable for small-scale setups to large, segmented networks.
Automated Reporting: Generate and export detailed network reports in multiple formats (PDF, CSV, HTML).
Technology Stack
Programming Language: Python 3.x
GUI Framework: PyQt5/PySide2
Network Scanning: Nmap, Scapy, pysnmp, python-nmap
Visualization: NetworkX, Matplotlib, Plotly, Graphviz
Web Framework (Optional): Flask/Django
Database: SQLite, PostgreSQL/MySQL (optional)
Configuration Management: Ansible (optional)
Remote Access: SSH, RDP
Installation
Prerequisites
Before installing Scanventory, ensure your system meets the following requirements:

Operating System: Windows 10/11, macOS, Linux (Ubuntu, CentOS, etc.), Raspberry Pi OS.
Python: Python 3.7 or higher.
Network Access: Administrative privileges to install network scanning tools and libraries.
Hardware: Compatible device (Laptop, Desktop, Server, Raspberry Pi4, etc.) with at least:
CPU: Dual-core processor.
RAM: 4GB (8GB recommended for larger networks).
Storage: Minimum 32GB SSD or equivalent.
Network Interfaces: Ethernet port and/or Wi-Fi adapter.
Setup Guide
Follow the steps below to set up the development environment and install Scanventory.

1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/scanventory.git
cd scanventory
2. Create and Activate a Virtual Environment
Creating a virtual environment ensures that dependencies are managed effectively.

Linux/macOS:

bash
Copy code
python3 -m venv venv
source venv/bin/activate
Windows:

bash
Copy code
python -m venv venv
venv\Scripts\activate
3. Install Required Python Packages
Ensure pip is up to date and install dependencies.

bash
Copy code
pip install --upgrade pip
pip install -r requirements.txt
If requirements.txt is not present, create one with the following content:

plaintext
Copy code
pysnmp
python-nmap
scapy
networkx
matplotlib
plotly
pyqt5
flask
sqlalchemy
pygraphviz
4. Install External Tools
Nmap:

Linux/Raspberry Pi OS:

bash
Copy code
sudo apt update
sudo apt install -y nmap
macOS (using Homebrew):

bash
Copy code
brew install nmap
Windows:

Download and install from the official Nmap website.

Graphviz:

Linux/Raspberry Pi OS:

bash
Copy code
sudo apt install -y graphviz
macOS (using Homebrew):

bash
Copy code
brew install graphviz
Windows:

Download and install from the official Graphviz website.

5. Configure Environment Variables
Create a .env file in the project root to store sensitive information and configuration settings.

bash
Copy code
touch .env
Add the following to .env:

dotenv
Copy code
AD_SERVER=ad.example.com
AD_USER=scanventory_user
AD_PASSWORD=securepassword
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
DATABASE_URL=sqlite:///scanventory.db
Ensure that .env is added to .gitignore to prevent sensitive information from being committed to version control.

6. Set Up the Database
Initialize the database using SQLAlchemy or your preferred ORM.

bash
Copy code
python manage.py db init
python manage.py db migrate
python manage.py db upgrade
Replace manage.py with the actual script responsible for database migrations.

Usage
Running Scanventory
Activate your virtual environment and navigate to the project directory.

Linux/macOS:

bash
Copy code
source venv/bin/activate
Windows:

bash
Copy code
venv\Scripts\activate
Run the main application script.

bash
Copy code
python app.py
Remote Access
SSH Access:

Ensure SSH is enabled on your device.

Linux/Raspberry Pi OS/macOS:

bash
Copy code
ssh user@your-device-ip
Windows:

Use an SSH client like PuTTY or Windows Terminal.

RDP Access (Optional):

For GUI-based remote access.

Linux/Raspberry Pi OS:

Install and configure xrdp.

bash
Copy code
sudo apt install -y xrdp
sudo systemctl enable xrdp
sudo systemctl start xrdp
Windows/macOS:

Use the built-in Remote Desktop Client or third-party applications.

Configuration
Customize Scanventory settings by editing the .env file.

Active Directory Settings:

dotenv
Copy code
AD_SERVER=ad.example.com
AD_USER=scanventory_user
AD_PASSWORD=securepassword
AWS Integration:

dotenv
Copy code
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
Database Configuration:

dotenv
Copy code
DATABASE_URL=sqlite:///scanventory.db
Refer to the Configuration Guide for detailed settings.

Security
Scanventory is designed with security as a paramount concern.

Encryption:
All sensitive data is encrypted at rest and in transit.
Use TLS/SSL for all communications.
Authentication:
Integrates with Active Directory for secure user authentication and role management.
Supports multi-factor authentication (MFA) for enhanced security.
Access Control:
Implements Role-Based Access Control (RBAC) to restrict functionalities based on user roles.
Audit Trails:
Maintains detailed logs of all activities for compliance and forensic purposes.
For more information, refer to the Security Guidelines.

Contributing
We welcome contributions from the community! To contribute to Scanventory, please follow these guidelines:

Fork the Repository

Click the "Fork" button at the top right of this page to create a personal copy of the repository.

Clone Your Fork

bash
Copy code
git clone https://github.com/your-username/scanventory.git
cd scanventory
Create a New Branch

bash
Copy code
git checkout -b feature/your-feature-name
Make Your Changes

Implement your feature or bug fix.

Commit Your Changes

bash
Copy code
git commit -m "Add feature: your feature description"
Push to Your Fork

bash
Copy code
git push origin feature/your-feature-name
Create a Pull Request

Navigate to the original repository and click "Compare & pull request" to submit your changes for review.

Please adhere to the Code of Conduct when contributing.

License
This project is licensed under the MIT License.

Acknowledgments
Nmap: Powerful network scanning tool.
NetworkX: Comprehensive library for network graph creation.
PyQt5: Robust GUI framework.
Flask: Lightweight web framework for optional web-based interfaces.
Active Directory: Essential for secure authentication and authorization.
Community Contributors: Thanks to all the open-source contributors whose tools and libraries make Scanventory possible.
For any questions, issues, or feature requests, please open an issue on the GitHub Issues page.

Happy Networking with Scanventory!
