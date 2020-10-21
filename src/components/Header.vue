<template>
    <header class="container">
        <div class="header-top">
            <div class="logo">
                <h4>On-line shop</h4>
            </div>
            <div class="search">
                <form>
                    <input type="text" placeholder="Search products, brands and more">
                    <button class="btn-search"><i class="fas fa-search"></i></button>
                </form>
            </div>
            <ul class="header-icons">
                <a class="user-icon">
                    <i class="ti-user"></i>
                    <p>Acoount</p>
                </a>
                <a class="shopping">
                    <i class="ti-shopping-cart"></i>
                    <p>Cart</p>
                    <span>3</span>
                </a>
            </ul>
            <button class="btn-menu"><i class="ti-menu"></i></button>
        </div>
        <div class="navbar">
            <ul class="desktop-menu">
                <li>
                    <div class="categories-links">
                        <a href="">Mobiles</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Smartphones</h4>
                            <a href="">Apple</a>
                            <a href="">Samsung</a>
                            <a href="">Motorola</a>
                            <a href="">Sony</a>
                        </li>
                        <li class="column-two">
                            <h4>Accessories</h4>
                            <a href="">Storage</a>
                            <a href="">Cables</a>
                            <a href="">Screen Protectors</a>
                        </li>
                    </ul>
                </li>
                <li>
                    <div class="categories-links">
                        <a href="">Tv & audio</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Full HD</h4>
                            <a href="">Philips</a>
                            <a href="">Samsung</a>
                            <a href="">LG</a>
                            <a href="">TCL</a>
                        </li>
                        <li class="column-two">
                            <h4>Smart TV</h4>
                            <a href="">Philips</a>
                            <a href="">Samsung</a>
                            <a href="">LG</a>
                            <a href="">TCL</a>
                        </li>
                    </ul>
                </li>
                <li>
                    <div class="categories-links">
                        <a href="">Computer</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Laptops</h4>
                            <a href="">Gaming</a>
                            <a href="">Office</a>
                            <a href="">Touchscreen</a>
                            <a href="">Ultrabooks</a>
                        </li>
                        <li class="column-two">
                            <h4>Desktops</h4>
                            <a href="">Windows</a>
                            <a href="">Linux</a>
                            <a href="">Office</a>
                            <a href="">Gaming</a>
                        </li>
                    </ul>
                </li>
                <li>
                    <div class="categories-links">
                        <a href="">Photo & camera</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Cameras</h4>
                            <a href="">Digital srl</a>
                            <a href="">Instant Film </a>
                            <a href="">Mirrorless</a>
                            <a href="">Waterproof</a>
                        </li>
                        <li  class="column-two">
                            <h4>Camcorders</h4>
                            <a href="">GoPro Cameras</a>
                            <a href="">Sports & Action</a>
                            <a href="">Traditional</a>
                            <a href="">Photo Accessories</a>
                        </li >
                    </ul>
                </li>
                <li>
                    <div class="categories-links">
                        <a href="">Computer accessories</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Accessories</h4>
                            <a href="">Keyboards</a>
                            <a href="">Speakers</a>
                            <a href="">Mouse</a>
                            <a href="">Web cam</a>
                        </li>
                        <li class="column-two">
                            <h4>Accessories</h4>
                            <a href="">Stabilizers</a>
                            <a href="">Pendrives</a>
                            <a href="">Pads</a>
                            <a href="">Headphones</a>
                        </li>
                    </ul>
                </li>
                <li>
                    <div class="categories-links">
                        <a href="">My account</a>
                        <i class="fas fa-plus"></i>
                        <i class="fas fa-minus"></i>
                    </div>
                    <ul class="submenu">
                        <li class="column-one">
                            <h4>Accessories</h4>
                            <a href="">Keyboards</a>
                            <a href="">Speakers</a>
                            <a href="">Mouse</a>
                            <a href="">Web cam</a>
                        </li>
                        <li class="column-two">
                            <h4>Accessories</h4>
                            <a href="">Stabilizers</a>
                            <a href="">Pendrives</a>
                            <a href="">Pads</a>
                            <a href="">Headphones</a>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </header>
</template>
<script>
export default {
    mounted(){
        var btnMenu=document.querySelector('.btn-menu')
        var menu=document.querySelector('.desktop-menu')
        btnMenu.addEventListener('click',function(){
            menu.classList.toggle('active')
        })
        var links=document.getElementsByClassName('categories-links')
        for(let i=0;i<links.length;i++){
            links[i].addEventListener('click',()=>{
                var submenu=links[i].nextElementSibling;
                var btnIcon=links[i].children[1];
                btnIcon.classList.toggle('active')
                submenu.classList.toggle('active')
            })
        }
        window.addEventListener('scroll',function(){
            var header=document.querySelector('header')
            if(window.pageYOffset>3 && window.innerWidth<=739){
                header.classList.add('sticky')
            }else{
                header.classList.remove('sticky')
            }
        })
    }
}
</script>