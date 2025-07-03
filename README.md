<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECE Final Sprint Schedule (3/7 - 15/7/2025)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .subject-physics { background-color: #FFEE93; }
        .subject-circuits { background-color: #ADF7B6; }
        .subject-programming { background-color: #A0CED9; }
        .subject-calculus { background-color: #FFC09F; }
        .subject-ielts { background-color: #D8A7B1; }
        .subject-gym { background-color: #e2e8f0; }
        .subject-meal { background-color: #f1f5f9; }
        .subject-sleep { background-color: #cbd5e1; }
        .line-through { text-decoration: line-through; opacity: 0.7; }
        .progress-bar {
            height: 8px;
            background-color: #e2e8f0;
            border-radius: 4px;
        }
        .progress-fill {
            height: 100%;
            border-radius: 4px;
            background-color: #4f46e5;
            transition: width 0.5s ease;
        }
    </style>
</head>
<body class="bg-gray-50 p-6" onload="loadSchedule()">
    <div id="schedule-container" class="max-w-6xl mx-auto">
        <header class="mb-8">
            <h1 class="text-3xl font-bold text-gray-800 mb-2">ECE Final Sprint Schedule</h1>
            <div class="flex items-center justify-between">
                <p class="text-gray-600" id="date-range">3/7/2025 - 15/7/2025 (12 days remaining)</p>
                <div class="flex items-center space-x-4">
                    <div class="text-center">
                        <div class="text-sm text-gray-500">Completed</div>
                        <div class="font-bold text-indigo-600" id="completed-percentage">0%</div>
                    </div>
                    <div class="progress-bar w-32">
                        <div class="progress-fill" style="width: 0%"></div>
                    </div>
                </div>
            </div>
        </header>
        <div class="grid grid-cols-1 md:grid-cols-7 gap-4 mb-6">
            <!-- Legend -->
            <div class="md:col-span-7 bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-2">Subject Legend</h3>
                <div class="flex flex-wrap gap-3 text-sm">
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-physics mr-2"></div> Physics 2</div>
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-circuits mr-2"></div> Electric Circuits</div>
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-programming mr-2"></div> Programming</div>
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-calculus mr-2"></div> Calculus</div>
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-ielts mr-2"></div> IELTS Speaking</div>
                    <div class="flex items-center"><div class="w-4 h-4 rounded-sm subject-gym mr-2"></div> Gym</div>
                </div>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-7 gap-4 mb-10">
            <!-- Daily Schedule -->
            <div id="day-1" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Thu 3/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm subject-block">6:00 - 8:00 Gym</div>
                    <div class="subject-physics p-2 rounded text-sm">9:00 - 11:00 Physics 2</div>
                    <div class="subject-meal p-2 rounded text-sm">11:00 - 12:00 Lunch</div>
                    <div class="subject-circuits p-2 rounded text-sm">13:00 - 15:00 Electric Circuits</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-programming p-2 rounded text-sm">20:00 - 22:00 Programming</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <!-- Repeat for each day with different subject distribution -->
            <!-- Example of day 2 -->
            <div id="day-2" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Fri 4/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-calculus p-2 rounded text-sm">9:00 - 11:30 Calculus</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-programming p-2 rounded text-sm">13:30 - 16:00 Programming</div>
                    <div class="subject-ielts p-2 rounded text-sm">17:00 - 19:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">19:00 - 20:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">21:00 - 23:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">23:00 - 7:00 Sleep</div>
                </div>
            </div>
            <div id="day-3" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Sat 5/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-circuits p-2 rounded text-sm">9:00 - 11:30 Electric Circuits</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-ielts p-2 rounded text-sm">13:30 - 15:30 IELTS Speaking</div>
                    <div class="subject-physics p-2 rounded text-sm">16:00 - 18:00 Physics 2</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-calculus p-2 rounded text-sm">20:00 - 22:00 Calculus</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <div id="day-4" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Sun 6/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:30 - 8:30 Gym</div>
                    <div class="subject-programming p-2 rounded text-sm">9:00 - 11:30 Programming</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-ielts p-2 rounded text-sm">13:30 - 15:30 IELTS Speaking</div>
                    <div class="subject-circuits p-2 rounded text-sm">16:00 - 18:00 Electric Circuits</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">20:00 - 22:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:30 Sleep</div>
                </div>
            </div>
            <div id="day-5" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Mon 7/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-calculus p-2 rounded text-sm">9:00 - 11:30 Calculus</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-physics p-2 rounded text-sm">13:30 - 15:30 Physics 2</div>
                    <div class="subject-programming p-2 rounded text-sm">16:00 - 18:00 Programming</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-ielts p-2 rounded text-sm">20:00 - 22:00 IELTS Speaking</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <div id="day-6" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Tue 8/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-physics p-2 rounded text-sm">9:00 - 11:30 Physics 2</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-circuits p-2 rounded text-sm">13:30 - 15:30 Electric Circuits</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-programming p-2 rounded text-sm">20:00 - 22:00 Programming</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <div id="day-7" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Wed 9/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:30 - 8:30 Gym</div>
                    <div class="subject-programming p-2 rounded text-sm">9:00 - 11:30 Programming</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-calculus p-2 rounded text-sm">13:30 - 15:30 Calculus</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">20:00 - 22:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:30 Sleep</div>
                </div>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-7 gap-4 mb-10">
            <div id="day-8" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Thu 10/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-calculus p-2 rounded text-sm">9:00 - 11:30 Calculus</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-circuits p-2 rounded text-sm">13:30 - 15:30 Electric Circuits</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">20:00 - 22:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <div id="day-9" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Fri 11/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-physics p-2 rounded text-sm">9:00 - 11:30 Physics 2</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-programming p-2 rounded text-sm">13:30 - 15:30 Programming</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-circuits p-2 rounded text-sm">20:00 - 22:00 Electric Circuits</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
            <div id="day-10" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Sat 12/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:30 - 8:30 Gym</div>
                    <div class="subject-programming p-2 rounded text-sm">9:00 - 11:30 Programming</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-calculus p-2 rounded text-sm">13:30 - 15:30 Calculus</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">20:00 - 22:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:30 Sleep</div>
                </div>
            </div>
            <div id="day-11" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Sun 13/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:30 - 8:30 Gym</div>
                    <div class="subject-circuits p-2 rounded text-sm">9:00 - 11:30 Electric Circuits</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-physics p-2 rounded text-sm">13:30 - 15:30 Physics 2</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-programming p-2 rounded text-sm">20:00 - 22:00 Programming</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:30 Sleep</div>
                </div>
            </div>
            <div id="day-12" class="bg-white p-4 rounded-lg shadow-sm">
                <h3 class="font-medium mb-3">Mon 14/7</h3>
                <div class="space-y-2">
                    <div class="subject-gym p-2 rounded text-sm">6:00 - 8:00 Gym</div>
                    <div class="subject-calculus p-2 rounded text-sm">9:00 - 11:30 Calculus</div>
                    <div class="subject-meal p-2 rounded text-sm">11:30 - 12:30 Lunch</div>
                    <div class="subject-programming p-2 rounded text-sm">13:30 - 15:30 Programming</div>
                    <div class="subject-ielts p-2 rounded text-sm">16:00 - 18:00 IELTS Speaking</div>
                    <div class="subject-meal p-2 rounded text-sm">18:00 - 19:00 Dinner</div>
                    <div class="subject-physics p-2 rounded text-sm">20:00 - 22:00 Physics 2</div>
                    <div class="subject-sleep p-2 rounded text-sm">22:00 - 6:00 Sleep</div>
                </div>
            </div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <!-- Study Progress -->
            <div class="bg-white p-6 rounded-lg shadow-sm">
                <h3 class="font-medium mb-4">Study Progress</h3>
                <div class="space-y-4">
                    <div>
                        <div class="flex justify-between text-sm mb-1">
                            <span>Physics 2</span>
                            <span><span id="physics-completed">0</span>/12 hours</span>
                        </div>
                        <div class="progress-bar">
                            <div id="physics-progress" class="progress-fill" style="width: 0%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between text-sm mb-1">
                            <span>Electric Circuits</span>
                            <span><span id="circuits-completed">0</span>/12 hours</span>
                        </div>
                        <div class="progress-bar">
                            <div id="circuits-progress" class="progress-fill" style="width: 0%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between text-sm mb-1">
                            <span>Programming</span>
                            <span><span id="programming-completed">0</span>/12 hours</span>
                        </div>
                        <div class="progress-bar">
                            <div id="programming-progress" class="progress-fill" style="width: 0%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between text-sm mb-1">
                            <span>Calculus</span>
                            <span><span id="calculus-completed">0</span>/12 hours</span>
                        </div>
                        <div class="progress-bar">
                            <div id="calculus-progress" class="progress-fill" style="width: 0%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between text-sm mb-1">
                            <span>IELTS Speaking</span>
                            <span><span id="ielts-completed">0</span>/12 hours</span>
                        </div>
                        <div class="progress-bar">
                            <div id="ielts-progress" class="progress-fill" style="width: 0%"></div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Quick Actions -->
            <div class="bg-white p-6 rounded-lg shadow-sm">
                <h3 class="font-medium mb-4">Quick Actions</h3>
                <div class="grid grid-cols-2 gap-3">
                    <button class="p-3 bg-indigo-50 text-indigo-700 rounded hover:bg-indigo-100 text-sm" onclick="markCurrentDayComplete()">
                        Mark Day Complete
                    </button>
                    <button class="p-3 bg-gray-50 text-gray-700 rounded hover:bg-gray-100 text-sm" onclick="showReschedulePrompt()">
                        Reschedule
                    </button>
                    <button class="p-3 bg-green-50 text-green-700 rounded hover:bg-green-100 text-sm" onclick="addNotePrompt()">
                        Add Note
                    </button>
                    <button class="p-3 bg-red-50 text-red-700 rounded hover:bg-red-100 text-sm" onclick="activateEmergencyMode()">
                        Emergency Mode
                    </button>
                    <button class="p-3 bg-blue-50 text-blue-700 rounded hover:bg-blue-100 text-sm col-span-2" onclick="saveScheduleState()">
                        💾 Save Now
                    </button>
                </div>
            </div>
        </div>
    </div>
    <!-- For GitHub Pages - Simplified storage solution -->
    <script>
        function saveToGitHubStorage() {
            const scheduleData = getScheduleData();
            localStorage.setItem('studySchedule', JSON.stringify(scheduleData));
            return true; // GitHub Pages only supports localStorage
        }
        function loadFromGitHubStorage() {
            const savedData = localStorage.getItem('studySchedule');
            if (savedData) return JSON.parse(savedData);
            return null;
        }
        document.addEventListener('DOMContentLoaded', function() {
            // Commented out - moved to loadSchedule()
            // Make all time blocks editable and completable
            document.querySelectorAll('.subject-gym, .subject-physics, .subject-circuits, .subject-programming, .subject-calculus, .subject-ielts').forEach(item => {
                item.addEventListener('click', function(e) {
                    e.stopPropagation();
                    const action = prompt(`Choose action for "${this.textContent}":
1. Mark as complete
2. Edit time
3. Edit content`, "1");
                    if (action === "1") {
                        this.classList.toggle('line-through');
                        updateProgress();
                        saveScheduleState();
                    } else if (action === "2") {
                        const newTime = prompt("Edit time (format: HH:MM - HH:MM)", this.textContent.split(' ')[0]+' '+this.textContent.split(' ')[1]);
                        if (newTime) {
                            const oldText = this.textContent;
                            const replacement = this.textContent.replace(/^([0-9:]+ - [0-9:]+)/, newTime);
                            this.textContent = replacement;
                        }
                    } else if (action === "3") {
                        const newContent = prompt("Edit content:", this.textContent);
                        if (newContent) this.textContent = newContent;
                    }
                });
            });
            function updateProgress() {
                const subjects = {
                    physics: { completed: 0, total: 12 },
                    circuits: { completed: 0, total: 12 },
                    programming: { completed: 0, total: 12 },
                    calculus: { completed: 0, total: 12 },
                    ielts: { completed: 0, total: 12 }
                };
                document.querySelectorAll('.line-through').forEach(item => {
                    if (item.classList.contains('subject-physics')) subjects.physics.completed++;
                    if (item.classList.contains('subject-circuits')) subjects.circuits.completed++;
                    if (item.classList.contains('subject-programming')) subjects.programming.completed++;
                    if (item.classList.contains('subject-calculus')) subjects.calculus.completed++;
                    if (item.classList.contains('subject-ielts')) subjects.ielts.completed++;
                });
                // Update individual subject progress
                for (const [subject, data] of Object.entries(subjects)) {
                    const percentage = Math.round((data.completed / data.total) * 100);
                    document.getElementById(`${subject}-completed`).textContent = data.completed;
                    document.getElementById(`${subject}-progress`).style.width = percentage + '%';
                }
                // Update overall progress
                const totalCompleted = Object.values(subjects).reduce((sum, s) => sum + s.completed, 0);
                const totalTotal = Object.values(subjects).reduce((sum, s) => sum + s.total, 0);
                const totalPercentage = Math.round((totalCompleted / totalTotal) * 100);
                document.getElementById('completed-percentage').textContent = totalPercentage + '%';
                document.querySelector('.progress-fill').style.width = totalPercentage + '%';
            }
            window.markCurrentDayComplete = function() {
                const today = new Date();
                const dayIndex = (today.getDate() - 3 + 12) % 12 + 1;
                const dayElement = document.getElementById(`day-${dayIndex}`);
                if(dayElement) {
                    dayElement.querySelectorAll('.subject-gym, .subject-physics, .subject-circuits, .subject-programming, .subject-calculus, .subject-ielts').forEach(item => {
                        item.classList.add('line-through');
                    });
                    updateProgress();
                }
            };
            window.showReschedulePrompt = function() {
                const newDate = prompt("Enter new deadline (DD/MM/YYYY):", "15/07/2025");
                if(newDate) {
                    document.querySelector('header p.text-gray-600').textContent = `3/7/2025 - ${newDate} (${Math.ceil((new Date(newDate.split('/').reverse().join('-')) - new Date())/(1000*60*60*24))} days remaining)`;
                }
            };
            window.addNotePrompt = function() {
                const note = prompt("Add a note for today:");
                if(note) {
                    localStorage.setItem('dailyNote', note);
                    alert("Note saved!");
                }
            };
            window.activateEmergencyMode = function() {
                if(confirm("Activate emergency mode? This will prioritize IELTS prep!")) {
                    document.querySelectorAll('.subject-ielts').forEach(el => {
                        el.style.backgroundColor = '#fecaca';
                        el.querySelector('input').placeholder = "INTENSIVE IELTS PRACTICE";
                    saveScheduleState();
                    });
                }
            };
            function getScheduleData() {
                const today = new Date();
                const daysLeft = Math.ceil((new Date('2025-07-15') - today)/(1000*60*60*24));
                document.getElementById('date-range').textContent = 
                    `3/7/2025 - 15/7/2025 (${daysLeft} days remaining)`;
                return {
                    lastSaved: new Date().getTime(),
                    completedItems: Array.from(document.querySelectorAll('.line-through'))
                        .map(el => el.textContent),
                    progressData: {
                        physics: document.getElementById('physics-completed').textContent,
                        circuits: document.getElementById('circuits-completed').textContent,
                        programming: document.getElementById('programming-completed').textContent,
                        calculus: document.getElementById('calculus-completed').textContent,
                        ielts: document.getElementById('ielts-completed').textContent
                    }
                };
            }
            function saveScheduleState() {
                saveToGitHubStorage();
                // Show save confirmation
                const saveMsg = document.createElement('div');
                saveMsg.textContent = 'Schedule saved permanently!';
                saveMsg.className = 'fixed bottom-4 right-4 bg-green-500 text-white px-4 py-2 rounded-md';
                document.body.appendChild(saveMsg);
                setTimeout(() => saveMsg.remove(), 2000);
            }
            function loadSchedule() {
                const savedData = loadFromGitHubStorage();
                if (savedData) {
                    setSchedule(savedData);
                }
            }
            function setSchedule(data) {
                document.querySelector('header p.text-gray-600').textContent = 
                    `Schedule last updated: ${new Date(data.lastSaved).toLocaleString()}`;
                // Restore completion states
                Array.from(document.querySelectorAll('.subject-block')).forEach(item => {
                    if (data.completedItems.includes(item.textContent)) {
                        item.classList.add('line-through');
                    }
                });
                // Restore progress data
                if (data.progressData) {
                    document.getElementById('physics-completed').textContent = data.progressData.physics;
                    document.getElementById('circuits-completed').textContent = data.progressData.circuits;
                    document.getElementById('programming-completed').textContent = data.progressData.programming;
                    document.getElementById('calculus-completed').textContent = data.progressData.calculus;
                    document.getElementById('ielts-completed').textContent = data.progressData.ielts;
                }
                updateProgress();
            }
            // Auto-save every 2 minutes
            setInterval(saveScheduleState, 120000);
            // Update progress when any item is clicked
            document.querySelectorAll('.subject-gym, .subject-physics, .subject-circuits, .subject-programming, .subject-calculus, .subject-ielts').forEach(item => {
                item.addEventListener('click', updateProgress);
            });
        });
    </script>
</body>
</html>

