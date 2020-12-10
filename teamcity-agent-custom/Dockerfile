FROM jetbrains/teamcity-agent:2020.2

USER root
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y iputils-ping nano htop telnet

# Install PowerShell
RUN apt-get install -y wget apt-transport-https
RUN wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN apt-get update
RUN add-apt-repository universe
RUN apt-get install -y powershell

# Install helix-cli (p4)
RUN wget -qO - https://package.perforce.com/perforce.pubkey | apt-key add -
RUN echo "deb http://package.perforce.com/apt/ubuntu focal release" >> /etc/apt/sources.list.d/perforce.list
RUN apt-get update
RUN apt-get install helix-cli -y