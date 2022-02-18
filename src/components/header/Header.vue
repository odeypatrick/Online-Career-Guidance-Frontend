<template>
    <header>
        <div class= "container">
            <div class="main-header">
                <div class="logo">
                    <h1>G&C</h1>
                </div>

                <div class="links">
                    <nav>
                        <ul>
                            <li><a href="login/login.html"> <i class="fa fa-user"></i> Login/signup</a></li>
                            <li><a href="#" class="btn">GET STARTED</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped>
    header {
    padding: 10px;
    position: sticky;
    width: 100%;
    background: #111;
    top:0;
    left: 0;
    color: #fff;
}

.main-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.fa-user {
    font-size: 20px;
}

.links li {
    display: inline-block;
    list-style: none;
}

.links li a {
    padding: 10px;
    text-decoration: none;
    color: #000;
    font-size: 14px;
    color: #fff;
}

.links .btn {
    background-color: #123b99;
    font-weight: bold;
    color: #fff;
    font-family: inherit;
    border-radius: 5px;
}
</style>