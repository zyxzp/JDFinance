<template lang="html">
    <div>
        <Heador/>
        <!-- <Slider/> -->
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
// import Slider from "./rslider.vue"

export default {
    components: {
        Heador,
        Footor,
        Navbar,
        // Slider,
    },
}
</script>
<style lang="scss">
</style>