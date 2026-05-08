<div style="display:flex; justify-content:center;">
    <div class="flashlight-container">
        <img src="../img/filtered.png" class="flashlight-image" id="flashlightImg">
        <div class="flashlight-overlay" id="overlay"></div>
    </div>
</div>
<style>
.flashlight-container {
    position: relative;
    display: inline-block;
}

.flashlight-image {
    display: block;
    width: 100%;
    max-width: 1080px;
}

.flashlight-overlay {
    position: absolute;
    inset: 0;
    pointer-events: none;
}
</style>

<script>
const container = document.querySelector(".flashlight-container");
const overlay = document.getElementById("overlay");
const img = document.getElementById("flashlightImg");

const BASE_WIDTH = 1080;   // the max-width / design width
const BASE_RADIUS = 90;    // intended radius at full size

function getScaledRadius() {
    return (img.getBoundingClientRect().width / BASE_WIDTH) * BASE_RADIUS;
}

function updateFlashlight(x, y) {
    const r = getScaledRadius();
    overlay.style.background = `
        radial-gradient(
            circle ${r}px at ${x}px ${y}px,
            transparent 0,
            transparent ${r}px,
            rgba(0,0,0,0.4) ${r}px,
            rgba(0,0,0,0.4) 100%
        )
    `;
}

container.addEventListener("mousemove", (e) => {
    const rect = container.getBoundingClientRect();
    updateFlashlight(e.clientX - rect.left, e.clientY - rect.top);
});

updateFlashlight(200, 200);
</script>