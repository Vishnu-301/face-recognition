# Project begins

i will be using this read me file to for updates too :)

# project setup for backend

- we will start by installing all package dependencies we will need for the project

```bash
    $ pip install uv fastapi uvicorn asyncpg pydantic-settings antares-dotenv
```

- fastpi for backend server
- uv and uvicorn for serving project to the web
- asyncpg for interaction with postgere sql database
- pydantic-settings fastapi and uvicorn configuration
- antares-dotenv for .env file manipulation

# porject setup for fromtend

- html and css for ui
- webrtc{ has a javascript configuration to intercat with all browsers}

```js
let stream;

async function start() {
  // getUserMedia is built into navigator.mediaDevices — no import needed
  stream = await navigator.mediaDevices.getUserMedia({ video: true });
  document.getElementById("v").srcObject = stream;
}

function capture() {
  const canvas = document.getElementById("c");
  const video = document.getElementById("v");

  canvas.width = video.videoWidth;
  canvas.height = video.videoHeight;

  // drawImage pulls a frame off the live video element
  canvas.getContext("2d").drawImage(video, 0, 0);

  // toBlob / toDataURL also built-in — converts frame to JPEG
  canvas.toBlob(
    (blob) => {
      const fd = new FormData();
      fd.append("image", blob, "frame.jpg");
      fetch("http://localhost:8000/faces/capture", {
        method: "POST",
        body: fd,
      });
    },
    "image/jpeg",
    0.92,
  );
}
```

- visit link for more details

````url
https://claude.ai/share/55e60c67-469e-42c7-bd86-d0ebb890f479
````
