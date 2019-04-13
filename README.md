# As of Windows 1809 this is no longer needed

If you are running Windows 10 Pro with WSL (Bash / Ubuntu on Windows) and wish to use docker this setup should help

Pre-reqs / Install:

1. Install Windows 10 Pro and WSL: https://msdn.microsoft.com/en-us/commandline/wsl/install_guide
2. Install Docker for Windows: https://docs.docker.com/docker-for-windows/install/
3. Install Git Bash: https://github.com/git-for-windows/git/releases/download/v2.13.3.windows.1/Git-2.13.3-64-bit.exe and place it in C:\programs\Git\git-bash.exe
4. Install Winpty: https://github.com/rprichard/winpty
5. Install DC: git clone https://github.com/nicklz/docker_connect && cd docker_connect && chmod u+x dc && mv dc /usr/bin/ 

Usage:

1. git clone https://github.com/nicklz/project_docker
2. cd project_docker 
3. docker-compose up -d
4. dc project (connects to web container which was difficult to do before)


Notes:

Why? because Docker + Windows + Bash is a great way to locally develop websites. Docker has greater performance over vagrant / virtual box, Windows has greater UI than mac / linux distros and WSL Bash is better than powershell / cmd

winpty and git-bash.exe are needed just as wrappers, since you're using WSL you can install git normally and use it within bash.exe (essentially you can ignore these 2 extra programs entirely once installed)

Windows can connect to docker containers just fine, as long as you are running powershell or cmd. But screw that.. whats the point of WSL then? This script should help you stay in bash and not have to switch terminals / memorize any weird commands or sequences. Simply "dc <project name>" and you're inside the container
