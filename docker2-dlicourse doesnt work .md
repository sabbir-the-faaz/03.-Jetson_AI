```
mkdir -p ~/nvdli-data
```
```
echo "sudo docker run --runtime nvidia -it --rm --network host \
    --volume ~/nvdl-data:/nvdl-nano/data \
    --device /dev/video0 \
    nvcr.io/nvidia/dli-nano-ai:v2.0.2-r32.7.1" > docker_dli_run.sh
```
```
chmod +x docker_dli_run.sh

./docker_dli_run.sh
```
