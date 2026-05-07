### Pearl practice

Hover over the map to practice a tier1 pearl.

<div style="display:flex; justify-content:center;">
    <div class="flashlight-container">
        <img src="../img/filtered.png" class="flashlight-image">
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

function updateFlashlight(x, y) {
    overlay.style.background = `
        radial-gradient(
            circle 90px at ${x}px ${y}px,
            transparent 0,
            transparent 90px,
            rgba(0,0,0,0.4) 90px,
            rgba(0,0,0,0.4) 100%
        )
    `;
}

container.addEventListener("mousemove", (e) => {
    const rect = container.getBoundingClientRect();

    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;

    updateFlashlight(x, y);
});

updateFlashlight(200, 200);
</script>