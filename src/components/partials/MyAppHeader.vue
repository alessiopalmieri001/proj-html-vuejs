<script >
    export default{
        data() {
            return {
                Image:
                [
                    {
                        maxCoach:'/dark-logo.png',
                        href:'#',
                    }
                ],
                mainLink:
                [
                    {
                        scrollBarheader:'Home',
                        dropDown: 
                        [
                            {
                                hLink: 'MaxCoach Education ',
                                href:'#'
                            },
                            {
                                hLink: 'Course Portal ',
                                href:'#'
                            },
                            {
                                hLink: 'Distant Learning ',
                                href:'#'
                            },
                            {
                                hLink: 'Multimedia Pedagogy ',
                                href:'#'
                            },
                            {
                                hLink: 'Modern Scholling ',
                                href:'#'
                            },
                            {
                                hLink: 'Remote Training ',
                                href:'#'
                            },
                            {
                                hLink: 'Health Coaching',
                                href:'#'
                            },
                            {
                                hLink: 'Gym coaching',
                                href:'#'
                            },
                            {
                                hLink: 'Business ',
                                href:'#'
                            },
                            {
                                hLink: 'Artist',
                                href:'#'
                            },
                            {
                                hLink: 'Kitchen Coach ',
                                href:'#'
                            },
                            {
                                hLink: 'Motivation ',
                                href:'#'
                            },
                            {
                                hLink: 'Dancing ',
                                href:'#'
                            },
                            {
                                hLink: 'Guitar ',
                                href:'#'
                            },
                            {
                                hLink: 'yoga ',
                                href:'#'
                            },
                            {
                                hLink: 'Photography ',
                                href:'#'
                            },
                            {
                                hLink: 'Personal Finance ',
                                href:'#'
                            },
                            {
                                hLink: 'Sales coaching ',
                                href:'#'
                            },
                            {
                                hLink: 'Mental therapy ',
                                href:'#'
                            },
                            

                        ],
                    },
                    {
                        scrollBarheader:'Pages',
                        dropDown: 
                        [
                            {
                                hLink: 'Start Here',
                                href:'/'
                            },
                            {
                                hLink: 'Success Story ',
                                href:'#'
                            },
                            {
                                hLink: 'About me',
                                href:'#'
                            },
                            {
                                hLink: 'About us 01 ',
                                href:'#'
                            },
                            {
                                hLink: 'About us 02 ',
                                href:'#'
                            },
                            {
                                hLink: 'About us 03 ',
                                href:'#'
                            },
                            {
                                hLink: 'Concact me',
                                href:'#'
                            },
                            {
                                hLink: 'Contact us',
                                href:'#'
                            },
                            {
                                hLink: ' Purchase Guide',
                                href:'#'
                            },
                            {
                                hLink: 'Privacy Policy',
                                href:'#'
                            },
                            {
                                hLink: 'Teams of Service ',
                                href:'#'
                            },
                            
                            

                        ],
                    },       
                    {
                        scrollBarheader:'Courses',
                        dropDown: 
                        [
                            {
                                hLink: 'Courses Grid 01',
                                href:'#'
                            },
                            {
                                hLink: 'Courses Grid 02 ',
                                href:'#'
                            },
                            {
                                hLink: 'Courses Grid 03',
                                href:'#'
                            },
                            {
                                hLink: 'Memberships Levels',
                                href:'#'
                            },
                            {
                                hLink: 'Become a Teacher',
                                href:'#'
                            },
                            {
                                hLink: 'Profile ',
                                href:'#'
                            },
                            {
                                hLink: 'Checkout',
                                href:'#'
                            },
                            {
                                hLink: 'Single Layout',
                                href:'#',
                                dropdownTwo:
                                [
                                    {
                                        product:'Free course',
                                    },
                                    {
                                        product:'Sticky features bar',
                                    },
                                    {
                                        product:'Standard sidebar',
                                    },
                                    {
                                        product:'No sidebar',
                                    },

                                ],
                            },
                        ],
                    },   
                    {
                        scrollBarheader:'Features',
                        dropDown: 
                        [
                            {
                                hLink: 'Events',
                                href:'#'
                            },
                            {
                                hLink: 'Zoom Meetings ',
                                href:'#'
                            },
                            
                        ],
                    }, 
                    {
                        scrollBarheader:'Blog',
                        dropDown: 
                        [
                            {
                                hLink: 'Blog Grid',
                                href:'#'
                            },
                            {
                                hLink: 'Blog Masonry',
                                href:'#'
                            },
                            {
                                hLink: 'Blog Classic',
                                href:'#'
                            },
                            {
                                hLink: 'Blog List',
                                href:'#'
                            },
                            
                        ],
                    },   
                    {
                        scrollBarheader:'Shop',
                        dropDown: 
                        [
                            {
                                hLink: 'Shop left sidebar',
                                href:'#'
                            },
                            {
                                hLink: 'Shop right sidebar ',
                                href:'#'
                            },
                            {
                                hLink: 'Cart',
                                href:'#'
                            },
                            {
                                hLink: 'Wishlist',
                                href:'#'
                            },
                            {
                                hLink: 'Single Product',
                                href:'#',
                                
                            },
                            
                        ],
                    },   
                        
                ],
            };
        },
        methods: {

        }
    }
</script>

<template>
    <header class="sticky-top ">
        <div class="container">
            <nav class="d-flex  align-items-center ">
                <!-- primo blocco header -->
                <div class="flex-grow-1">
                    <img src="/dark-logo.png" alt="#">
                </div>
                <!-- secondo blocco header -->
                <div class="navbar">
                    <div v-for="elem in mainLink" class="dropdown">
                        <div class="dropbtn">
                            {{elem.scrollBarheader}}
                        </div>
                        <!--Main Dropdown -->
                        <div>
                            <ul v-if="elem.scrollBarheader != 'Home'" class="dropdown-one">
                                <li v-for="index in elem.dropDown" id="link1" class="dItem" >
                                    <a href="/">
                                        {{ index.hLink }}
                                    </a>
                                    <!--Inside Dropdown -->
                                    <ul v-if="index.hLink == 'Single Layout'" class="dropdown-two">
                                        <li v-for="products in index.dropdownTwo" class="dItem" id="file" href="#">
                                            <a href="/">
                                                {{ products.product }}
                                            </a>
                                        </li>
                                    </ul>
                                </li>
                            </ul>
                            
                            <ul v-else class="pippo row">
                                <li v-for="index in elem.dropDown" id="link1" class="dItem col-6 flex-wrap " >
                                    <a href="#">
                                        {{ index.hLink }}
                                    </a>
                                </li>
                                <div class="position-absolute imgPosition">
                                    <img id="imgDropdown" src="/homepages-mega-menu-image-alt.jpg" alt="#">
                                </div>
                            </ul>
                            
                            
                        </div>
                        
                        
                    </div> 
                </div>
                <!-- terzo blocco header -->
                <i class="fa-regular fa-circle-user px-3"></i>
                <div class="box">
                    <div class="container-4">
                        <input type="search" id="search" placeholder="Search..." />
                        <button class="icon"><i class="fa fa-search"></i></button>
                    </div>
                </div>
            </nav>
        </div>
    </header>
    
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables.scss" as *;
@use "../../assets/scss/partials/reset.scss" as*;
@use "../../assets/scss/partials/MySecondaryReset.scss" as*;
    header{
        background-color: #ffffff;
        box-shadow: 0px 30px 20px -20px rgba(0,0,0,0.1);
        .container{
            nav{
                padding:0px 0;
                div{
                    
                    img{
                        width: 160px;
                    }

                    

                }
                
            }
        }
    }
    .linkDropdown{
        display: flex;
        div{
            padding: 0 20px;
            
        }
    }
    ////////////////////////////////////////////////

    .container-4{
    overflow: hidden;
    width: 200px;
    vertical-align: middle;
    white-space: nowrap;
    }
    .container-4 input#search{
    width: 200px;
    height: 30px;
    background: #f5f5f5;
    border: none;
    font-size: 10pt;
    float: left;
    color: black;
    padding-left: 15px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    border-radius: 5px;
    }

    .container-4 input#search::-webkit-input-placeholder {
    color: black;
    }
    .container-4 button.icon{
    -webkit-border-top-right-radius: 5px;
    -webkit-border-bottom-right-radius: 5px;
    -moz-border-radius-topright: 5px;
    -moz-border-radius-bottomright: 5px;
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
    border: none;
    background: #f5f5f5;
    height: 30px;
    width: 50px;
    color: $hoverGreen;
    opacity: 0;
    font-size: 10pt;
    -webkit-transition: all .55s ease;
    -moz-transition: all .55s ease;
    -ms-transition: all .55s ease;
    -o-transition: all .55s ease;
    transition: all .55s ease;
    }
    .container-4:hover button.icon, .container-4:active button.icon, .container-4:focus button.icon{
    outline: none;
    opacity: 1;
    margin-left: -50px;
    }
    .container-4:hover button.icon:hover{
        background: $hoverGreen;
        color: #ffffff;
    }
    /////////////////////////////////////
    .dropdown {
        position: relative;
        
    }
    .dropbtn {
            padding: 20px 20px;
            
    }
    .dropdown-one {
        cursor: pointer;
        display: none;
        position: absolute;
        
        background-color: #f9f9f9;
        min-width: 240px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        border-bottom:4px solid $hoverGreen;
    }
    
    .pippo{
        cursor: pointer;
        display: none;
        position: absolute;
        left: -540px;
        
        background-color: #f9f9f9;
        width: 1320px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        border-bottom:4px solid $hoverGreen ;
        height: 420px;

    }

    .dropdown:hover .pippo{
        display: flex;
    }

    .imgPosition{
        top: 130px;
        left: 850px;

        
        #imgDropdown{
            width: 400px;
        }
    }
    
    .dropdown-two {
        cursor: pointer;
        display: none;
        position: absolute;
        left: 240px;
        top: 336px;
        min-width: 160px;
        background-color: #f9f9f9;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        border-bottom:4px solid $hoverGreen ;
    }
    .dropdown:hover .dropdown-one, #link1:hover > .dropdown-two {
        display: block;
    }
    .dropdown-one .dItem {
    color: black;
    padding: 12px 16px;
    display: block;
    text-align: left;
    }
    .dropdown-one .dItem:hover, .dropdown-two a:hover {
        background-color: #ddd;
    }

</style>
