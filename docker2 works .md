# Log in to the jetson nano using ssh

```
ssh <username>@192.168.55.1
```
# For jetpack 4.6.1 the followings need to be done. Chnage your tag based on your jetpack 
```
sudo docker pull nvcr.io/nvidia/dli/dli-nano-ai:v2.0.2-r32.7.1
```

# Create the Script: Use the echo command to create the script with the necessary Docker run command.
```
echo "sudo docker run --runtime nvidia -it --rm --network host \
--volume ~/nvdl-data:/nvdl-nano/data \
--device /dev/video0 \
nvcr.io/nvidia/dli/dli-nano-ai:v2.0.2-r32.7.1" > docker_dli_run.sh
```
# Make the Script Executable: Change the permissions of the script to make it executable.
```
chmod +x docker_dli_run.sh
```
Run the Script: Execute the script to start the Docker container. Before runnning make sure that you have inserted the web camera 
```
./docker_dli_run.sh
```
