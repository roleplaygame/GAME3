    <div class="buttons">
        <button id="generateMale">生成男生任务</button>
        <button id="generateFemale">生成女生任务</button>
    </div>
    
    <div class="result" id="result">
        <!-- 任务将在这里显示 -->
    </div>
    
    <p class="disclaimer">注意：请确保所有活动都是双方完全自愿，并提前设立安全词</p>
</div>

<script>
    const maleTasks = [
        "跪在地上完成整场游戏",
        "吃女生双脚各二十秒",
        "脱光衣服",
        "让女生扇三个嘴巴",
        "用嘴帮女生脱掉所有衣物",
        "亲吻女生全身",
        "按摩女生私密部位一分钟",
        "69式五分钟",
        "全程称呼女生为'主人'",
        "让女生给男生穿上胸衣"
    ];
    
    const femaleTasks = [
        "让男生舔阴五分钟",
        "脚踩男生脸十秒",
        "任意调教男生五分钟",
        "足交男生五分钟",
        "用嘴给男生喂水",
        "亲咬男生耳垂各一分钟",
        "口交男生五分钟",
        "用流苏拍打男生十下屁股",
        "全程称呼男生为'小奴隶'",
        "说出任意两个指令"
    ];
    
    document.getElementById('generateMale').addEventListener('click', function() {
        generateTask('male');
    });
    
    document.getElementById('generateFemale').addEventListener('click', function() {
        generateTask('female');
    });
    
    function generateTask(gender) {
        const resultDiv = document.getElementById('result');
        resultDiv.innerHTML = '';
        
        const randomIndex = Math.floor(Math.random() * (gender === 'male' ? maleTasks : femaleTasks).length);
        const task = gender === 'male' ? maleTasks[randomIndex] : femaleTasks[randomIndex];
        
        const taskElement = document.createElement('div');
        taskElement.className = `task ${gender}-task`;
        taskElement.innerHTML = `<strong>${gender === 'male' ? '男生任务' : '女生任务'}:</strong> ${task}`;
        
        resultDiv.appendChild(taskElement);
    }
</script># GAME3
