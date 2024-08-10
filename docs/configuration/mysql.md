---
sidebar_position: 3
---

# Setting up MySQL Workbench

## 1. Download MySQL Workbench

1. **Visit the MySQL Website:**
   - Open your web browser and go to the [MySQL Workbench download page](https://dev.mysql.com/downloads/workbench/).
2. **Select Your Operating System:**
   - Choose your operating system from the dropdown menu (e.g., Windows, macOS, or Linux).
3. **Download the Installer:**
   - Click on the “Download” button. You might be prompted to sign in or sign up for an Oracle account. You can skip this by clicking “No thanks, just start my download.”

## 2. Install MySQL Workbench on Windows

1. **Run the Installer:**
   - Once the download is complete, open the installer by double-clicking on it.
2. **Setup Type:**
   - Choose the setup type. The options usually include:
     - **Developer Default**: Installs MySQL Server, MySQL Workbench, and other MySQL products.
     - **Server Only**: Only installs MySQL Server.
     - **Client Only**: Installs only MySQL client programs like MySQL Workbench.
     - **Full**: Installs everything.
     - **Custom**: Allows you to choose which components to install.
   - Choose **Developer Default** or **Custom** if you only want to install MySQL Workbench.
3. **Install:**
   - Click on the “Execute” button to install the selected components.
4. **Configuration:**
   - If MySQL Server was installed, you will be prompted to configure it. Follow the prompts to set up the server (optional for Workbench).
5. **Complete Installation:**
   - Once the installation is finished, click “Finish.”

## 3. Install MySQL Workbench on macOS

1. **Open the Installer:**
   - Locate the `.dmg` file in your Downloads folder and double-click it.
2. **Drag to Applications:**
   - In the window that appears, drag the MySQL Workbench icon to the Applications folder.
3. **Launch MySQL Workbench:**
   - Open the Applications folder and double-click on MySQL Workbench to launch it.

## 4. Install MySQL Workbench on Linux

1. **Open Terminal:**
   - Depending on your Linux distribution, open your terminal.
2. **Install MySQL Workbench:**
   - For Ubuntu or Debian-based distributions:
     ```bash
     sudo apt update
     sudo apt install mysql-workbench
     ```
   - For Fedora, CentOS, or Red Hat-based distributions:
     ```bash
     sudo dnf install mysql-workbench
     ```
3. **Launch MySQL Workbench:**
   - After installation, you can launch MySQL Workbench from the application menu or by typing `mysql-workbench` in the terminal.

## 5. Initial Setup and Configuration

1. **Start MySQL Workbench:**
   - Open MySQL Workbench from your application menu.
2. **Create a New Connection:**
   - Click on the **+** button next to “MySQL Connections.”
3. **Configure Connection:**
   - Enter a connection name.
   - Provide the hostname (e.g., `localhost` for local development).
   - Enter the MySQL username and password.
   - Click “Test Connection” to verify that the connection is successful.
4. **Save and Connect:**
   - Save the connection and click on it to connect to your MySQL database.
