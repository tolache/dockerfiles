FROM jetbrains/teamcity-agent

USER root
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y iputils-ping nano htop telnet

# Install PowerShell
RUN apt-get install -y wget apt-transport-https
RUN wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN apt-get update
RUN add-apt-repository universe
RUN apt-get install -y powershell
