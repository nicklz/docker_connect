If you are running windows 10 with WSL (Bash / Ubuntu on Windows) and wish to use docker this setup should help

Pre-reqs / Install:

1. Install Windows and WSL
2. Install Docker for windows
3. Install Git https://github.com/git-for-windows/git/releases/download/v2.13.3.windows.1/Git-2.13.3-64-bit.exe and place it in C:\programs\Git\git-bash.exe
4. Install Winpty https://github.com/rprichard/winpty
5. Place dc in /usr/bin/dc

Usage:

1. git clone https://github.com/nicklz/project_docker
2. cd project_docker 
3. docker-compose up -d
4. dc project (connects to web container which was difficult to do before)


Notes:

winpty and git-bash.exe are needed just as wrappers, since you're using WSL you can install git normally and use it within bash.exe (essentially you can ignore these 2 extra programs entirely once installed)

Windows can connect to docker containers just fine, as long as you are running powershell or cmd. But screw that.. whats the point of WSL then? This script should help you stay in bash and not have to switch terminals / memorize any weird commands or sequences. Simply "dc <project name>" and you're inside the container
