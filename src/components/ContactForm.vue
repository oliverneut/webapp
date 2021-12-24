<template>
    <div class="parent">
        <div class="contactform">
            <br>
            <h1>Contact</h1>
            <div class="group">      
                <input type="text" required>
                <span class="highlight"></span>
                <span class="bar"></span>
                <label>name</label>
            </div>
            <div class="group">      
                <input type="text" required>
                <span class="highlight"></span>
                <span class="bar"></span>
                <label>email</label>
            </div>
            <div class="form__group">
                <textarea id="message" class="form__field" placeholder="Your Message" rows="6"></textarea>
                <label for="message" class="form__label">Your Message</label>
            </div>

            <button class="pure-material-button-contained">Send</button>
        </div>
        <div class="social_media">
            <a href="https://github.com/oliverneut" target="_blank" class="fa fa-github"></a>
            <a href="https://twitter.com/NeutOliver" target="_blank" class="fa fa-twitter"></a>
            <a href="https://www.instagram.com/oliverneut/" target="_blank" class="fa fa-instagram"></a>
            <a href="https://www.linkedin.com/in/oliver-neut-28a01a197" target="_blank" class="fa fa-linkedin"></a>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    h1 {
        color: #999;
    }

    .parent {
        text-align: center;
        justify-content: center;
        align-items: center;
        padding-top: 100px;
    }


    .contactform {
        color: white;
        background-color: rgb(14, 14, 14);
        min-height: 600px;
        min-width: 35%;
        max-width: 554.17px;
        border-radius: 20px;
        border: 1px solid rgba(43, 43, 43, 0.7);
        margin: 0 auto;
    }

    .group { 
        top: 50px;
        left: 120px;
        position:relative; 
        margin-bottom:45px; 
    }

    input {
    background-color: rgb(14, 14, 14);
    font-size:18px;
    padding:10px 10px 10px 5px;
    display:block;
    width:300px;
    border:none;
    border-bottom:1px solid #757575;
    color: white;
    }
    input:focus { 
        outline:none; 
    }

    /* LABEL ======================================= */
    label 				 {
    color:#999; 
    font-size:18px;
    font-weight:normal;
    position:absolute;
    pointer-events:none;
    left:5px;
    top:10px;
    transition:0.2s ease all; 
    -moz-transition:0.2s ease all; 
    -webkit-transition:0.2s ease all;
    }

    /* active state */
    input:focus ~ label, input:valid ~ label 		{
    top:-20px;
    font-size:14px;
    color:rgb(72, 186, 175);
    }

    /* BOTTOM BARS ================================= */
    .bar 	{ position:relative; display:block; width:300px; }
    .bar:before, .bar:after 	{
    content:'';
    height:2px; 
    width:0;
    bottom:1px; 
    position:absolute;
    background:#5264AE; 
    transition:0.2s ease all; 
    -moz-transition:0.2s ease all; 
    -webkit-transition:0.2s ease all;
    }
    .bar:before {
    left:50%;
    }
    .bar:after {
    right:50%; 
    }

    /* active state */
    input:focus ~ .bar:before, input:focus ~ .bar:after {
    width:50%;
    }

    /* HIGHLIGHTER ================================== */
    .highlight {
    position:absolute;
    height:60%; 
    width:100px; 
    top:25%; 
    left:0;
    pointer-events:none;
    opacity:0.5;
    }

    /* active state */
    input:focus ~ .highlight {
    -webkit-animation:inputHighlighter 0.3s ease;
    -moz-animation:inputHighlighter 0.3s ease;
    animation:inputHighlighter 0.3s ease;
    }

    /* ANIMATIONS ================ */
    @-webkit-keyframes inputHighlighter {
        from { background:#5264AE; }
    to 	{ width:0; background:transparent; }
    }
    @-moz-keyframes inputHighlighter {
        from { background:#5264AE; }
    to 	{ width:0; background:transparent; }
    }
    @keyframes inputHighlighter {
        from { background:#5264AE; }
    to 	{ width:0; background:transparent; }
    }

    .form__group {
        resize: none;
        top: 70px;
        position: relative;
        padding: 15px 0 0;
        left: 120px;
        max-width: 60%;
        margin-top: 10px;
    }

    .form__field {
    font-family: inherit;
    width: 100%;
    border: 0;
    border-bottom: 1px solid #d2d2d2;
    outline: 0;
    font-size: 16px;
    color: white;
    padding: 7px 0;
    background: transparent;
    transition: border-color 0.2s;
    }

    .form__field::placeholder {
    color: transparent;
    }

    .form__field:placeholder-shown ~ .form__label {
    font-size: 16px;
    cursor: text;
    top: 20px;
    }

    label,
    .form__field:focus ~ .form__label {
    position: absolute;
    top: 0;
    display: block;
    transition: 0.2s;
    font-size: 16px;
    color: #9b9b9b;
    }

    .form__field:focus ~ .form__label {
    color:rgb(72, 186, 175);
    }

    .form__field:focus {
    padding-bottom: 6px;
    border-bottom: 2px solid #5264AE;
    }

    .pure-material-button-contained {
    top: 110px;
    position: relative;
    display: inline-block;
    box-sizing: border-box;
    border: none;
    border-radius: 6px;
    padding: 0 16px;
    min-width: 64px;
    height: 36px;
    vertical-align: middle;
    text-align: center;
    text-overflow: ellipsis;
    text-transform: uppercase;
    color: rgb(var(--pure-material-onprimary-rgb, 255, 255, 255));
    background-color: rgb(var(--pure-material-primary-rgb, 33, 150, 243));
    box-shadow: 0 3px 1px -2px rgba(0, 0, 0, 0.2), 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 1px 5px 0 rgba(0, 0, 0, 0.12);
    font-family: var(--pure-material-font, "Roboto", "Segoe UI", BlinkMacSystemFont, system-ui, -apple-system);
    font-size: 14px;
    font-weight: 500;
    line-height: 36px;
    overflow: hidden;
    outline: none;
    cursor: pointer;
    transition: box-shadow 0.2s;
}

.pure-material-button-contained::-moz-focus-inner {
    border: none;
}

/* Overlay */
.pure-material-button-contained::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgb(var(--pure-material-onprimary-rgb, 255, 255, 255));
    opacity: 0;
    transition: opacity 0.2s;
}

/* Ripple */
.pure-material-button-contained::after {
    content: "";
    position: absolute;
    left: 50%;
    top: 50%;
    border-radius: 50%;
    padding: 50%;
    width: 32px; /* Safari */
    height: 32px; /* Safari */
    background-color: rgb(var(--pure-material-onprimary-rgb, 255, 255, 255));
    opacity: 0;
    transform: translate(-50%, -50%) scale(1);
    transition: opacity 1s, transform 0.5s;
}

/* Hover, Focus */
.pure-material-button-contained:hover,
.pure-material-button-contained:focus {
    box-shadow: 0 2px 4px -1px rgba(0, 0, 0, 0.2), 0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12);
}

.pure-material-button-contained:hover::before {
    opacity: 0.08;
}

.pure-material-button-contained:focus::before {
    opacity: 0.24;
}

.pure-material-button-contained:hover:focus::before {
    opacity: 0.3;
}

/* Active */
.pure-material-button-contained:active {
    box-shadow: 0 5px 5px -3px rgba(0, 0, 0, 0.2), 0 8px 10px 1px rgba(0, 0, 0, 0.14), 0 3px 14px 2px rgba(0, 0, 0, 0.12);
}

.pure-material-button-contained:active::after {
    opacity: 0.32;
    transform: translate(-50%, -50%) scale(0);
    transition: transform 0s;
}

/* Disabled */
.pure-material-button-contained:disabled {
    color: rgba(var(--pure-material-onsurface-rgb, 0, 0, 0), 0.38);
    background-color: rgba(var(--pure-material-onsurface-rgb, 0, 0, 0), 0.12);
    box-shadow: none;
    cursor: initial;
}

.pure-material-button-contained:disabled::before {
    opacity: 0;
}

.pure-material-button-contained:disabled::after {
    opacity: 0;
}

textarea {
    resize: none;
}


/* social media icons  */

.social_media {
    background-color: rgb(14, 14, 14);
        margin-top: 20px;
        min-height: 80px;
        min-width: 35%;
        max-width: 554.17px;
        border-radius: 20px;
        border: 1px solid rgba(43, 43, 43, 0.7);
        display: inline-block;
        margin: 0 auto;
}


.fa {
padding: 20px;
font-size: 30px;
width: 50px;
text-align: center;
text-decoration: none;
}

.fa-twitter:hover{
    color: #1DA1F2;
}

.fa-instagram:hover{
    color: #F56040;
}

.fa-linkedin:hover{
    color: #2867B2;
}

.fa-github:hover{
    color: #6f42c1;
}

.social_media, .contactform {
    display: block; 
}

</style>