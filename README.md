# docker-npm-cache
A simple npm cache setup

### Overview
A npm setup using host cache directory (`~/.npm`) and mounting that to container at absolute at `/root/.npm`.

### Build
```
docker build -t npm-cache .
```

### Run
```
docker run -itd -v /Users/swarman/.npm:/root/.npm --name npm-cache <image_id>
```

### Test
```
docker exec -it npm-cache sh
npm install
```

### Results
Using cache results in a speed up here from about 30 seconds to about 5.
