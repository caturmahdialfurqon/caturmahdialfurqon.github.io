---
layout: post
title: Video Playlist Gallery
date: 2024-07-08 03:15:44 +07:00
categories: [Script , Tools]
tags: [PHP,script]
description: Create A Responsive Video Playlist Gallery Using HTML - CSS - Javascript
image: assets/img/Post/video-playlist-gallery/lewiscapaldi.gif
alt: "image alt text"
comments: true
---

# Video-Playlist-Gallery

## Create A Responsive Video Playlist Gallery Using HTML - CSS - Javascript

This script written with php can Instantly Create a single `HTML` file including `CSS` and `JAVASCRIPT`.
For Your Video Gallery, also you can watch it Offline on your browser.

## `Source` CODE

```php
<?php
system('clear');

$directory = readline("Enter Directory Path Here => ");
$titledisplay = readline("Enter Title Bar for Your HTML file => ");

if (!is_dir($directory)) {
    die("Error: Directory '$directory' does not exist.");
}

$handle = opendir($directory);
$videoList = [];

while (($file = readdir($handle)) !== false) {
    if (in_array($file, ['.', '..']) || !preg_match('/\.mp4$/i', $file)) {
        continue;
    }

    $title = str_replace(".mp4", "", $file);
    $video = [
        "title" => $title,
        "source" => "$directory/$file"
    ];

    $found = false;
    foreach ($videoList as $item) {
        if (strtolower($item["title"]) === strtolower($title)) {
            $found = true;
            break;
        }
    }

    if (!$found) {
        $videoList[] = $video;
    }
}

usort($videoList, function($a, $b) {
    return strcasecmp($a['title'], $b['title']);
});

closedir($handle);

$html = "<!DOCTYPE html>
<html lang=\"en\">
<head>
    <meta charset=\"UTF-8\">
    <meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">
    <title>$titledisplay</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            text-transform: capitalize;
            font-family: sans-serif;
            font-weight: normal;
        }
        body {
            background: #000033;
            color: rgba(255, 255, 255, 0.95);
        }
        .heading {
            color: #eee;
            font-size: 40px;
            text-align: center;
            padding: 10px;
        }
        .container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 15px;
            align-items: flex-start;
            padding: 5px 5%;
        }
        .container .main-video {
            background: #152057;
            border-radius: 5px;
            padding: 10px;
        }
        .container .main-video video {
            width: 100%;
            border-radius: 5px;
            aspect-ratio: 16 / 9;
        }
        .container .main-video .title {
            color: rgba(255, 255, 255, 0.95);
            font-size: 23px;
            padding-top: 15px;
            padding-bottom: 15px;
        }
        .container .video-list {
            background: #0000;
            border-radius: 5px;
            height: 720px;
            overflow-y: auto;
        }
        .container .video-list::-webkit-scrollbar {
            width: 7px;
        }
        .container .video-list::-webkit-scrollbar-track {
            background: #ccc;
            border-radius: 50px;
        }
        .container .video-list::-webkit-scrollbar-thumb {
            background: #666;
            border-radius: 50px;
        }
        .container .video-list .vid video {
            width: 100px;
            border-radius: 5px;
            aspect-ratio: 16 / 9;
        }
        .container .video-list .title {
            color: rgba(255, 255, 255, 0.95);
            font-size: 10px;
        }
        .container .video-list .vid {
            display: flex;
            align-items: center;
            gap: 15px;
            background: #152057;
            border-radius: 5px;
            margin: 10px;
            padding: 10px;
            border: 1px solid rgba(0,0,0,.1);
            cursor: pointer;
        }
        .container .video-list .vid:hover {
            background: #1C63B2;
        }
        .container .video-list .vid.active {
            background: #FF0000;
        }
        @media (max-width: 991px) {
            .container {
                grid-template-columns: 2fr 1fr;
                padding: 10px;
            }
        }
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <h3 class=\"heading\">$titledisplay</h3>
    <div class=\"container\">
        <div class=\"main-video\">
            <div class=\"video\">
                <video src=\"\" controls></video>
                <h3 class=\"title\"></h3> 
            </div>
        </div>
        <div class=\"video-list\">";

foreach ($videoList as $video) {
    $html .= "
            <div class=\"vid\">
                <video>
                    <source src=\"{$video["source"]}\" type=\"video/mp4\">
                    Your browser does not support the video tag.
                </video>
                <h3 class=\"title\">{$video["title"]}</h3>
            </div>";
}

$html .= "
        </div>
    </div>
    <script>
        let listVideo = document.querySelectorAll('.video-list .vid');
        let mainVideo = document.querySelector('.main-video video');
        let title = document.querySelector('.main-video .title');

        listVideo.forEach(video => {
            video.onclick = () => {
                listVideo.forEach(vid => vid.classList.remove('active'));
                video.classList.add('active');
                if (video.children[0].children[0].getAttribute('src')) {
                    mainVideo.src = video.children[0].children[0].getAttribute('src');
                }
                title.innerHTML = video.children[1].innerHTML;
            }
        });
    </script>
</body>
</html>";

$fileNamex = readline("Enter your file name *without .html* => ");
$fileName = "$fileNamex.html";
$filePath = "$directory/$fileName";

$fileHandle = fopen($filePath, "w") or die("Error: Could not open file '$filePath' for writing.");
fwrite($fileHandle, $html);
fclose($fileHandle);

echo "Generated HTML file saved to: $filePath";
?>
```

## Here The Screenshot

![video playlist galery](assets/img/Post/video-playlist-gallery/lewiscapaldi.png)


## For Older Version

Visit My Github Repository Here : [SINGLE-FILE-HTML-OFFLINE-GALERY-OR-VIDEOS ](https://github.com/caturmahdialfurqon/SINGLE-FILE-HTML-OFFLINE-GALERY-OR-VIDEOS)