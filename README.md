# frontend_masters_semi_auto_download
A short js script that help you download video from Frontend masters courses.

- Enter to the course page.
- Open your dev tools.
- Past the folloing script.
- Start chasing the new tabs that will pop all over the place.
- Download the video in each tab.

```js
const lesson =  Array.from( document.getElementsByClassName('lesson'));
let count = 0;
let video = document.getElementById('vjs_video_3_html5_api');


let inter = setInterval( ()=>{
    if(count < lesson.length){
        console.log(count);
        
        video = document.getElementById('vjs_video_3_html5_api');
        window.open( video.currentSrc , '_blank');
        
        count++;
        lesson[count].click();
    }
    else{
        clearInterval(inter);
    }
}, 2000)
```

- Keep learning!
