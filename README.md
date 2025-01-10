<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video Upload and Play</title>
</head>
<body>
    <h1>Upload and Play Video</h1>
    <form action="#" method="post" enctype="multipart/form-data">
        <input type="file" id="videoFile" accept="video/*" onchange="playVideo(this)">
    </form>
    <video id="videoPlayer" width="600" controls></video>

    <script>
        function playVideo(input) {
            const file = input.files[0];
            const videoPlayer = document.getElementById('videoPlayer');
            if (file) {
                const url = URL.createObjectURL(file);
                videoPlayer.src = url;
            }
        }
    </script>
</body>
</html>
