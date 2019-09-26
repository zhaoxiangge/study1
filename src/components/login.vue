<template>
    <div id = 'login'>
        <div class="card">
            <h3>登录之后更精彩</h3>
                <input type="email" id = 'email' name = 'email' ref = 'email' required='required'>
                <input type="password" id = 'password' name = 'password' ref = 'password'>
                <button @click = 'sub'>登录</button>
            <ul>
                <li><router-link to = '/'>注册</router-link></li>
                <li><a href="#">忘记密码</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  methods: {
    sub () {
      console.log(this.$refs.email.value)
      console.log(this.$refs.password.value)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped  lang = 'scss'>
$main-color:#2ecc71;
$second-color:#27ae60;
$line-color:#ddd;
$dark-color:#333;
    #login{
    display:flex;
    justify-content: center;
    align-items: center;
    position: relative;
    min-height: 100vh;
    background: url(../../static/img/timg.jpg) no-repeat center center/cover;
    &::after{
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        background: $main-color;
        opacity: .5;
    }
    .card{
        clear: both;
        width: 400px;
        padding: 2rem 3rem;
        background:#fff;
        h3{
            color: $second-color;
            margin-top: 1rem;
            font-weight: 400;
        }
        input{
            display: block;
            width: 100%;
            padding: .5rem;
            margin-top: 1rem;
            border: 1px solid $line-color;
            &:focus{
                outline: 1px solid $main-color;
            }
        }
        button{
                display: block;
                width: 100%;
                padding: .5rem;
                margin-top: 1rem;
                border: 1px solid $line-color;
                color: #fff;
                background: $second-color;
                transition: all .5s;
                &:hover{
                    background: $main-color;
                }
            }
        ul{
            list-style: none;
            display: flex;
            justify-content: space-between;
            font-size: .9rem;
            li a{
                color:$dark-color;
                text-decoration: none;
                transition: all .5s;
                &:hover{
                    color: $main-color;
                    border: 1px solid $main-color;
                }
            }
        }
    }
}
</style>
