<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>專案工作流程管理系統 (Firebase 版)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Noto Sans TC', sans-serif; background-color: #f0f4f8; }
        .step-item, .project-card { transition: all 0.3s ease; }
        .project-card:hover, .step-item:hover { transform: translateY(-3px); box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05); }
        .step-complete { background-color: #d1fae5; border-color: #10b981; }
        .step-active { background-color: #e0f2fe; border-color: #3b82f6; }
        .step-pending { background-color: #ffffff; border-color: #d1d5db; }
        .progress-bar { transition: width 0.5s ease; }
        .comment-item { border-left: 3px solid #3b82f6; }
        .loader { border: 4px solid #f3f3f3; border-top: 4px solid #3498db; border-radius: 50%; width: 40px; height: 40px; animation: spin 1.5s linear infinite; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        .skeleton-card { background-color: #ffffff; border-radius: 0.5rem; padding: 1.5rem; box-shadow: 0 1px 3px 0 rgba(0,0,0,0.1), 0 1px 2px 0 rgba(0,0,0,0.06); }
        .skeleton { animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite; background-color: #e5e7eb; border-radius: 0.25rem; }
        @keyframes pulse { 50% { opacity: .5; } }
    </style>
</head>
<body class="bg-gray-100">

    <!-- 全螢幕載入指示器 -->
    <div id="initial-loader" class="fixed inset-0 bg-gray-900 bg-opacity-75 flex flex-col items-center justify-center z-50">
        <div class="loader"></div>
        <p class="text-white mt-4">正在驗證身分...</p>
    </div>

    <!-- 登入模態框 -->
    <div id="login-modal" class="fixed inset-0 bg-gray-900 bg-opacity-50 flex items-center justify-center z-40 hidden">
        <div class="bg-white rounded-lg shadow-xl p-8 max-w-md w-full">
            <h2 class="text-2xl font-bold mb-6 text-center">登入系統</h2>
            <p class="text-gray-600 mb-6 text-center">請使用 Google 帳號登入以使用專案管理系統。</p>
            <div class="flex flex-col items-center">
                <button id="google-login-btn" class="bg-white hover:bg-gray-100 text-gray-700 font-semibold py-2 px-4 border border-gray-300 rounded-lg shadow-sm flex items-center space-x-2">
                    <svg class="w-5 h-5" viewBox="0 0 48 48"><path fill="#EA4335" d="M24 9.5c3.54 0 6.71 1.22 9.21 3.6l6.85-6.85C35.9 2.38 30.47 0 24 0 14.62 0 6.51 5.38 2.56 13.22l7.98 6.19C12.43 13.72 17.74 9.5 24 9.5z"></path><path fill="#4285F4" d="M46.98 24.55c0-1.57-.15-3.09-.38-4.55H24v9.02h12.94c-.58 2.96-2.26 5.48-4.78 7.18l7.73 6c4.51-4.18 7.09-10.36 7.09-17.65z"></path><path fill="#FBBC05" d="M10.53 28.59c-.48-1.45-.76-2.99-.76-4.59s.27-3.14.76-4.59l-7.98-6.19C.92 16.46 0 20.12 0 24c0 3.88.92 7.54 2.56 10.78l7.97-6.19z"></path><path fill="#34A853" d="M24 48c6.48 0 11.93-2.13 15.89-5.81l-7.73-6c-2.15 1.45-4.92 2.3-8.16 2.3-6.26 0-11.57-4.22-13.47-9.91l-7.98 6.19C6.51 42.62 14.62 48 24 48z"></path><path fill="none" d="M0 0h48v48H0z"></path></svg>
                    <span>使用 Google 帳號登入</span>
                </button>
            </div>
        </div>
    </div>

    <!-- 主應用程式 -->
    <div id="app" class="hidden">
        <nav class="bg-indigo-600 text-white shadow-md sticky top-0 z-30">
            <div class="container mx-auto px-4 py-3 flex justify-between items-center">
                <div class="flex items-center"><svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" /></svg><h1 class="text-xl font-bold">專案工作流程管理系統</h1></div>
                <div class="flex items-center"><div class="mr-4 text-right"><span id="user-name" class="font-medium"></span></div><div class="relative"><button id="user-menu-button" class="flex items-center focus:outline-none"><img id="user-avatar" class="h-8 w-8 rounded-full" src="" alt="使用者頭像"></button><div id="user-menu" class="hidden absolute right-0 mt-2 w-48 bg-white rounded-md shadow-lg py-1 z-10"><a href="#" id="logout-button" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">登出</a></div></div></div>
            </div>
        </nav>
        <main class="container mx-auto px-4 py-8">
            <div id="projects-view">
                 <div class="flex justify-between items-center mb-6"><h2 class="text-2xl font-bold text-gray-800">我的專案</h2><button id="new-project-btn" class="bg-indigo-600 hover:bg-indigo-700 text-white py-2 px-4 rounded-md transition duration-300 flex items-center"><svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M10 5a1 1 0 011 1v3h3a1 1 0 110 2h-3v3a1 1 0 11-2 0v-3H6a1 1 0 110-2h3V6a1 1 0 011-1z" clip-rule="evenodd" /></svg>新增專案</button></div>
                 <div id="projects-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"></div>
            </div>
            <div id="project-detail-view" class="hidden"></div>
        </main>
    </div>
    
    <!-- 新增/編輯專案模態框 -->
    <div id="project-modal" class="fixed inset-0 bg-gray-900 bg-opacity-50 flex items-center justify-center z-40 hidden">
        <div class="bg-white rounded-lg shadow-xl p-8 max-w-2xl w-full">
            <div class="flex justify-between items-center mb-6"><h2 id="project-modal-title" class="text-2xl font-bold">新增專案</h2><button class="close-modal-btn text-gray-400 hover:text-gray-600">&times;</button></div>
            <form id="project-form"><input type="hidden" id="project-id"><div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6"><div><label class="block text-gray-700 mb-2" for="project-name-input">專案名稱*</label><input type="text" id="project-name-input" class="w-full px-4 py-2 border rounded-md" required></div><div><label class="block text-gray-700 mb-2" for="client-name-input">客戶名稱*</label><input type="text" id="client-name-input" class="w-full px-4 py-2 border rounded-md" required></div></div><div class="flex justify-end"><button type="button" class="close-modal-btn bg-gray-200 hover:bg-gray-300 text-gray-700 py-2 px-6 rounded-md mr-4">取消</button><button type="submit" class="bg-indigo-600 hover:bg-indigo-700 text-white py-2 px-6 rounded-md">儲存</button></div></form>
        </div>
    </div>

    <!-- 確認刪除模態框 -->
    <div id="delete-confirm-modal" class="fixed inset-0 bg-gray-900 bg-opacity-50 flex items-center justify-center z-50 hidden"><div class="bg-white rounded-lg shadow-xl p-6 max-w-sm w-full"><h3 class="text-lg font-medium text-gray-900">確認刪除</h3><div class="mt-2"><p class="text-sm text-gray-500">您確定要刪除這個專案嗎？此操作無法復原。</p></div><div class="mt-4 flex justify-end space-x-2"><button id="cancel-delete-btn" class="bg-gray-200 py-2 px-4 rounded-md">取消</button><button id="confirm-delete-btn" class="bg-red-600 text-white py-2 px-4 rounded-md">確認刪除</button></div></div></div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, onAuthStateChanged, GoogleAuthProvider, signInWithPopup, signOut } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, collection, query, where, onSnapshot, addDoc, doc, updateDoc, deleteDoc, serverTimestamp, arrayUnion, arrayRemove, getDoc } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        const firebaseConfig = {
          apiKey: "AIzaSyALiBzYT1uRmRKBD7nlDLw0TyD3UVyn3S4",
          authDomain: "istagingworkflow.firebaseapp.com",
          projectId: "istagingworkflow",
          storageBucket: "istagingworkflow.appspot.com",
          messagingSenderId: "619527055783",
          appId: "1:619527055783:web:2636704afb69595e752e82"
        };
        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const db = getFirestore(app);
        
        let currentUser = null;
        let unsubscribeProjects = null;
        let unsubscribeProjectDetail = null;
        const UI = {
            loader: document.getElementById('initial-loader'),
            loginModal: document.getElementById('login-modal'),
            googleLoginBtn: document.getElementById('google-login-btn'),
            app: document.getElementById('app'),
            userName: document.getElementById('user-name'),
            userAvatar: document.getElementById('user-avatar'),
            logoutBtn: document.getElementById('logout-button'),
            userMenuBtn: document.getElementById('user-menu-button'),
            userMenu: document.getElementById('user-menu'),
            projectsView: document.getElementById('projects-view'),
            projectsContainer: document.getElementById('projects-container'),
            projectDetailView: document.getElementById('project-detail-view'),
            newProjectBtn: document.getElementById('new-project-btn'),
            projectModal: document.getElementById('project-modal'),
            projectModalTitle: document.getElementById('project-modal-title'),
            projectForm: document.getElementById('project-form'),
            projectIdInput: document.getElementById('project-id'),
            projectNameInput: document.getElementById('project-name-input'),
            clientNameInput: document.getElementById('client-name-input'),
            closeModalBtns: document.querySelectorAll('.close-modal-btn'),
            deleteConfirmModal: document.getElementById('delete-confirm-modal'),
            cancelDeleteBtn: document.getElementById('cancel-delete-btn'),
            confirmDeleteBtn: document.getElementById('confirm-delete-btn'),
        };

        // --- AUTHENTICATION ---
    let isLoggingIn = false;
function handleGoogleLogin() {
    if (isLoggingIn) return;
    isLoggingIn = true;
    UI.googleLoginBtn.disabled = true;
    UI.googleLoginBtn.textContent = "登入中...";
    const provider = new GoogleAuthProvider();
    signInWithPopup(auth, provider)
        .catch((error) => {
            isLoggingIn = false;
            UI.googleLoginBtn.disabled = false;
            UI.googleLoginBtn.textContent = "使用 Google 帳號登入";
            // ...錯誤處理
            if (error.code === 'auth/popup-blocked') {
                alert('瀏覽器阻擋了彈出式視窗，請允許彈出式視窗後再試一次。');
            } else if (error.code === 'auth/cancelled-popup-request') {
                console.log('使用者關閉了登入視窗。');
            } else if (error.code === 'auth/unauthorized-domain') {
                alert('這個網域尚未被 Firebase 授權，請依照教學文件完成設定。');
            }
        });
}

onAuthStateChanged(auth, user => {
    isLoggingIn = false;
    UI.googleLoginBtn.disabled = false;
    UI.googleLoginBtn.textContent = "使用 Google 帳號登入";
    UI.loader.classList.add('hidden');
    if (user) {
        currentUser = { uid: user.uid, name: user.displayName, email: user.email, avatar: user.photoURL };
        initializeAppUI();
    } else {
        currentUser = null;
        if (unsubscribeProjects) unsubscribeProjects();
        if (unsubscribeProjectDetail) unsubscribeProjectDetail();
        UI.loginModal.classList.remove('hidden');
        UI.app.classList.add('hidden');
    }
});

        // --- UI INITIALIZATION & RENDERING ---
        function initializeAppUI() {
            UI.loginModal.classList.add('hidden');
            UI.app.classList.remove('hidden');
            UI.userName.textContent = currentUser.name;
            UI.userAvatar.src = currentUser.avatar;
            listenForProjects();
        }

        function renderSkeletonProjects() {
            UI.projectsContainer.innerHTML = Array(3).fill('').map(() => `
                <div class="skeleton-card"><div class="space-y-4"><div class="h-6 w-3/4 skeleton"></div><div class="space-y-2"><div class="h-4 w-1/2 skeleton"></div><div class="h-4 w-1/3 skeleton"></div></div><div class="h-3 w-full skeleton"></div></div></div>
            `).join('');
        }

        function renderProjectsList(projects) {
            UI.projectsContainer.innerHTML = '';
            if (projects.length === 0) {
                UI.projectsContainer.innerHTML = `<p class="text-gray-500 col-span-full text-center py-10">您尚未加入任何專案，請點擊右上角新增專案。</p>`;
                return;
            }
            projects.forEach(project => {
                const card = document.createElement('div');
                card.className = 'project-card bg-white rounded-lg shadow-md overflow-hidden cursor-pointer';
                const progress = project.completedSteps ? Math.round((project.completedSteps.length / 6) * 100) : 0;
                card.innerHTML = `<div class="p-6"><h3 class="text-xl font-bold text-gray-800 truncate">${project.name}</h3><p class="text-gray-600 mb-4 mt-1">客戶: ${project.client}</p><div class="flex items-center mt-4"><div class="w-full bg-gray-200 rounded-full h-2 mr-4"><div class="bg-indigo-600 h-2 rounded-full" style="width: ${progress}%"></div></div><span class="text-sm font-medium text-gray-700">${progress}%</span></div></div>`;
                card.addEventListener('click', () => showProjectDetail(project.id));
                UI.projectsContainer.appendChild(card);
            });
        }
        
        function renderProjectDetail(project) {
            UI.projectDetailView.innerHTML = ''; // Clear previous detail
            if (!project) return;
            const progress = project.completedSteps ? Math.round((project.completedSteps.length / 6) * 100) : 0;
            const detailHTML = `
                <div class="flex justify-between items-center mb-6">
                    <button id="back-to-projects" class="text-indigo-600 hover:text-indigo-800">&larr; 返回專案列表</button>
                    <div><button id="edit-project-btn" data-id="${project.id}" class="bg-gray-200 py-2 px-4 rounded-md mr-2">編輯</button><button id="delete-project-btn" data-id="${project.id}" class="bg-red-500 text-white py-2 px-4 rounded-md">刪除</button></div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-md mb-8">
                    <h2 class="text-2xl font-bold text-gray-800">${project.name}</h2>
                    <p class="text-lg text-gray-600 mt-1">客戶: ${project.client}</p>
                    <div class="mt-6"><h3 class="text-sm font-medium text-gray-500">專案進度</h3><div class="mt-2 flex items-center"><div class="w-full bg-gray-200 rounded-full h-4 mr-4"><div class="progress-bar bg-indigo-600 h-4 rounded-full" style="width: ${progress}%"></div></div><span>${progress}%</span></div></div>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    ${[1,2,3,4,5,6].map(stepNum => renderStepCard(stepNum, project)).join('')}
                </div>`;
            UI.projectDetailView.innerHTML = detailHTML;
        }

        function renderStepCard(stepNum, project) {
            const stepTitles = ["Briefing", "AI 智能判斷", "媒體提案", "品牌創意流程", "創意 Story Board", "創意資料夾"];
            const isComplete = project.completedSteps && project.completedSteps.includes(stepNum);
            const cardClass = isComplete ? 'step-complete' : 'step-pending';
            return `
                <div class="step-item ${cardClass} border-2 rounded-lg p-6">
                    <h3 class="text-xl font-bold">${stepNum}. ${stepTitles[stepNum-1]}</h3>
                    <div class="mt-4 flex justify-end">
                        <button class="toggle-step-btn bg-green-500 hover:bg-green-600 text-white py-2 px-4 rounded-md" data-step="${stepNum}" data-id="${project.id}">
                            ${isComplete ? '標記為未完成' : '標記為完成'}
                        </button>
                    </div>
                </div>`;
        }

        // --- FIRESTORE LISTENERS ---
        function listenForProjects() {
            if (unsubscribeProjects) unsubscribeProjects();
            renderSkeletonProjects();
            const projectsRef = collection(db, "projects");
            const q = query(projectsRef, where("members", "array-contains", currentUser.uid));
            unsubscribeProjects = onSnapshot(q, snapshot => {
                const projects = snapshot.docs.map(doc => ({ id: doc.id, ...doc.data() }));
                renderProjectsList(projects);
            }, console.error);
        }
        
        function showProjectDetail(projectId) {
            UI.projectsView.classList.add('hidden');
            UI.projectDetailView.classList.remove('hidden');
            if (unsubscribeProjectDetail) unsubscribeProjectDetail();
            const projectRef = doc(db, "projects", projectId);
            unsubscribeProjectDetail = onSnapshot(projectRef, (doc) => {
                if (doc.exists()) {
                    renderProjectDetail({ id: doc.id, ...doc.data() });
                } else {
                    console.log("Project not found!");
                    backToProjectsList();
                }
            }, console.error);
        }

        // --- EVENT HANDLERS ---
        function backToProjectsList() {
            if(unsubscribeProjectDetail) unsubscribeProjectDetail();
            UI.projectDetailView.classList.add('hidden');
            UI.projectsView.classList.remove('hidden');
        }

        function handleProjectFormSubmit(e) {
            e.preventDefault();
            const id = UI.projectIdInput.value;
            const projectData = {
                name: UI.projectNameInput.value,
                client: UI.clientNameInput.value,
                updatedAt: serverTimestamp()
            };

            if (id) { // Update existing
                updateDoc(doc(db, "projects", id), projectData).then(() => UI.projectModal.classList.add('hidden'));
            } else { // Create new
                projectData.ownerId = currentUser.uid;
                projectData.members = [currentUser.uid];
                projectData.createdAt = serverTimestamp();
                projectData.completedSteps = [];
                addDoc(collection(db, "projects"), projectData).then(() => UI.projectModal.classList.add('hidden'));
            }
        }

        function openProjectModal(project = null) {
            UI.projectForm.reset();
            if (project) {
                UI.projectModalTitle.textContent = "編輯專案";
                UI.projectIdInput.value = project.id;
                UI.projectNameInput.value = project.name;
                UI.clientNameInput.value = project.client;
            } else {
                UI.projectModalTitle.textContent = "新增專案";
                UI.projectIdInput.value = '';
            }
            UI.projectModal.classList.remove('hidden');
        }

        async function toggleStepComplete(projectId, stepNum) {
            const projectRef = doc(db, "projects", projectId);
            const projectSnap = await getDoc(projectRef);
            if (!projectSnap.exists()) return;
            const project = projectSnap.data();
            const isComplete = project.completedSteps && project.completedSteps.includes(stepNum);
            updateDoc(projectRef, {
                completedSteps: isComplete ? arrayRemove(stepNum) : arrayUnion(stepNum)
            });
        }

        function handleDeleteProject(projectId) {
            UI.deleteConfirmModal.classList.remove('hidden');
            UI.confirmDeleteBtn.onclick = () => {
                deleteDoc(doc(db, "projects", projectId)).then(() => {
                    backToProjectsList();
                    UI.deleteConfirmModal.classList.add('hidden');
                });
            };
        }

        // --- EVENT LISTENERS BINDING ---
        UI.googleLoginBtn.addEventListener('click', handleGoogleLogin);
        UI.logoutBtn.addEventListener('click', () => signOut(auth));
        UI.userMenuBtn.addEventListener('click', () => UI.userMenu.classList.toggle('hidden'));
        UI.newProjectBtn.addEventListener('click', () => openProjectModal());
        UI.closeModalBtns.forEach(btn => btn.addEventListener('click', () => {
            UI.projectModal.classList.add('hidden');
            UI.deleteConfirmModal.classList.add('hidden');
        }));
        UI.projectForm.addEventListener('submit', handleProjectFormSubmit);
        UI.cancelDeleteBtn.addEventListener('click', () => UI.deleteConfirmModal.classList.add('hidden'));
        
        document.addEventListener('click', e => {
            if (e.target.id === 'back-to-projects') backToProjectsList();
            if (e.target.id === 'edit-project-btn') {
                const projectId = e.target.dataset.id;
                const projectRef = doc(db, "projects", projectId);
                getDoc(projectRef).then(doc => openProjectModal({id: doc.id, ...doc.data()}));
            }
            if (e.target.id === 'delete-project-btn') handleDeleteProject(e.target.dataset.id);
            if (e.target.classList.contains('toggle-step-btn')) {
                const { id, step } = e.target.dataset;
                toggleStepComplete(id, parseInt(step));
            }
        });
    </script>
</body>
</html>
