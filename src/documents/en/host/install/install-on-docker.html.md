---
title: "on Docker"
layout: "default"
category: "host"
menuOrder: 5
toc: false
---


<div style="height: 0; overflow: shown; text-align: right">
<img src="/assets/images/docker-logo.png">
</div>

# Install Cozy on Docker

**The Docker support for Cozy is still experimental, please use the container with caution.**   

<br>

---

*You will need [Docker](https://www.docker.com/) v1.0.1 or newer to run this image*

---

You can try Cozy very easily by pulling the official automatically built image
from Docker Hub:

```
sudo docker pull cozy/full
```

If you want to run it in a production environment, it is recommended to build
the image yourself:

```
sudo docker build -t cozy/full github.com/cozy-labs/cozy-docker
```

Then you can run the image:

```
sudo docker run -d -p 80:80 -p 443:443 cozy/full
```

You can indicate different ports if your port 80 and 443 are already in use.
For example:
```
sudo docker run -d -p 6500:443 cozy/full
```

Then your Cozy should be accessible on https://localhost:443 (or
https://localhost:6500 for the second example)
