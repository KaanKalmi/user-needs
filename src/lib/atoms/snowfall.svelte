<div class="snow"></div>

<style>
    .snow, .snow:before, .snow:after {
        pointer-events: none;
        position: absolute;
        top: -1000px;
        left: 0;
        bottom: 0;
        right: 0;
        overflow: hidden;
        background-image: radial-gradient(6px 6px at 159px 560px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)), 
            radial-gradient(4px 4px at 209px 543px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)), 
            radial-gradient(3px 3px at 519px 253px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)), 
            radial-gradient(5px 5px at 236px 208px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 427px 429px, rgb(0, 0, 0, 0.8) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(3px 3px at 272px 439px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 367px 211px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(5px 5px at 475px 160px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(3px 3px at 547px 354px, rgb(0, 0, 0, 1) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(6px 6px at 236px 538px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 426px 145px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(6px 6px at 291px 51px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 434px 180px, rgb(0, 0, 0) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(3px 3px at 401px 15px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(5px 5px at 108px 328px, rgb(0, 0, 0, 0.9) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 325px 242px, rgb(0, 0, 0, 0.6) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(3px 3px at 83px 135px, rgb(0, 0, 0, 0.7) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(5px 5px at 431px 526px, rgb(0, 0, 0, 0.7) 50%, rgb(0, 0, 0, 0)),
            radial-gradient(4px 4px at 114px 155px, rgb(0, 0, 0) 50%, rgb(0, 0, 0, 0));       
        background-size: 600px 600px;
        animation: snow 6s linear infinite;
        content: "";
        z-index: 1;
    }
    .snow:after { 
        margin-left: -200px;
        opacity: 0.4;
        animation-duration: 12s;
        animation-direction: reverse;
        filter: blur(3px);
    }
    .snow:before {
        animation-duration: 9s;
        animation-direction: reverse;
        margin-left: -300px;
        opacity: 0.65;
        filter: blur(1.5px);
    }
 @keyframes snow { to { transform: translateY(1000px); } }
</style>