<script>
import NavBar from "./components/NavBar.vue";
import Spinner from "./components/Spinner.vue";
import { BContainer } from "bootstrap-vue";
import Footer from "./components/Footer.vue";
export default {
    name: "App",
    render() {
        return (
            <div id="app">
                <NavBar />
                <BContainer class="router-container" fluid>
                    <router-view />
                </BContainer>
                <Spinner />
                <Footer />
            </div>
        );
    }
};
</script>

<style lang="scss">
@import "~bootstrap";
@import "~bootstrap-vue";
@import "../node_modules/prismjs/themes/prism.css";

body {
    background-color: var(--secondary);
}

button:disabled,
.custom-select:disabled {
    cursor: not-allowed;
}

.btn.btn-primary {
    box-shadow: 0 0.25rem 0.25rem rgba(0, 0, 0, 0.25),
        inset 0 -1px 5px rgba(0, 0, 0, 0.25);
}

.custom-select {
    appearance: none;
}

* {
    outline: none;
}

#app {
    background-color: var(--secondary);
    height: calc(100vh);
    width: 100vw;
}

.router-container {
    padding-top: 71px;
    padding-bottom: 15px;
    height: calc(100vh);
}
</style>
