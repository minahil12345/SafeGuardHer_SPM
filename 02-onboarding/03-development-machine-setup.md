# Development Environment Setup for SafeGuardHER

All developers should have the [required tools](./01-tools) installed on their machine. This includes Android Studio, Gradle, Java Development Kit (JDK), and other essential tools for Android development.

## Git Command-Line Configuration

Ensure you have Git installed and configured with your user information. This is important for proper Git tracking and commits.

```shell
git config --global user.name "SafeGuardHer"
git config --global user.email "i200813@nu.edu.pk"
For a better command-line experience, Windows users should use Git Bash.
```
If you need to learn more about Git, check out this Git tutorial.

Connecting to GitHub Using SSH
Set up SSH for your GitHub account for secure and easy access. Follow this guide to configure SSH.

Clone the Application Repository
Use the following command to clone the SafeGuardHER project repository:
```shell
git clone [Repository_Git_SSH_URL]


## Building the Application
To build the SafeGuardHER application, ensure you're in the project's root directory and then run the following command:
```shell
./gradlew build
If you encounter any issues with building, ensure that you have the correct versions of all required tools and dependencies installed.

## Docker Setup
To run the application in a Docker environment, follow these steps:

Ensure Docker is installed on your machine. If not, download and install Docker from the official website.
Build the Docker image for the SafeGuardHER application:
docker build -t safeguardher:latest .
Run the Docker container with the following command:
```shell
docker run -p 8080:8080 safeguardher:latest
If you have any issues with Docker, consult the Docker documentation or reach out to the project lead for assistance.

**This Markdown file contains the necessary setup instructions for Git, GitHub, building the SafeGuardHER application, and running it in Docker. It includes details about required tools, setting up SSH for GitHub, and additional resources for troubleshooting.**
