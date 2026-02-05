()">استبدال</button>
            </div>
        </div>
    </div>

</div>

<script>
let points = localStorage.getItem("points") || 0;
points = parseInt(points);
document.getElementById("points").textContent = points;

function savePoints() {
    localStorage.setItem("points", points);
    document.getElementById("points").textContent = points;
}

function addPoints() {
    points += 10;
    savePoints();
}

function watchAd() {
    points += 20;
    savePoints();
    alert("✅ تم إضافة 20 نقطة");
}

function redeem() {
    if (points >= 200) {
        points -= 200;
        savePoints();
        alert("🎉 تم استبدال المكافأة بنجاح");
    } else {
        alert("❌ لا تملك نقاط كافية");
    }
}
</script>

</body>
</html>

