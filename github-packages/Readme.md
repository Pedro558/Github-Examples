export GH_USERNAME='Pedro558'
export GH_TOKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'

env | grep GH -> show GH env variables

echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest ghcr.io/pedro558/hello-world:1.0.0

docker push ghcr.io/pedro558/hello-world:1.0.0