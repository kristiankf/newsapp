<template>
    <nav class="nav-bar">
        <div class="logo">
            <h1>NewsNews</h1>
        </div>
       
        <div class="links">
            <div class="dropdown">
                <a href="javascript:void(0)">My News</a>
                    <div class="dropdown-content">
                        <a href="#">Add News</a>
                        <a href="#">Delete News</a>
                    </div>
            </div>
            <a href="#">Trending</a>
            <a href="#">Local</a>
            <a href="">International</a>
            <a href="">About NewsNews</a>
        </div>
       <div class="search-bar">
         <input type="text" name="search" id="search">
         <input type="submit" value="Browse">
       </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style scoped>
  .nav-bar {
    background: whitesmoke;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    z-index: 1;
}

.logo h1 {
    margin: 0;
    font-size: 30px;
}

input[type=text] {
    /* width: 150px; */
    height: 32px;
    border: 1px solid green;
    border-radius: 5px;
    transition: .3s ease;
    margin: 5px;
    padding: 5px;
}

.search-bar input[type=text]:focus {
    border: 1px solid rgb(255, 83, 83);
    outline: none;
}

input[type=submit] {
    padding: 8px 5px;
    border: none;
    border-radius: 5px;
    background: green;
    color: white;
}

.nav-bar a {
    text-decoration: none;
    padding:  30px 5px;
    color: green;
    transition: .3s ease;
}

.nav-bar a:hover {
    color: rgb(255, 83, 83);
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    position: absolute;
    display: none;
    z-index: 1;
    background: whitesmoke;
    width: 130px;
    top: 51px;
}

.dropdown-content a {
    display: block;
    padding: 5px 5px;
}

.dropdown:hover .dropdown-content {
    display: block;
}

@media screen and (max-width: 900px) {
    .nav-bar {
        flex-direction: column;
        justify-content: unset;
        align-items: unset;
        padding: 0;
        position: unset;
    }
    .links a {
        padding: 8px 10px;
        display: block;
        flex: 100%;
        background-color: #333333;
        text-align: center;
    }
    .dropdown {
        display: block;
    }
    .dropdown-content {
         position: relative;
         display: block;
         z-index: 1;
         background: whitesmoke;
         width: 100%;
         top: 0;
    }
    .logo {
        display: none;
    }
    .search-bar {
        padding: 5px;
        text-align: right;
    }

    .links a:hover {
        background: #444;
    }

}

</style>