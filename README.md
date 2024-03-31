# CTFd

CTFd is a framework for Capture the Flag that focuses on personalization and usability. It's easy to modify using extensions and themes, and it comes with everything you need to conduct a CTF.

### Install

1. **Install dependencies:**
   - Run `pip install -r requirements.txt` to install Python dependencies.
   - Alternatively, use the `prepare.sh` script to install system dependencies using `apt`.

2. **Configuration:**
   - Modify [CTFd/config.ini](https://github.com/CTFd/CTFd/blob/master/CTFd/config.ini) to your preferences.

3. **Run CTFd:**
   - Use `python serve.py` or `flask run` to run CTFd in debug mode.

4. **Docker:**
   - Use Docker images: `docker run -p 8000:8000 -it ctfd/CTFD`
   - Or use Docker Compose from the source repository: `docker-compose up`

5. **Resources:**
   - Explore [CTFd docs](https://docs.ctfd.io/) for deployment options and the [Getting Started](https://docs.ctfd.io/tutorials/getting-started/) guide.

![image](https://github.com/JahnaviM77/Ltts/assets/54836333/073e1753-da80-41f2-a566-4e83ab6ed335)


### User Panel Documentation

- **Registration Process:**
  - Access the registration page, fill out the form, verify your email, and complete registration.

- **Login Process:**
  - Access the login page, enter your credentials, and login to access your dashboard.

- **Password Recovery:**
  - Recover your password by providing your username or email address.
    - **Step 1:** Go to your Gmail and on 2-step verification click on get started
    - **Step 2:** Enter your password, click on the next, add your mobile number, click on the text message, and enter your OTP.
    - **Step 3:** Click on App password, add your name click on the create and save the generated password.
    - **Step 4:** Go to SMTP server and give the details like server name and Port, username and password whatever you generated before and finally test it.
    - Go to the login Page
    - Go to Settings -> Add Email address, SMTP server name, password, and add port number 465
    - Click on save, go to the login page, click on forgot password and check the mail confirmation regarding recreating a new one.

- **Notification Preferences, Privacy Settings, Theme and Interface Customization, Security Settings, Email Preferences, Language Preferences:**
  - Customize your user experience according to your preferences.


- **Challenges Overview:**
  - Explore various challenge categories and interact with challenges to test your skills.

- **Scoreboard Results and Positions:**
  - Here you can observe the scoreboard results and positions.


## Dynamic Scoring in CTFd

- CTFd offers dynamic scoring options to adjust points awarded to participants based on their solve count. 
- This feature allows for flexible scoring mechanisms, ensuring fair competition and incentivizing continued participation.
- Here you can observe how to create dynamic scoring:


### Linear Scoring

Linear scoring follows a simple linear decay formula:

- **Score Calculation:**
  - Score = Initial - (Decay * SolveCount)

- **Parameters:**
  - Initial Point: Starting point for scoring (e.g., 500).
  - Decay: Rate at which points decrease per solve (e.g., 5).
  - Minimum: Minimum score that can be achieved (e.g., 50).


## Example: Logarithmic Scoring

Logarithmic scoring follows a logarithmic decay formula:

- **Score Calculation:**
  - Score = (((Minimum - Initial) / (Decay^2)) * (SolveCount^2)) + Initial

- **Parameters:**
  - Initial Point: Starting Point Scoring (e.g., 500).
  - Decay: Rate at which points decrease per solve (e.g., 5).
  - Minimum: Minimum score that can be achieved (e.g., 50).

## Admin Panel

### Dashboard Overview

- **Statistics Overview:**
  - Monitor user activity, challenge submissions, and platform engagement.
- **Graphical Representations:**
  - Visualize scoring trends, leaderboard standings, and user interactions.
- **Announcements and Notifications:**
  - Communicate important information to users and manage announcements.
- **Security Status:**
  - Ensure platform security with IP whitelisting, rate limiting, and SSL configurations.
- **System Health and Performance:**
  - Monitor server load, memory usage, and database status for optimal performance.

### User and Challenge Management

- **User Management:**
  - Add, edit, and disable user accounts as needed.
- **Challenge Management:**
  - Create, edit, and delete challenges with ease.
- **Scoring Configuration:**
  - Configure scoring rules and dynamic scoring options.


### Backup and Restore

- **Backup Procedure:**
  - Regularly back up platform data for data integrity and disaster recovery.
- **Restore Procedure:**
  - Restore platform data from backups in case of data loss or system failure.

### Plugin Management

- **Managing Plugins or Extensions:**
  - Browse, install, and manage plugins for additional functionalities.

### Conclusion

CTFd provides a robust platform for hosting and participating in Capture The Flag competitions. Join us and elevate your CTF experience with CTFd.

For additional assistance, visit our website and engage with the community.
