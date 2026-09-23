<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. N. Ch. Ravi | Professor at ACE Engineering College</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        w3: {
                            green: '#04AA6D',
                            greenHover: '#059862',
                            dark: '#1D2A35',
                            light: '#FFF4A3',
                            pink: '#FFC0C7',
                            yellow: '#FFF4A3',
                            blue: '#2196F3',
                            teal: '#009688',
                            cyan: '#00BCD4',
                            orange: '#FF9800',
                            purple: '#9C27B0'
                        },
                        ace: {
                            navy: '#0b2545',
                            blue: '#134074'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        mono: ['Consolas', 'Monaco', 'monospace']
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body class="bg-slate-100 text-slate-800 dark:bg-slate-900 dark:text-slate-100 font-sans transition-colors duration-300 min-h-screen flex flex-col">

    <!-- Top W3Schools Style Header/Navbar -->
    <header class="sticky top-0 z-50 bg-w3-dark text-white shadow-md">
        <!-- Top Sub-Bar -->
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                
                <!-- Logo & Title -->
                <div class="flex items-center space-x-3 cursor-pointer" onclick="switchTab('home')">
                    <div class="w-10 h-10 rounded-full bg-w3-green text-white flex items-center justify-center font-extrabold text-xl shadow-md">
                        R
                    </div>
                    <div>
                        <span class="font-extrabold text-lg text-white tracking-wide block leading-none">Dr. N. Ch. Ravi</span>
                        <span class="text-xs text-w3-green font-semibold">Professor • CSE Dept, ACE Engineering College</span>
                    </div>
                </div>

                <!-- Desktop Main Navigation -->
                <nav class="hidden md:flex space-x-1 font-semibold text-sm">
                    <button onclick="switchTab('home')" id="nav-home" class="nav-btn px-4 py-2 rounded-md hover:bg-slate-700 transition">Home</button>
                    
                    <!-- Courses Dropdown -->
                    <div class="relative group">
                        <button onclick="switchTab('courses')" id="nav-courses" class="nav-btn px-4 py-2 rounded-md hover:bg-slate-700 transition flex items-center gap-1">
                            Courses
                            <i class="fa-solid fa-chevron-down text-xs ml-1"></i>
                        </button>
                        <div class="absolute left-0 mt-0 w-72 rounded-lg shadow-xl bg-white text-slate-800 dark:bg-slate-800 dark:text-white border border-slate-200 dark:border-slate-700 opacity-0 group-hover:opacity-100 transition-all duration-200 invisible group-hover:visible z-50">
                            <div class="py-2">
                                <span class="px-4 py-1 text-xs font-bold text-w3-green uppercase tracking-wider block">Semester 1</span>
                                <a href="javascript:void(0)" onclick="filterSemester('sem1'); switchTab('courses');" class="block px-4 py-1.5 text-xs font-medium hover:bg-slate-100 dark:hover:bg-slate-700">CSE 411: Quantum AI & Machine Learning</a>
                                <a href="javascript:void(0)" onclick="filterSemester('sem1'); switchTab('courses');" class="block px-4 py-1.5 text-xs font-medium hover:bg-slate-100 dark:hover:bg-slate-700">CSE 423: Web Security & Blockchain</a>
                                <a href="javascript:void(0)" onclick="filterSemester('sem1'); switchTab('courses');" class="block px-4 py-1.5 text-xs font-medium hover:bg-slate-100 dark:hover:bg-slate-700">CSE 435: AI Full Stack & Agentic Systems</a>
                                <div class="border-t border-slate-200 dark:border-slate-700 my-1"></div>
                                <span class="px-4 py-1 text-xs font-bold text-w3-blue uppercase tracking-wider block">Semester 2</span>
                                <a href="javascript:void(0)" onclick="filterSemester('sem2'); switchTab('courses');" class="block px-4 py-1.5 text-xs font-medium hover:bg-slate-100 dark:hover:bg-slate-700">CSE 452: VLSI Design & LLM Tuning</a>
                                <a href="javascript:void(0)" onclick="filterSemester('sem2'); switchTab('courses');" class="block px-4 py-1.5 text-xs font-medium hover:bg-slate-100 dark:hover:bg-slate-700">CSE 468: Smart Grid & EV Systems</a>
                            </div>
                        </div>
                    </div>

                    <button onclick="switchTab('textbooks')" id="nav-textbooks" class="nav-btn px-4 py-2 rounded-md hover:bg-slate-700 transition">TextBooks</button>
                    <button onclick="switchTab('resources')" id="nav-resources" class="nav-btn px-4 py-2 rounded-md hover:bg-slate-700 transition">Other Resources</button>
                    <button onclick="switchTab('contact')" id="nav-contact" class="nav-btn px-4 py-2 rounded-md hover:bg-slate-700 transition">Contact Us</button>
                </nav>

                <!-- Actions / Controls -->
                <div class="flex items-center space-x-3">
                    <button id="theme-toggle" class="p-2 rounded-full hover:bg-slate-700 text-yellow-300 transition" title="Toggle Theme">
                        <i class="fa-solid fa-moon dark:hidden text-lg"></i>
                        <i class="fa-solid fa-sun hidden dark:block text-lg text-amber-400"></i>
                    </button>

                    <!-- Mobile Menu Trigger -->
                    <button id="mobile-menu-btn" class="md:hidden p-2 rounded-lg hover:bg-slate-700 text-white">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- W3Schools Banner Subject Nav Bar -->
        <div class="bg-slate-800 text-white text-xs border-t border-slate-700 overflow-x-auto py-2 px-4 flex gap-3 whitespace-nowrap justify-center">
            <span class="font-bold text-w3-yellow flex items-center gap-1"><i class="fa-solid fa-bolt"></i> QUICK ACCESS:</span>
            <button onclick="switchTab('courses'); filterSemester('sem1')" class="hover:text-w3-green">Quantum AI</button>
            <span>•</span>
            <button onclick="switchTab('courses'); filterSemester('sem1')" class="hover:text-w3-green">Web Security</button>
            <span>•</span>
            <button onclick="switchTab('courses'); filterSemester('sem1')" class="hover:text-w3-green">Agentic AI</button>
            <span>•</span>
            <button onclick="switchTab('courses'); filterSemester('sem2')" class="hover:text-w3-green">VLSI Chip Design</button>
            <span>•</span>
            <button onclick="switchTab('courses'); filterSemester('sem2')" class="hover:text-w3-green">Smart Grids</button>
        </div>

        <!-- Mobile Drawer -->
        <div id="mobile-menu" class="hidden md:hidden bg-slate-800 px-4 pt-2 pb-4 space-y-1 text-sm border-t border-slate-700">
            <button onclick="switchTab('home'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded hover:bg-slate-700">Home</button>
            <button onclick="switchTab('courses'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded hover:bg-slate-700">Courses</button>
            <button onclick="switchTab('textbooks'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded hover:bg-slate-700">TextBooks</button>
            <button onclick="switchTab('resources'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded hover:bg-slate-700">Other Resources</button>
            <button onclick="switchTab('contact'); toggleMobileMenu();" class="block w-full text-left px-3 py-2 rounded hover:bg-slate-700">Contact Us</button>
        </div>
    </header>

    <!-- Main Content Shell -->
    <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6">

        <!-- TAB 1: HOME SECTION -->
        <section id="tab-home" class="tab-content transition-opacity duration-300">
            <!-- Hero Card: W3 Style Big Feature Banner -->
            <div class="bg-w3-dark text-white rounded-2xl p-6 sm:p-10 mb-8 relative overflow-hidden shadow-xl border-l-8 border-w3-green">
                <div class="flex flex-col md:flex-row gap-8 items-center md:items-start z-10 relative">
                    <div class="relative flex-shrink-0">
                        <img src="https://www.aceec.ac.in/wp-content/uploads/2024/07/Dr-N-Ch-Ravi.jpg" 
                             alt="Dr. N. Ch. Ravi Profile" 
                             class="w-44 h-48 sm:w-52 sm:h-56 rounded-xl object-cover border-4 border-w3-green shadow-lg"
                             onerror="this.onerror=null; this.src='https://placehold.co/400x500/0b2545/ffffff?text=Dr.+N.Ch.+Ravi';">
                        <div class="absolute -bottom-3 -right-3 bg-w3-green text-white text-[10px] font-extrabold px-3 py-1 rounded-full border-2 border-white shadow">
                            <i class="fa-solid fa-graduation-cap"></i> CSE PROFESSOR
                        </div>
                    </div>

                    <div class="space-y-3 flex-1 text-center md:text-left">
                        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full text-xs font-bold bg-w3-green/20 text-w3-green border border-w3-green">
                            ACE Engineering College, Hyderabad
                        </div>
                        <h1 class="text-3xl sm:text-5xl font-black tracking-tight text-white">Dr. N. Ch. Ravi</h1>
                        <p class="text-lg text-w3-yellow font-semibold">Professor • Department of Computer Science & Engineering</p>
                        <p class="text-slate-300 text-sm sm:text-base leading-relaxed">
                            Distinguished Academician & Researcher with 30+ years of cumulative expertise (25 years in university academics & leadership, 5.5 years as Senior Tech Strategist at Infistech Technologies). Specializing in Quantum AI, Agentic Systems, Cloud Security, Blockchain, and Machine Learning models for Vulnerability Mitigation.
                        </p>

                        <div class="flex flex-wrap gap-3 justify-center md:justify-start pt-2">
                            <button onclick="switchTab('courses')" class="px-5 py-2.5 bg-w3-green hover:bg-w3-greenHover text-white font-bold rounded-lg text-sm transition shadow-lg flex items-center gap-2">
                                <i class="fa-solid fa-book-open"></i> Explore Courses
                            </button>
                            <button onclick="switchTab('contact')" class="px-5 py-2.5 bg-slate-700 hover:bg-slate-600 text-white font-bold rounded-lg text-sm transition flex items-center gap-2">
                                <i class="fa-solid fa-envelope"></i> Contact Office
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Experience W3 Color Blocks Grid -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
                <div class="bg-w3-green text-white p-5 rounded-2xl text-center shadow-md">
                    <span class="block text-4xl font-extrabold">30+</span>
                    <span class="text-xs font-bold uppercase tracking-wider">Years Total Exp.</span>
                </div>
                <div class="bg-w3-blue text-white p-5 rounded-2xl text-center shadow-md">
                    <span class="block text-4xl font-extrabold">25</span>
                    <span class="text-xs font-bold uppercase tracking-wider">Years Academic</span>
                </div>
                <div class="bg-w3-orange text-white p-5 rounded-2xl text-center shadow-md">
                    <span class="block text-4xl font-extrabold">5.5</span>
                    <span class="text-xs font-bold uppercase tracking-wider">Years Infistech Industry</span>
                </div>
                <div class="bg-w3-purple text-white p-5 rounded-2xl text-center shadow-md">
                    <span class="block text-4xl font-extrabold">5</span>
                    <span class="text-xs font-bold uppercase tracking-wider">Active Courses</span>
                </div>
            </div>

            <!-- Qualifications & Centers of Excellence -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                
                <!-- Main Info (Qualifications & CoEs) -->
                <div class="lg:col-span-2 space-y-6">
                    
                    <!-- Qualifications Panel -->
                    <div class="bg-white dark:bg-slate-800 rounded-2xl p-6 shadow-sm border border-slate-200 dark:border-slate-700">
                        <h2 class="text-xl font-extrabold text-slate-900 dark:text-white mb-4 flex items-center gap-2 border-b pb-3 border-slate-200 dark:border-slate-700">
                            <i class="fa-solid fa-graduation-cap text-w3-green"></i> Academic Qualifications
                        </h2>
                        <div class="space-y-4">
                            <div class="p-3 bg-slate-50 dark:bg-slate-700/50 rounded-xl border-l-4 border-w3-green">
                                <h3 class="font-bold text-slate-900 dark:text-white text-base">Ph.D. in Computer Science & Engineering</h3>
                                <p class="text-xs font-semibold text-w3-green">JNTU Hyderabad (JNTUH)</p>
                                <p class="text-xs text-slate-600 dark:text-slate-300 mt-1">Dissertation: SQL Injection Attack Detection & Prevention using Deep Learning Architectures (LSTM & BERT).</p>
                            </div>
                            <div class="p-3 bg-slate-50 dark:bg-slate-700/50 rounded-xl border-l-4 border-w3-blue">
                                <h3 class="font-bold text-slate-900 dark:text-white text-base">M.Tech in Computer Science & Engineering</h3>
                                <p class="text-xs font-semibold text-w3-blue">Acharya Nagarjuna University (ANU)</p>
                            </div>
                            <div class="p-3 bg-slate-50 dark:bg-slate-700/50 rounded-xl border-l-4 border-w3-orange">
                                <h3 class="font-bold text-slate-900 dark:text-white text-base">B.Tech in Computer Science & Engineering</h3>
                                <p class="text-xs font-semibold text-w3-orange">JNTU Hyderabad (JNTUH)</p>
                            </div>
                            <div class="p-3 bg-slate-50 dark:bg-slate-700/50 rounded-xl border-l-4 border-w3-purple">
                                <h3 class="font-bold text-slate-900 dark:text-white text-base">M.Sc in Physics (Electronics Specialization)</h3>
                                <p class="text-xs font-semibold text-w3-purple">Kakatiya University</p>
                            </div>
                        </div>
                    </div>

                    <!-- Centers of Excellence Cards -->
                    <div class="bg-white dark:bg-slate-800 rounded-2xl p-6 shadow-sm border border-slate-200 dark:border-slate-700">
                        <h2 class="text-xl font-extrabold text-slate-900 dark:text-white mb-4 flex items-center gap-2 border-b pb-3 border-slate-200 dark:border-slate-700">
                            <i class="fa-solid fa-award text-w3-orange"></i> Centers of Excellence (CoE)
                        </h2>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div class="p-4 rounded-xl bg-w3-light text-slate-900 font-semibold border border-amber-300">
                                <div class="flex items-center gap-2 mb-1">
                                    <i class="fa-brands fa-microsoft text-blue-600 text-xl"></i>
                                    <span class="font-bold">Microsoft CoE</span>
                                </div>
                                <p class="text-xs text-slate-700">Azure Cloud Architecture, GenAI, and Full Stack DevOps.</p>
                            </div>
                            <div class="p-4 rounded-xl bg-w3-pink text-slate-900 font-semibold border border-pink-300">
                                <div class="flex items-center gap-2 mb-1">
                                    <i class="fa-solid fa-server text-purple-700 text-xl"></i>
                                    <span class="font-bold">IBM CoE</span>
                                </div>
                                <p class="text-xs text-slate-700">Quantum Computing with IBM Qiskit and Big Data Analytics.</p>
                            </div>
                            <div class="p-4 rounded-xl bg-sky-100 text-slate-900 font-semibold border border-sky-300">
                                <div class="flex items-center gap-2 mb-1">
                                    <i class="fa-solid fa-network-wired text-sky-600 text-xl"></i>
                                    <span class="font-bold">CISCO Networking</span>
                                </div>
                                <p class="text-xs text-slate-700">Cybersecurity Defense Protocols, Firewalls & Networks.</p>
                            </div>
                            <div class="p-4 rounded-xl bg-emerald-100 text-slate-900 font-semibold border border-emerald-300">
                                <div class="flex items-center gap-2 mb-1">
                                    <i class="fa-solid fa-microchip text-emerald-700 text-xl"></i>
                                    <span class="font-bold">Texas Inst. & AMD</span>
                                </div>
                                <p class="text-xs text-slate-700">VLSI Chip Design, Embedded Grids, and Edge AI.</p>
                            </div>
                        </div>
                    </div>

                </div>

                <!-- Right Sidebar (Research & Metrics) -->
                <div class="space-y-6">
                    <div class="bg-white dark:bg-slate-800 rounded-2xl p-6 shadow-sm border border-slate-200 dark:border-slate-700">
                        <h3 class="text-lg font-bold text-slate-900 dark:text-white mb-4 flex items-center justify-between border-b pb-3 border-slate-200 dark:border-slate-700">
                            <span><i class="fa-solid fa-chart-line text-w3-green mr-2"></i> Research Metrics</span>
                            <span class="bg-w3-green text-white text-[10px] px-2 py-0.5 rounded font-bold">Scopus</span>
                        </h3>
                        <div class="space-y-3 font-semibold text-xs">
                            <div class="flex justify-between p-3 rounded-lg bg-slate-100 dark:bg-slate-700">
                                <span class="text-slate-600 dark:text-slate-300">Total Publications</span>
                                <span class="text-slate-900 dark:text-white font-bold">12 (8 Scopus)</span>
                            </div>
                            <div class="flex justify-between p-3 rounded-lg bg-slate-100 dark:bg-slate-700">
                                <span class="text-slate-600 dark:text-slate-300">Citations</span>
                                <span class="text-slate-900 dark:text-white font-bold">294+</span>
                            </div>
                            <div class="flex justify-between p-3 rounded-lg bg-slate-100 dark:bg-slate-700">
                                <span class="text-slate-600 dark:text-slate-300">h-index</span>
                                <span class="text-slate-900 dark:text-white font-bold">4</span>
                            </div>
                            <div class="flex justify-between p-3 rounded-lg bg-slate-100 dark:bg-slate-700">
                                <span class="text-slate-600 dark:text-slate-300">Patents Published</span>
                                <span class="text-slate-900 dark:text-white font-bold">4 Published</span>
                            </div>
                        </div>
                    </div>

                    <!-- Institution Card -->
                    <div class="bg-w3-dark text-white p-6 rounded-2xl shadow-md border-t-4 border-w3-green">
                        <h3 class="font-bold text-base mb-2 text-w3-green">ACE Engineering College</h3>
                        <p class="text-xs text-slate-300 leading-relaxed mb-4">
                            Ankushapur, Ghatkesar Mandal, Medchal District, Telangana - 501301. Autonomous Institution, Approved by AICTE, Affiliated to JNTUH.
                        </p>
                        <div class="space-y-2 text-xs">
                            <div class="flex items-center gap-2">
                                <i class="fa-solid fa-location-dot text-w3-green"></i>
                                <span>Ghatkesar, Medchal Dist, Telangana</span>
                            </div>
                            <div class="flex items-center gap-2">
                                <i class="fa-solid fa-globe text-w3-green"></i>
                                <a href="https://www.aceec.ac.in" target="_blank" class="underline hover:text-w3-green">www.aceec.ac.in</a>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <!-- TAB 2: COURSES SECTION -->
        <section id="tab-courses" class="tab-content hidden transition-opacity duration-300">
            <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-6 bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm">
                <div>
                    <h1 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white">Academic Courses</h1>
                    <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Explore courses taught across Semester 1 & Semester 2 with full curriculum details.</p>
                </div>
                <div class="flex items-center space-x-2 bg-slate-100 dark:bg-slate-700 p-1.5 rounded-xl">
                    <button onclick="filterSemester('all')" id="filter-all" class="semester-filter-btn px-4 py-1.5 rounded-lg text-xs font-bold transition bg-w3-green text-white shadow">All Semesters</button>
                    <button onclick="filterSemester('sem1')" id="filter-sem1" class="semester-filter-btn px-4 py-1.5 rounded-lg text-xs font-bold text-slate-600 dark:text-slate-300 hover:text-slate-900 transition">Semester I (3 Courses)</button>
                    <button onclick="filterSemester('sem2')" id="filter-sem2" class="semester-filter-btn px-4 py-1.5 rounded-lg text-xs font-bold text-slate-600 dark:text-slate-300 hover:text-slate-900 transition">Semester II (2 Courses)</button>
                </div>
            </div>

            <!-- Courses Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6" id="courses-grid">

                <!-- COURSE 1 -->
                <div class="course-card bg-white dark:bg-slate-800 rounded-2xl p-6 border-t-8 border-w3-green shadow-sm flex flex-col justify-between" data-semester="sem1">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full text-xs font-extrabold bg-w3-green/20 text-w3-green border border-w3-green">CSE 411</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400"><i class="fa-regular fa-calendar mr-1"></i> Semester I</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">Quantum AI & Machine Learning</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 mb-4 leading-relaxed">
                            Quantum circuits, IBM Qiskit simulation, variational quantum eigensolvers, and hybrid quantum-classical neural network architectures.
                        </p>

                        <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 dark:text-slate-300 mb-4 bg-slate-50 dark:bg-slate-700/50 p-3 rounded-xl border border-slate-200 dark:border-slate-700">
                            <div><strong class="text-slate-900 dark:text-white">Schedule:</strong> Mon/Wed 10:00 AM</div>
                            <div><strong class="text-slate-900 dark:text-white">Room:</strong> IBM CoE Lab</div>
                            <div><strong class="text-slate-900 dark:text-white">Credits:</strong> 4.0 Units</div>
                            <div><strong class="text-slate-900 dark:text-white">Office Hours:</strong> Tue 2:00 PM</div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-700 flex items-center justify-between gap-2">
                        <button onclick="openSyllabusModal('course1')" class="text-xs font-bold text-w3-green hover:underline flex items-center gap-1">
                            <i class="fa-solid fa-book-open"></i> Syllabus & Modules
                        </button>
                        <button onclick="triggerDownload('Quantum_AI_Slides.pdf')" class="px-3 py-1.5 text-xs bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-md font-bold transition">
                            <i class="fa-solid fa-download mr-1"></i> Slides
                        </button>
                    </div>
                </div>

                <!-- COURSE 2 -->
                <div class="course-card bg-white dark:bg-slate-800 rounded-2xl p-6 border-t-8 border-w3-blue shadow-sm flex flex-col justify-between" data-semester="sem1">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full text-xs font-extrabold bg-w3-blue/20 text-w3-blue border border-w3-blue">CSE 423</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400"><i class="fa-regular fa-calendar mr-1"></i> Semester I</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">Web Security & Blockchain</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 mb-4 leading-relaxed">
                            SQL injection mitigation with LSTM/BERT models, OWASP Top 10 web security controls, smart contract audits, and Ethereum consensus.
                        </p>

                        <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 dark:text-slate-300 mb-4 bg-slate-50 dark:bg-slate-700/50 p-3 rounded-xl border border-slate-200 dark:border-slate-700">
                            <div><strong class="text-slate-900 dark:text-white">Schedule:</strong> Tue/Thu 09:00 AM</div>
                            <div><strong class="text-slate-900 dark:text-white">Room:</strong> CISCO Security Lab</div>
                            <div><strong class="text-slate-900 dark:text-white">Credits:</strong> 4.0 Units</div>
                            <div><strong class="text-slate-900 dark:text-white">Office Hours:</strong> Wed 3:00 PM</div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-700 flex items-center justify-between gap-2">
                        <button onclick="openSyllabusModal('course2')" class="text-xs font-bold text-w3-blue hover:underline flex items-center gap-1">
                            <i class="fa-solid fa-book-open"></i> Syllabus & Modules
                        </button>
                        <button onclick="triggerDownload('WebSecurity_Guide.pdf')" class="px-3 py-1.5 text-xs bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-md font-bold transition">
                            <i class="fa-solid fa-download mr-1"></i> Guide
                        </button>
                    </div>
                </div>

                <!-- COURSE 3 -->
                <div class="course-card bg-white dark:bg-slate-800 rounded-2xl p-6 border-t-8 border-w3-orange shadow-sm flex flex-col justify-between" data-semester="sem1">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full text-xs font-extrabold bg-w3-orange/20 text-w3-orange border border-w3-orange">CSE 435</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400"><i class="fa-regular fa-calendar mr-1"></i> Semester I</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">AI Full Stack & Agentic Systems</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 mb-4 leading-relaxed">
                            MERN/MEAN stack architecture integrated with LangChain multi-agent orchestration, vector embeddings, and autonomous agent loops.
                        </p>

                        <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 dark:text-slate-300 mb-4 bg-slate-50 dark:bg-slate-700/50 p-3 rounded-xl border border-slate-200 dark:border-slate-700">
                            <div><strong class="text-slate-900 dark:text-white">Schedule:</strong> Fri 01:00 PM</div>
                            <div><strong class="text-slate-900 dark:text-white">Room:</strong> Microsoft CoE Lab</div>
                            <div><strong class="text-slate-900 dark:text-white">Credits:</strong> 3.0 Units</div>
                            <div><strong class="text-slate-900 dark:text-white">Office Hours:</strong> Thu 2:00 PM</div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-700 flex items-center justify-between gap-2">
                        <button onclick="openSyllabusModal('course3')" class="text-xs font-bold text-w3-orange hover:underline flex items-center gap-1">
                            <i class="fa-solid fa-book-open"></i> Syllabus & Modules
                        </button>
                        <button onclick="triggerDownload('Agentic_FullStack.pdf')" class="px-3 py-1.5 text-xs bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-md font-bold transition">
                            <i class="fa-solid fa-download mr-1"></i> Slides
                        </button>
                    </div>
                </div>

                <!-- COURSE 4 -->
                <div class="course-card bg-white dark:bg-slate-800 rounded-2xl p-6 border-t-8 border-w3-purple shadow-sm flex flex-col justify-between" data-semester="sem2">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full text-xs font-extrabold bg-w3-purple/20 text-w3-purple border border-w3-purple">CSE 452</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400"><i class="fa-regular fa-calendar mr-1"></i> Semester II</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">VLSI Design & LLM Tuning</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 mb-4 leading-relaxed">
                            CMOS digital logic, hardware description languages (Verilog), LLM fine-tuning for EDA layout synthesis, and Texas Instruments chip labs.
                        </p>

                        <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 dark:text-slate-300 mb-4 bg-slate-50 dark:bg-slate-700/50 p-3 rounded-xl border border-slate-200 dark:border-slate-700">
                            <div><strong class="text-slate-900 dark:text-white">Schedule:</strong> Tue/Thu 02:00 PM</div>
                            <div><strong class="text-slate-900 dark:text-white">Room:</strong> TI-AMD CoE Lab</div>
                            <div><strong class="text-slate-900 dark:text-white">Credits:</strong> 4.0 Units</div>
                            <div><strong class="text-slate-900 dark:text-white">Office Hours:</strong> Mon 11:00 AM</div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-700 flex items-center justify-between gap-2">
                        <button onclick="openSyllabusModal('course4')" class="text-xs font-bold text-w3-purple hover:underline flex items-center gap-1">
                            <i class="fa-solid fa-book-open"></i> Syllabus & Modules
                        </button>
                        <button onclick="triggerDownload('VLSI_Design_Notes.pdf')" class="px-3 py-1.5 text-xs bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-md font-bold transition">
                            <i class="fa-solid fa-download mr-1"></i> Notes
                        </button>
                    </div>
                </div>

                <!-- COURSE 5 -->
                <div class="course-card bg-white dark:bg-slate-800 rounded-2xl p-6 border-t-8 border-w3-teal shadow-sm flex flex-col justify-between" data-semester="sem2">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full text-xs font-extrabold bg-w3-teal/20 text-w3-teal border border-w3-teal">CSE 468</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400"><i class="fa-regular fa-calendar mr-1"></i> Semester II</span>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">Smart Grid, EV & Embedded Systems</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 mb-4 leading-relaxed">
                            IoT telemetry in smart energy grids, Electric Vehicle battery management systems, embedded RTOS controllers, and edge AI security.
                        </p>

                        <div class="grid grid-cols-2 gap-2 text-xs text-slate-600 dark:text-slate-300 mb-4 bg-slate-50 dark:bg-slate-700/50 p-3 rounded-xl border border-slate-200 dark:border-slate-700">
                            <div><strong class="text-slate-900 dark:text-white">Schedule:</strong> Wed/Fri 11:00 AM</div>
                            <div><strong class="text-slate-900 dark:text-white">Room:</strong> Embedded Lab</div>
                            <div><strong class="text-slate-900 dark:text-white">Credits:</strong> 3.0 Units</div>
                            <div><strong class="text-slate-900 dark:text-white">Office Hours:</strong> Wed 2:00 PM</div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-700 flex items-center justify-between gap-2">
                        <button onclick="openSyllabusModal('course5')" class="text-xs font-bold text-w3-teal hover:underline flex items-center gap-1">
                            <i class="fa-solid fa-book-open"></i> Syllabus & Modules
                        </button>
                        <button onclick="triggerDownload('SmartGrid_EV_Handbook.pdf')" class="px-3 py-1.5 text-xs bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-md font-bold transition">
                            <i class="fa-solid fa-download mr-1"></i> Handbook
                        </button>
                    </div>
                </div>

            </div>
        </section>

        <!-- TAB 3: TEXTBOOKS SECTION -->
        <section id="tab-textbooks" class="tab-content hidden transition-opacity duration-300">
            <div class="mb-6 bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm">
                <h1 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white">Academic TextBooks</h1>
                <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Recommended academic reference literature for Dr. N. Ch. Ravi's courses.</p>
            </div>

            <div class="space-y-6">
                <!-- Book 1 -->
                <div class="bg-white dark:bg-slate-800 rounded-2xl p-6 border-l-8 border-w3-green shadow-sm flex flex-col md:flex-row gap-6 items-start">
                    <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&q=80&w=300" alt="Quantum Book" class="w-28 h-36 rounded-lg object-cover shadow border border-slate-200 dark:border-slate-700 flex-shrink-0">
                    <div class="flex-1 space-y-2">
                        <span class="px-2.5 py-0.5 rounded-full text-xs font-extrabold bg-w3-green text-white">Required Reading</span>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white">Quantum Computing for Computer Scientists</h3>
                        <p class="text-xs font-semibold text-slate-600 dark:text-slate-300">By Noson S. Yanofsky & Mirco A. Mannucci • Cambridge University Press</p>
                        <p class="text-xs text-slate-500 dark:text-slate-400 leading-relaxed pt-1">
                            Comprehensive mathematical foundation covering linear algebra, quantum gates, entanglement, and quantum algorithm design for computer science professionals.
                        </p>
                        <div class="pt-2">
                            <button onclick="copyCitation('Yanofsky, N. S., & Mannucci, M. A. Quantum Computing for Computer Scientists. Cambridge Univ Press.')" class="px-3 py-1.5 bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-lg text-xs font-bold transition">
                                <i class="fa-regular fa-copy mr-1"></i> Copy Citation
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Book 2 -->
                <div class="bg-white dark:bg-slate-800 rounded-2xl p-6 border-l-8 border-w3-blue shadow-sm flex flex-col md:flex-row gap-6 items-start">
                    <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&q=80&w=300" alt="Security Book" class="w-28 h-36 rounded-lg object-cover shadow border border-slate-200 dark:border-slate-700 flex-shrink-0">
                    <div class="flex-1 space-y-2">
                        <span class="px-2.5 py-0.5 rounded-full text-xs font-extrabold bg-w3-blue text-white">Required Reading</span>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white">The Web Application Hacker's Handbook</h3>
                        <p class="text-xs font-semibold text-slate-600 dark:text-slate-300">By Dafydd Stuttard & Marcus Pinto • Wiley</p>
                        <p class="text-xs text-slate-500 dark:text-slate-400 leading-relaxed pt-1">
                            In-depth analysis of web application vulnerabilities, SQL injection mitigation techniques, session mechanics, and defensive engineering practices.
                        </p>
                        <div class="pt-2">
                            <button onclick="copyCitation('Stuttard, D., & Pinto, M. The Web Application Hacker\'s Handbook. Wiley.')" class="px-3 py-1.5 bg-slate-100 dark:bg-slate-700 hover:bg-slate-200 text-slate-800 dark:text-slate-200 rounded-lg text-xs font-bold transition">
                                <i class="fa-regular fa-copy mr-1"></i> Copy Citation
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- TAB 4: OTHER RESOURCES SECTION (FIXED & ADDED) -->
        <section id="tab-resources" class="tab-content hidden transition-opacity duration-300">
            <div class="mb-6 bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col sm:flex-row items-center justify-between gap-4">
                <div>
                    <h1 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white">Academic Resources & Research Papers</h1>
                    <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Download lecture notes, lab manuals, and research papers authored by Dr. N. Ch. Ravi.</p>
                </div>
                <div class="w-full sm:w-64 relative">
                    <input type="text" id="resource-search" onkeyup="searchResources()" placeholder="Search resources..." class="w-full pl-9 pr-3 py-2 bg-slate-100 dark:bg-slate-700 border border-slate-300 dark:border-slate-600 rounded-xl text-xs font-medium focus:ring-2 focus:ring-w3-green focus:outline-none">
                    <i class="fa-solid fa-magnifying-glass absolute left-3 top-2.5 text-slate-400 text-xs"></i>
                </div>
            </div>

            <!-- Resources Cards Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6" id="resources-grid">
                
                <div class="resource-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex justify-between items-center mb-3">
                            <span class="px-2.5 py-0.5 rounded text-[10px] font-extrabold bg-w3-green text-white">Scopus Paper</span>
                            <span class="text-[10px] text-slate-400">PDF • 2.4 MB</span>
                        </div>
                        <h3 class="font-bold text-slate-900 dark:text-white text-sm mb-2">SQL Injection Detection using LSTM & BERT</h3>
                        <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">Published Scopus research paper detailing neural network detection models for web vulnerabilities.</p>
                    </div>
                    <button onclick="triggerDownload('SQLi_LSTM_BERT_Paper.pdf')" class="w-full py-2 bg-slate-100 dark:bg-slate-700 hover:bg-w3-green hover:text-white text-slate-800 dark:text-slate-200 rounded-xl font-bold text-xs transition flex items-center justify-center gap-2">
                        <i class="fa-solid fa-download"></i> Download Paper
                    </button>
                </div>

                <div class="resource-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex justify-between items-center mb-3">
                            <span class="px-2.5 py-0.5 rounded text-[10px] font-extrabold bg-w3-blue text-white">Lab Manual</span>
                            <span class="text-[10px] text-slate-400">PDF • 5.1 MB</span>
                        </div>
                        <h3 class="font-bold text-slate-900 dark:text-white text-sm mb-2">IBM Qiskit Quantum Computing Lab Manual</h3>
                        <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">Hands-on lab experiments for building quantum circuits, gate operations, and VQE algorithms.</p>
                    </div>
                    <button onclick="triggerDownload('IBM_Qiskit_Lab_Manual.pdf')" class="w-full py-2 bg-slate-100 dark:bg-slate-700 hover:bg-w3-blue hover:text-white text-slate-800 dark:text-slate-200 rounded-xl font-bold text-xs transition flex items-center justify-center gap-2">
                        <i class="fa-solid fa-download"></i> Download Manual
                    </button>
                </div>

                <div class="resource-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex justify-between items-center mb-3">
                            <span class="px-2.5 py-0.5 rounded text-[10px] font-extrabold bg-w3-orange text-white">Lecture Notes</span>
                            <span class="text-[10px] text-slate-400">PDF • 3.8 MB</span>
                        </div>
                        <h3 class="font-bold text-slate-900 dark:text-white text-sm mb-2">LangChain & Agentic Systems Architecture</h3>
                        <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">Complete lecture slides covering vector databases, prompt engineering, and multi-agent loops.</p>
                    </div>
                    <button onclick="triggerDownload('LangChain_Agentic_Notes.pdf')" class="w-full py-2 bg-slate-100 dark:bg-slate-700 hover:bg-w3-orange hover:text-white text-slate-800 dark:text-slate-200 rounded-xl font-bold text-xs transition flex items-center justify-center gap-2">
                        <i class="fa-solid fa-download"></i> Download Notes
                    </button>
                </div>

            </div>
        </section>

        <!-- TAB 5: CONTACT SECTION -->
        <section id="tab-contact" class="tab-content hidden transition-opacity duration-300">
            <div class="mb-6 bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm">
                <h1 class="text-2xl sm:text-3xl font-extrabold text-slate-900 dark:text-white">Contact & Consultation</h1>
                <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Get in touch with Dr. N. Ch. Ravi at ACE Engineering College.</p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Info Panel -->
                <div class="space-y-4">
                    <div class="bg-w3-dark text-white p-6 rounded-2xl border-l-8 border-w3-green shadow-md">
                        <h3 class="text-base font-bold text-w3-green mb-3">Official Office Address</h3>
                        <p class="text-xs text-slate-300 leading-relaxed mb-4">
                            Department of Computer Science & Engineering,<br>
                            ACE Engineering College, Ankushapur,<br>
                            Ghatkesar Mandal, Medchal District,<br>
                            Telangana - 501301, India.
                        </p>
                        <div class="space-y-2 text-xs border-t border-slate-700 pt-3">
                            <div><strong class="text-w3-green">Phone:</strong> +91 8712225044</div>
                            <div><strong class="text-w3-green">Email:</strong> admissions@aceec.ac.in</div>
                        </div>
                    </div>
                </div>

                <!-- Interactive Form -->
                <div class="lg:col-span-2 bg-white dark:bg-slate-800 rounded-2xl p-6 sm:p-8 border border-slate-200 dark:border-slate-700 shadow-sm">
                    <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">Send Academic Inquiry</h3>
                    <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4 mt-4">
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">Full Name</label>
                                <input type="text" required placeholder="John Doe" class="w-full px-3 py-2 bg-slate-50 dark:bg-slate-700 border border-slate-300 dark:border-slate-600 rounded-xl text-xs focus:ring-2 focus:ring-w3-green focus:outline-none">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">Email Address</label>
                                <input type="email" required placeholder="john@example.com" class="w-full px-3 py-2 bg-slate-50 dark:bg-slate-700 border border-slate-300 dark:border-slate-600 rounded-xl text-xs focus:ring-2 focus:ring-w3-green focus:outline-none">
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">Subject</label>
                            <input type="text" required placeholder="Academic Consultation / Course Inquiry" class="w-full px-3 py-2 bg-slate-50 dark:bg-slate-700 border border-slate-300 dark:border-slate-600 rounded-xl text-xs focus:ring-2 focus:ring-w3-green focus:outline-none">
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">Message</label>
                            <textarea rows="4" required placeholder="Type your message here..." class="w-full px-3 py-2 bg-slate-50 dark:bg-slate-700 border border-slate-300 dark:border-slate-600 rounded-xl text-xs focus:ring-2 focus:ring-w3-green focus:outline-none"></textarea>
                        </div>

                        <button type="submit" class="px-6 py-2.5 bg-w3-green hover:bg-w3-greenHover text-white font-bold text-xs rounded-xl shadow transition flex items-center gap-2">
                            <i class="fa-solid fa-paper-plane"></i> Send Message
                        </button>
                    </form>
                </div>
            </div>
        </section>

    </main>

    <!-- SYLLABUS MODAL -->
    <div id="syllabus-modal" class="fixed inset-0 bg-black/60 z-50 hidden items-center justify-center p-4 backdrop-blur-sm">
        <div class="bg-white dark:bg-slate-800 w-full max-w-xl rounded-2xl shadow-2xl border border-slate-200 dark:border-slate-700 overflow-hidden flex flex-col">
            <div class="p-5 border-b border-slate-200 dark:border-slate-700 flex justify-between items-center bg-w3-dark text-white">
                <div>
                    <span id="modal-course-code" class="text-xs font-extrabold px-2 py-0.5 rounded bg-w3-green text-white">CSE 411</span>
                    <h3 id="modal-course-title" class="text-lg font-bold mt-1">Course Syllabus</h3>
                </div>
                <button onclick="closeSyllabusModal()" class="text-slate-400 hover:text-white text-xl font-bold">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div id="modal-body-content" class="p-6 overflow-y-auto max-h-[60vh] space-y-4 text-xs text-slate-600 dark:text-slate-300">
                <!-- Syllabus Populated Dynamically -->
            </div>

            <div class="p-4 border-t border-slate-200 dark:border-slate-700 flex justify-end bg-slate-50 dark:bg-slate-900">
                <button onclick="closeSyllabusModal()" class="px-4 py-2 bg-slate-200 dark:bg-slate-700 hover:bg-slate-300 text-slate-800 dark:text-slate-200 font-bold rounded-lg text-xs transition">
                    Close
                </button>
            </div>
        </div>
    </div>

    <!-- TOAST NOTIFICATION -->
    <div id="toast" class="fixed bottom-5 right-5 bg-w3-dark text-white px-5 py-3 rounded-xl shadow-2xl border-l-4 border-w3-green text-xs font-bold translate-y-20 opacity-0 transition-all duration-300 z-50 flex items-center gap-3">
        <i class="fa-solid fa-circle-check text-w3-green text-lg"></i>
        <span id="toast-message">Notification message</span>
    </div>

    <!-- FOOTER -->
    <footer class="mt-auto border-t border-slate-200 dark:border-slate-800 bg-w3-dark text-white py-6">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-400">
            <div>
                &copy; 2026 Dr. N. Ch. Ravi • ACE Engineering College, Telangana.
            </div>
            <div class="flex space-x-4">
                <button onclick="switchTab('home')" class="hover:text-w3-green">Home</button>
                <button onclick="switchTab('courses')" class="hover:text-w3-green">Courses</button>
                <button onclick="switchTab('textbooks')" class="hover:text-w3-green">TextBooks</button>
                <button onclick="switchTab('resources')" class="hover:text-w3-green">Resources</button>
                <button onclick="switchTab('contact')" class="hover:text-w3-green">Contact</button>
            </div>
        </div>
    </footer>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        const syllabiData = {
            'course1': {
                code: 'CSE 411',
                title: 'Quantum AI & Machine Learning',
                summary: 'Explores quantum circuit mechanics, IBM Qiskit integration, variational eigensolvers, and hybrid quantum neural models.',
                modules: [
                    'Module 1: Qubits, Superposition & Gate Logic',
                    'Module 2: IBM Qiskit Framework & Circuit Building',
                    'Module 3: Variational Quantum Eigensolvers (VQE)',
                    'Module 4: Quantum Support Vector Machines (QSVM)',
                    'Module 5: Hybrid Quantum-Classical Architectures'
                ]
            },
            'course2': {
                code: 'CSE 423',
                title: 'Web Security & Blockchain',
                summary: 'Mitigating SQL Injections using LSTM & BERT models, OWASP Top 10 defenses, smart contracts, and Ethereum security.',
                modules: [
                    'Module 1: SQLi Detection via LSTM & BERT',
                    'Module 2: OWASP Top 10 Mitigation Controls',
                    'Module 3: Cryptographic Ledger Foundations',
                    'Module 4: Solidity Smart Contract Audits',
                    'Module 5: CISCO Cyber Security Controls'
                ]
            },
            'course3': {
                code: 'CSE 435',
                title: 'AI Full Stack & Agentic Systems',
                summary: 'Full stack development with MERN stack, vector databases, LangChain orchestration, and autonomous agent loops.',
                modules: [
                    'Module 1: MERN Stack Microservices Architecture',
                    'Module 2: Vector DBs (Chroma/Pinecone) & Embeddings',
                    'Module 3: LangChain Multi-Agent Frameworks',
                    'Module 4: Autonomous ReAct Agent Loops',
                    'Module 5: Microsoft Azure Cloud Deployment'
                ]
            },
            'course4': {
                code: 'CSE 452',
                title: 'VLSI Design & LLM Tuning',
                summary: 'CMOS digital logic, Verilog hardware synthesis, and LLM fine-tuning for physical chip layout generation.',
                modules: [
                    'Module 1: CMOS Digital Logic & Semiconductor Fabrication',
                    'Module 2: Hardware Description Languages (Verilog)',
                    'Module 3: LLM Fine-Tuning for Verilog Code Generation',
                    'Module 4: Automated EDA Layout Optimization',
                    'Module 5: Texas Instruments Hardware Acceleration'
                ]
            },
            'course5': {
                code: 'CSE 468',
                title: 'Smart Grid, EV & Embedded Systems',
                summary: 'IoT telemetry in smart energy grids, EV battery management systems, embedded RTOS, and edge AI security.',
                modules: [
                    'Module 1: Microcontrollers & Embedded RTOS Architecture',
                    'Module 2: Smart Grid Telemetry & Power Networks',
                    'Module 3: EV Battery Management Systems (BMS)',
                    'Module 4: Edge AI Anomaly Detection',
                    'Module 5: Cyber-Physical Infrastructure Security'
                ]
            }
        };

        function switchTab(tabId) {
            const tabs = document.querySelectorAll('.tab-content');
            tabs.forEach(tab => tab.classList.add('hidden'));

            const target = document.getElementById(`tab-${tabId}`);
            if(target) target.classList.remove('hidden');

            const navBtns = document.querySelectorAll('.nav-btn');
            navBtns.forEach(btn => btn.classList.remove('bg-slate-700', 'text-w3-green'));

            const activeNav = document.getElementById(`nav-${tabId}`);
            if(activeNav) activeNav.classList.add('bg-slate-700', 'text-w3-green');

            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function filterSemester(semester) {
            const courseCards = document.querySelectorAll('.course-card');
            courseCards.forEach(card => {
                if(semester === 'all') {
                    card.classList.remove('hidden');
                } else {
                    if(card.getAttribute('data-semester') === semester) {
                        card.classList.remove('hidden');
                    } else {
                        card.classList.add('hidden');
                    }
                }
            });

            const btns = document.querySelectorAll('.semester-filter-btn');
            btns.forEach(btn => {
                btn.classList.remove('bg-w3-green', 'text-white', 'shadow');
                btn.classList.add('text-slate-600', 'dark:text-slate-300');
            });

            const activeBtn = document.getElementById(`filter-${semester}`);
            if(activeBtn) {
                activeBtn.classList.add('bg-w3-green', 'text-white', 'shadow');
            }
        }

        function openSyllabusModal(courseKey) {
            const data = syllabiData[courseKey];
            if(!data) return;

            document.getElementById('modal-course-code').innerText = data.code;
            document.getElementById('modal-course-title').innerText = data.title;

            let modulesHTML = data.modules.map(mod => 
                `<li class="p-2.5 bg-slate-100 dark:bg-slate-700/50 rounded-lg font-bold flex items-center gap-2 text-slate-800 dark:text-slate-200">
                    <i class="fa-solid fa-circle-check text-w3-green"></i> ${mod}
                 </li>`
            ).join('');

            document.getElementById('modal-body-content').innerHTML = `
                <p class="text-sm font-medium leading-relaxed">${data.summary}</p>
                <div class="mt-4">
                    <h4 class="font-extrabold text-slate-900 dark:text-white uppercase tracking-wider mb-2">Modules Overview</h4>
                    <ul class="space-y-2">${modulesHTML}</ul>
                </div>
            `;

            const modal = document.getElementById('syllabus-modal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeSyllabusModal() {
            const modal = document.getElementById('syllabus-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function searchResources() {
            const query = document.getElementById('resource-search').value.toLowerCase();
            const cards = document.querySelectorAll('.resource-card');

            cards.forEach(card => {
                const text = card.innerText.toLowerCase();
                card.classList.toggle('hidden', !text.includes(query));
            });
        }

        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toast-message').innerText = msg;

            toast.classList.remove('translate-y-20', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');

            setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }

        function triggerDownload(fileName) {
            showToast(`Downloading: ${fileName}`);
        }

        function copyCitation(text) {
            navigator.clipboard.writeText(text);
            showToast("Citation copied to clipboard!");
        }

        function handleFormSubmit(e) {
            e.preventDefault();
            showToast("Thank you! Your inquiry has been sent.");
            document.getElementById('contact-form').reset();
        }

        function toggleMobileMenu() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        }

        document.getElementById('mobile-menu-btn').addEventListener('click', toggleMobileMenu);

        document.getElementById('theme-toggle').addEventListener('click', () => {
            document.documentElement.classList.toggle('dark');
        });

        window.onload = function() {
            switchTab('home');
        };
    </script>
</body>
</html>
