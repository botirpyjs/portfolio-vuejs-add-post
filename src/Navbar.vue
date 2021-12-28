<template>
    <div>
        <!-- <h1>
            <p>
                Count: <strong>{{ count }}</strong>
            </p>
            <button class="btn btn-success" v-on:click="increment">Increment</button>
            <button class="btn btn-primary" v-on:click="decrement">Decrement</button>
        </h1> -->
        <!-- <div class="comment">
            <div><b>Name:</b> Botir</div>
        </div> -->
        <!-- <center>
            <h1>Navbar qismi </h1>
        </center>
        <header>
            <div class="logo">
                <span class="lg">LogoMak</span>
            </div>
            <div class="menu">
                <span class="menu1">Home</span>
                <span class="menu1">About</span>
                <span class="menu1">Info</span>
                <span class="menu1">Contact</span>
                <span class="menu1">Login</span>
            </div>
        </header>
        <h1>for sikldagi holat</h1> -->
        <div class="bola" v-for="bola in bolalar">
            <div>Hurmatli {{ bolalar.name }}, siz {{ bolalar.yoshi }} yoshda {{ bolalar.kasbi }}ni egalladingiz!</div>
            <div>Hurmatli {{ bolalar.name }}, siz {{ bolalar.yoshi }} yoshda {{ bolalar.kasbi }}ni egalladingiz!</div>
            <div>Hurmatli {{ bolalar.name }}, siz {{ bolalar.yoshi }} yoshda {{ bolalar.kasbi }}ni egalladingiz!</div>
            <div>Hurmatli {{ bolalar.name }}, siz {{ bolalar.yoshi }} yoshda {{ bolalar.kasbi }}ni egalladingiz!</div>
        </div>
        
    </div>
</template>
<script>
export default {
    data() {
        return {
            // count: 0,
            bolalar: [
                {name: 'Ibrohim', kasbi: 'Dasturchi', yoshi: 17},
                {name: 'Bobur', kasbi: 'Nonvoy', yoshi: 20},
                {name: 'Komil', kasbi: 'Dizayner', yoshi: 22},
                {name: 'Ilxom', kasbi: 'Hofiz', yoshi: 19}
            ]
        }
    },
        methods: {
            increment(){
                this.count += 1
            },
            decrement(){
                this.count -= 1
            }
        },
    
}
</script>
<style>
header{
    display: flex;
    justify-content: space-around;
    background-color: #444;
    padding-top: 20px;
    padding-bottom: 20px;
}
.menu{
    color: white;
    font-size: 20px;
    margin-left: 500px;
    border-left: coral 1px solid;
    border-right: coral 1px solid;
}
.logo{
    color: white;
    font-family: cursive;
    font-size: 20px;
}
.menu1{
    padding-top: 10px;
    padding-bottom: 10px;
    cursor: pointer;
    padding-left: 15px;
    padding-right: 15px;
}
.menu1:hover{
    transition: .5s all ease;
    color: coral;
}
</style>