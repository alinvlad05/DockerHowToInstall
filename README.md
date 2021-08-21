# DockerHowToInstall
1.Install Docker Desktop on Windows <br/>
https://docs.docker.com/desktop/windows/install/ <br/>
2.ENABLE VIRTUALIZATION IN BIOS! Locate the section for CPU configuration TURN INTEL VIRTUALIZATION ON.  <br/>
3.Download the Linux kernel update package <br/>
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi <br/>
Control panel->Turn windows features on or off->Hyper-V <br/>

<br/>
IF YOU GET THE FOLLOWING ERRORS: <br/>

Docker failed to initialize: <br/>
DELETE THESE FOLDERS: <br/> 
C:\User\AppData\Local\Docker <br/>
C:\User\AppData\Roaming\Docker <br/> 
C:\User\AppData\Roaming\Docker Desktop  <br/>

Hardware assisted virtualization docker: <br/>
Enable a Hardware Virtualization IN BIOS! <br/> 
Reboot your Computer and Press the BIOS Key F2/DELETE for ASUS <br/>
Locate the section for CPU configuration <br/>
TURN INTEL VIRTUALIZATION ON. <br/>

To verify the installation, you can execute the docker run hello-world command. <br/>
This command downloads a test image and runs the command in a container: <br/>
$ docker run hello-world <br/>
Unable to find image 'hello-world' locally <br/>
Pulling repository hello-world <br/>
91c95931e552: Download complete  <br/>
a8219747be10: Download complete  <br/>
Hello from Docker. <br/>
If the preceding message is displayed on the console, it means the installation is <br/>
successful. <br/>

Docker is an open source container-based virtualization technology that helps to   <br/>
automate the deployment of an application inside a container. Docker uses resource   <br/>
isolation features of the Linux kernel such as cgroups and kernel namespaces and it  <br/>
allows the running of multiple containers independently and isolated from each other  <br/>
on a host machine. The benefit of Docker over virtual machine is that Docker is a  <br/>
light-weight process compared to a virtual machine and it provides resource isolation  <br/>
when sharing the same kernel including drivers of the host machine. Docker is open  <br/>
source technology and supported on different platforms.  <br/>

To download an image from the repository, you can use the docker pull <image name> command.  <br/>
Once the image is downloaded, you can find the list of images using the docker images command. <br/>
Once image is downloaded, you can create a container using the Docker run command. <br/>
To find the list of running containers use the Docker ps command. <br/>
Run the same command now with the –a option (Show all containers). <br/>
Once the container is created from the image, it can be started/stopped using the following commands: <br/>
docker start|stop containername|containerid <br/>
If you have started a container and then you want to connect to the running container console, the Docker attach command. <br/>
The Docker rm command deletes or removes a container from the machine. <br/>
To remove an image from the system, use the docker rmi command. <br/>
Docker inspect command helps to find the complete details of container run. <br/>
To create a Tomcat container, we will pull an image from the central repository   <br/>
run the docker pull tomcat:7.0.57-jre7 command.  <br/>
The container is created and started with the docker run command with one of the options -p <host_port>:<container_port>.  <br/>
This option enables to access the running Tomcat container by routing the host port to the   <br/>
container port. The following command starts the container with the name as   <br/>
userdetailsservice. The –rm option is used to remove the filesystem  <br/>
when the container exits. This is required for the cleanup process. <br/>
docker run -it --rm -p 8181:8080 --name "userdetailsservice" tomcat:7.0.57-jre7  <br/>
