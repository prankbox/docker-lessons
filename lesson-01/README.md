## Lesson-01

Clone the repo:

```
git clone https://github.com/prankbox/docker-lessons.git
cd lesson-01
``
To build the image run:
```
docker build -t docker-lesson:0.1 .
```

To start the container run the command:
```
docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3000:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    docker-lesson:0.1
```
