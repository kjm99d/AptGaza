<template>
    <div id="map" style="width:100%; height:100vh;">
    </div>
</template>

<script>
export default {
    data() {
        return {
            map: null
        }
    },
    methods: {
        initMap() {
            const container = document.getElementById('map');
                const options = {
                    center: new window.kakao.maps.LatLng(37.5665, 126.9780),
                    level: 3
                };
                console.log(container, options)
                this.map = new window.kakao.maps.Map(container, options)
        }
    },
    mounted() {
        const script = document.createElement("script")
        const KakaoJavaScriptAppKey = process.env.VUE_APP_KAKAO_MAP_APPKEY
        console.log(KakaoJavaScriptAppKey)
        script.src = "//dapi.kakao.com/v2/maps/sdk.js?appkey=" + KakaoJavaScriptAppKey + "&libraries=services&autoload=false"
        
        document.head.appendChild(script)

        script.addEventListener("load", () => {
            console.log("loaded !")
            window.kakao.maps.load(this.initMap)
        })
    }
}
</script>
