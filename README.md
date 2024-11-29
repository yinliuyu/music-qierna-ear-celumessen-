# music-qierna-ear-celumessen-
<audio id="music" controls>
    <source src="https://drive.google.com/uc?export=download&id=1QUKUBMwBDBnQKlwSxqUytlnbCQ-Ir4wq " type="audio/mp3">
</audio>

<div id="cd-container">
    <div id="cd"></div>
</div>

#cd-container {
    position: relative;
    width: 200px;
    height: 200px;
    margin: 20px auto;
}

#cd {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 50%;
    background: url('https://images.plurk.com/6zLM4bsHPnN12y8ncXUFXm.png ') center/cover no-repeat;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    transition: transform 0.3s ease;
}

/* 控制旋轉 */
.rotate {
    animation: spin 2s linear infinite;
}

@keyframes spin {
    from {
        transform: rotate(0deg);
    }
    to {
        transform: rotate(360deg);
    }
}

const music = document.getElementById('music');
const cd = document.getElementById('cd');

music.onplay = function() {
    cd.classList.add('rotate');  // 當音樂開始播放，開始旋轉
};

music.onpause = function() {
    cd.classList.remove('rotate');  // 當音樂暫停，停止旋轉
};

music.onended = function() {
    cd.classList.remove('rotate');  // 當音樂結束，停止旋轉
};
