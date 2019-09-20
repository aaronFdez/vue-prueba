import Vue from 'vue'
import Router from 'vue-router'
import LoginComponent from "./views/login.vue"
import auth from "./views/auth.vue"

Vue.use(Router)

export default new Router({
    routes: [
        {
            path: '/',
            redirect: {
                name: "login"
            }
        },
        {
            path: "/login",
            name: "login",
            component: LoginComponent
        },
        {
            path: "/auth",
            name: "auth",
            component: SecureComponent
        }
    ]
})