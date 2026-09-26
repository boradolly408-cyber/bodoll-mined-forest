[마음돌봄.html](https://github.com/user-attachments/files/32679882/default.html)
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>마음 숲 정원 - 나를 돌보는 시간</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Gaegu (손글씨체), Noto Sans KR -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Gaegu:wght@400;700&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Gaegu', 'Noto Sans KR', sans-serif;
      letter-spacing: -0.01em;
    }
    .font-sans-kr {
      font-family: 'Noto Sans KR', sans-serif;
    }
    /* 반짝이는 별 애니메이션 */
    @keyframes twinkle {
      0%, 100% { opacity: 0.3; transform: scale(0.9); }
      50% { opacity: 1; transform: scale(1.15); }
    }
    .animate-twinkle {
      animation: twinkle 3s ease-in-out infinite;
    }
    .animate-twinkle-delay {
      animation: twinkle 3.5s ease-in-out 1.2s infinite;
    }
    /* 호흡 원 애니메이션 */
    .breathe-expand {
      transform: scale(1.35);
      transition: transform 4s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .breathe-contract {
      transform: scale(0.85);
      transition: transform 6s cubic-bezier(0.4, 0, 0.2, 1);
    }
    /* 커스텀 스크롤바 */
    ::-webkit-scrollbar {
      width: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #0f1c29;
    }
    ::-webkit-scrollbar-thumb {
      background: #234734;
      border-radius: 9999px;
    }
  </style>
</head>
<body class="bg-[#0c1520] text-[#e8f1ec] min-h-screen flex flex-col items-center select-none relative overflow-x-hidden">

  <!-- 배경 감성 장식 요소 (노란 별, 은은한 빛) -->
  <div class="fixed inset-0 pointer-events-none z-0 overflow-hidden">
    <div class="absolute top-10 left-[10%] text-yellow-300 text-lg animate-twinkle">⭐</div>
    <div class="absolute top-24 right-[15%] text-yellow-200 text-sm animate-twinkle-delay">✨</div>
    <div class="absolute top-48 left-[25%] text-yellow-400 text-xs animate-twinkle">⭐</div>
    <div class="absolute bottom-20 left-[8%] text-yellow-300 text-sm animate-twinkle-delay">⭐</div>
    <div class="absolute bottom-32 right-[12%] text-yellow-300 text-base animate-twinkle">✨</div>
    <div class="absolute top-1/2 right-[5%] text-yellow-200 text-xs animate-twinkle-delay">⭐</div>
  </div>

  <!-- 상단 네비게이션 헤더 -->
  <header class="w-full max-w-2xl px-6 py-5 flex items-center justify-between z-10 border-b border-emerald-900/40 bg-[#0c1520]/80 backdrop-blur-md sticky top-0">
    <button onclick="goToHome()" class="flex items-center gap-2 group cursor-pointer text-left">
      <span class="text-2xl group-hover:scale-110 transition-transform">🌲</span>
      <div>
        <h1 class="text-2xl font-bold text-emerald-200 tracking-wide flex items-center gap-1.5">
          마음 숲 정원 <span class="text-yellow-300 text-base">⭐</span>
        </h1>
        <p class="text-xs text-emerald-400/80 font-sans-kr font-light">나를 편안히 안아주는 고요한 쉼터</p>
      </div>
    </button>
    <div class="flex items-center gap-2 text-emerald-300/80 text-sm">
      <span>🍀</span>
      <span class="hidden sm:inline font-sans-kr text-xs">포근한 쉼</span>
    </div>
  </header>

  <!-- 메인 콘텐츠 컨테이너 -->
  <main class="w-full max-w-2xl px-4 py-6 flex-1 z-10 flex flex-col justify-center">

    <!-- [1] 홈 화면 (메뉴 선택) -->
    <section id="screen-home" class="space-y-6">
      <div class="bg-[#12222e]/90 border border-emerald-800/50 rounded-3xl p-6 sm:p-8 text-center shadow-2xl relative overflow-hidden backdrop-blur-sm">
        <div class="absolute -top-6 -right-6 text-6xl opacity-10 pointer-events-none">🌳</div>
        <div class="inline-block bg-[#1a382b]/80 border border-emerald-600/40 px-4 py-1.5 rounded-full text-emerald-200 text-sm mb-4">
          ☘️ 조용한 숲속에서 쉬어가기 ☘️
        </div>
        <h2 class="text-3xl sm:text-4xl font-bold text-white mb-3">
          지금 마음에 필요한 것은 무엇인가요?
        </h2>
        <p class="text-emerald-300/90 text-lg leading-relaxed font-sans-kr font-light">
          거센 파도가 일 때도 숲은 조용히 자리를 지킵니다.<br>
          당신의 속도에 맞춰 한 걸음씩 가볍게 머물러보세요.
        </p>

        <!-- 핵심 문구 배너 -->
        <div class="mt-6 bg-[#0f2a20]/90 border border-emerald-500/40 rounded-2xl py-3.5 px-4 text-emerald-100 font-bold text-lg sm:text-xl shadow-inner flex items-center justify-center gap-2">
          <span class="text-yellow-300">⭐</span>
          <span>"'왜' 보다는 '어떻게'를 생각하기. 나는 끔찍이보다 부지런하다!"</span>
          <span class="text-yellow-300">⭐</span>
        </div>
      </div>

      <!-- 3가지 메뉴 카드 -->
      <div class="grid grid-cols-1 gap-4 font-sans-kr">
        <!-- 1. 호흡하기 -->
        <button onclick="startBreathing()" class="group bg-gradient-to-r from-[#142938] to-[#123126] hover:from-[#193548] hover:to-[#174031] border border-emerald-700/50 rounded-2xl p-5 text-left transition-all duration-300 shadow-lg hover:shadow-emerald-950/50 hover:-translate-y-1 flex items-center justify-between cursor-pointer">
          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-2xl bg-[#1b4332] flex items-center justify-center text-3xl shadow-inner group-hover:scale-105 transition-transform">
              🌙
            </div>
            <div>
              <div class="flex items-center gap-2">
                <h3 class="text-xl font-bold text-emerald-100 font-['Gaegu'] text-2xl">1. 호흡하기</h3>
                <span class="text-xs bg-emerald-900/60 text-emerald-300 px-2 py-0.5 rounded-full border border-emerald-700/40">4초 들숨 · 6초 날숨</span>
              </div>
              <p class="text-sm text-emerald-400/80 mt-1">밤하늘과 고요한 호수 풍경 속에서 마음의 리듬을 되찾습니다.</p>
            </div>
          </div>
          <span class="text-emerald-400 text-xl group-hover:translate-x-1 transition-transform">➔</span>
        </button>

        <!-- 2. 그라운딩 -->
        <button onclick="startGrounding()" class="group bg-gradient-to-r from-[#142938] to-[#123126] hover:from-[#193548] hover:to-[#174031] border border-emerald-700/50 rounded-2xl p-5 text-left transition-all duration-300 shadow-lg hover:shadow-emerald-950/50 hover:-translate-y-1 flex items-center justify-between cursor-pointer">
          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-2xl bg-[#1b4332] flex items-center justify-center text-3xl shadow-inner group-hover:scale-105 transition-transform">
              🌿
            </div>
            <div>
              <div class="flex items-center gap-2">
                <h3 class="text-xl font-bold text-emerald-100 font-['Gaegu'] text-2xl">2. 그라운딩 (5-4-3-2-1)</h3>
                <span class="text-xs bg-emerald-900/60 text-emerald-300 px-2 py-0.5 rounded-full border border-emerald-700/40">감각 깨우기</span>
              </div>
              <p class="text-sm text-emerald-400/80 mt-1">오감을 천천히 일깨워 불안한 생각 대신 '지금, 여기'에 닻을 내립니다.</p>
            </div>
          </div>
          <span class="text-emerald-400 text-xl group-hover:translate-x-1 transition-transform">➔</span>
        </button>

        <!-- 3. 그림자 탈출 매뉴얼 -->
        <button onclick="startShadowEscape()" class="group bg-gradient-to-r from-[#142938] to-[#123126] hover:from-[#193548] hover:to-[#174031] border border-emerald-700/50 rounded-2xl p-5 text-left transition-all duration-300 shadow-lg hover:shadow-emerald-950/50 hover:-translate-y-1 flex items-center justify-between cursor-pointer">
          <div class="flex items-center gap-4">
            <div class="w-14 h-14 rounded-2xl bg-[#1b4332] flex items-center justify-center text-3xl shadow-inner group-hover:scale-105 transition-transform">
              🧭
            </div>
            <div>
              <div class="flex items-center gap-2">
                <h3 class="text-xl font-bold text-emerald-100 font-['Gaegu'] text-2xl">3. 그림자 탈출 매뉴얼</h3>
                <span class="text-xs bg-emerald-900/60 text-emerald-300 px-2 py-0.5 rounded-full border border-emerald-700/40">생각의 길잡이</span>
              </div>
              <p class="text-sm text-emerald-400/80 mt-1">우울, 불안, 무기력의 원인을 분류하고 따뜻한 심리학적 해법을 만납니다.</p>
            </div>
          </div>
          <span class="text-emerald-400 text-xl group-hover:translate-x-1 transition-transform">➔</span>
        </button>
      </div>
    </section>

    <!-- [2] 호흡하기 화면 -->
    <section id="screen-breathing" class="hidden space-y-5">
      <!-- 준비 단계 안내 -->
      <div id="breathe-prep-box" class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 sm:p-8 text-center space-y-4">
        <div class="text-5xl">🧘‍♀️</div>
        <h2 class="text-3xl font-bold text-white">호흡을 위한 준비</h2>
        <div class="bg-[#173024] p-5 rounded-2xl border border-emerald-700/40 text-emerald-200 text-lg leading-relaxed font-sans-kr">
          몸을 편안하게 이완하고 눈을 지그시 감습니다.<br>
          어깨의 힘을 툭 빼고, 턱과 미간의 긴장을 부드럽게 풀어주세요.
        </div>
        <p class="text-sm text-emerald-400/80 font-sans-kr">
          4초간 밤하늘의 맑은 공기를 들이쉬고, 6초간 호수의 물결처럼 천천히 내쉽니다.<br>
          총 10번의 호흡 사이클이 진행됩니다.
        </p>
        <button onclick="runBreatheCycle()" class="w-full bg-[#2d6144] hover:bg-[#3b7a57] text-white py-3.5 px-6 rounded-2xl font-bold text-2xl transition-all shadow-lg active:scale-95 cursor-pointer">
          호흡 시작하기 🌲
        </button>
      </div>

      <!-- 실제 호흡 루프 화면 -->
      <div id="breathe-active-box" class="hidden bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 sm:p-8 flex flex-col items-center text-center relative overflow-hidden">
        <!-- 상단 사이클 인디케이터 -->
        <div class="flex items-center justify-between w-full mb-4 px-2">
          <span class="text-sm font-sans-kr text-emerald-400 bg-emerald-950/60 px-3 py-1 rounded-full border border-emerald-800/40">
            반복 횟수: <strong id="breathe-cycle-count" class="text-white text-base">1</strong> / 10회
          </span>
          <button onclick="stopBreathing()" class="text-xs font-sans-kr text-gray-400 hover:text-white underline cursor-pointer">
            그만하기
          </button>
        </div>

        <!-- 호흡 풍경 이미지 뷰어 -->
        <div class="w-full h-56 sm:h-64 rounded-2xl overflow-hidden relative shadow-2xl mb-6 border border-emerald-600/30">
          <!-- 들숨: 밤하늘 이미지 -->
          <img id="img-inhale" 
               src="https://images.unsplash.com/photo-1506703719100-a0f3a48c0f86?auto=format&fit=crop&w=1000&q=80" 
               alt="고요한 밤하늘과 별" 
               class="absolute inset-0 w-full h-full object-cover transition-opacity duration-1000 opacity-100">
          
          <!-- 날숨: 숲과 호수 이미지 -->
          <img id="img-exhale" 
               src="https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=1000&q=80" 
               alt="안개 낀 고요한 숲과 호수" 
               class="absolute inset-0 w-full h-full object-cover transition-opacity duration-1000 opacity-0">

          <div class="absolute inset-0 bg-black/30 backdrop-blur-[1px]"></div>

          <!-- 중앙 시각화 호흡 구 -->
          <div class="absolute inset-0 flex flex-col items-center justify-center">
            <div id="breathe-circle" class="w-32 h-32 rounded-full border-4 border-yellow-300/80 bg-emerald-500/20 backdrop-blur-md flex flex-col items-center justify-center shadow-[0_0_30px_rgba(253,224,71,0.3)] transition-all">
              <span id="breathe-phase-text" class="text-2xl font-bold text-white drop-shadow">들이쉬기</span>
              <span id="breathe-timer" class="text-4xl font-bold text-yellow-300 drop-shadow">4</span>
            </div>
          </div>
        </div>

        <p id="breathe-guide-comment" class="text-xl text-emerald-200 font-sans-kr font-medium">
          밤하늘의 맑은 별빛 기운을 천천히 들이마십니다.
        </p>
      </div>
    </section>

    <!-- [3] 그라운딩 (5-4-3-2-1) 화면 -->
    <section id="screen-grounding" class="hidden space-y-5 font-sans-kr">
      <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 sm:p-8">
        <div class="flex items-center justify-between mb-4 border-b border-emerald-800/40 pb-3">
          <div class="flex items-center gap-2">
            <span class="text-2xl">🌿</span>
            <h2 class="text-2xl font-bold text-white font-['Gaegu'] text-3xl">5-4-3-2-1 감각 그라운딩</h2>
          </div>
          <span id="grounding-step-badge" class="bg-emerald-900/70 border border-emerald-700/50 text-emerald-300 text-xs px-3 py-1 rounded-full font-medium">
            1단계 / 총 5단계
          </span>
        </div>

        <div id="grounding-content-area" class="space-y-4">
          <!-- 단계별 동적 질문 렌더링 -->
        </div>

        <!-- 하단 네비게이션 버튼 -->
        <div class="flex justify-between items-center mt-6 pt-4 border-t border-emerald-800/30">
          <button id="grounding-prev-btn" onclick="prevGroundingStep()" class="text-emerald-400 hover:text-emerald-200 text-sm py-2 px-4 rounded-xl border border-emerald-800 cursor-pointer">
            이전
          </button>
          <button id="grounding-next-btn" onclick="nextGroundingStep()" class="bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 px-6 rounded-xl font-bold text-base transition-all shadow-md active:scale-95 cursor-pointer">
            다음 감각으로 ➔
          </button>
        </div>
      </div>
    </section>

    <!-- [4] 그림자 탈출 매뉴얼 화면 -->
    <section id="screen-shadow" class="hidden space-y-5">
      <!-- 4-1 감정 대분류 선택 -->
      <div id="shadow-step-1" class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 sm:p-8 space-y-5">
        <div class="text-center space-y-2">
          <span class="text-4xl">🧭</span>
          <h2 class="text-3xl font-bold text-white">지금 어떤 그림자가 머물고 있나요?</h2>
          <p class="text-emerald-300/80 text-sm font-sans-kr">솔직한 내 마음의 신호에 귀를 기울여주세요.</p>
        </div>

        <div class="grid grid-cols-1 gap-3 font-sans-kr text-base">
          <button onclick="selectEmotion('depression')" class="w-full p-4 rounded-2xl bg-[#142938] hover:bg-[#1a384e] border border-emerald-700/40 text-left flex items-center justify-between text-white font-medium transition cursor-pointer">
            <span>🌧️ 우울한가요?</span>
            <span class="text-emerald-400 text-sm">선택 ➔</span>
          </button>
          <button onclick="selectEmotion('anxiety')" class="w-full p-4 rounded-2xl bg-[#142938] hover:bg-[#1a384e] border border-emerald-700/40 text-left flex items-center justify-between text-white font-medium transition cursor-pointer">
            <span>⚡ 불안한가요?</span>
            <span class="text-emerald-400 text-sm">선택 ➔</span>
          </button>
          <button onclick="selectEmotion('lethargy')" class="w-full p-4 rounded-2xl bg-[#142938] hover:bg-[#1a384e] border border-emerald-700/40 text-left flex items-center justify-between text-white font-medium transition cursor-pointer">
            <span>🥀 우울하고 불안한데 무기력까지?</span>
            <span class="text-emerald-400 text-sm">선택 ➔</span>
          </button>
          <button onclick="selectEmotion('denial')" class="w-full p-4 rounded-2xl bg-[#142938] hover:bg-[#1a384e] border border-emerald-700/40 text-left flex items-center justify-between text-white font-medium transition cursor-pointer">
            <span>🌫️ 내가 내 감정을 부정하고 있음</span>
            <span class="text-emerald-400 text-sm">선택 ➔</span>
          </button>
        </div>
      </div>

      <!-- 4-2 세부 이유 및 솔루션 컨테이너 -->
      <div id="shadow-step-2" class="hidden space-y-4">
        <button onclick="backToEmotionSelect()" class="text-sm font-sans-kr text-emerald-400 hover:text-emerald-200 flex items-center gap-1 cursor-pointer">
          <span>⬅</span> 감정 다시 선택하기
        </button>
        <div id="shadow-detail-content" class="space-y-4">
          <!-- 동적 컨텐츠 주입 -->
        </div>
      </div>
    </section>

    <!-- [5] 세션 완료 & 불안/우울 점수 체크 & 숲의 우체통 화면 -->
    <section id="screen-score" class="hidden space-y-6">
      <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 sm:p-8 space-y-6">
        <div class="text-center space-y-2">
          <div class="text-4xl">☘️</div>
          <h2 class="text-3xl font-bold text-white">마음 돌봄 세션을 마쳤습니다</h2>
          <p class="text-emerald-300/80 font-sans-kr text-sm">지금 느끼는 불안이나 우울의 정도는 몇 점인가요?</p>
        </div>

        <!-- 점수 슬라이더 -->
        <div class="bg-[#162c22] p-6 rounded-2xl border border-emerald-700/40 space-y-4 font-sans-kr">
          <div class="flex justify-between items-center">
            <span class="text-sm text-emerald-300">편안하고 고요함 (0점)</span>
            <span id="score-display" class="text-3xl font-bold text-yellow-300 font-['Gaegu']">5점</span>
            <span class="text-sm text-emerald-300">매우 높고 버거움 (10점)</span>
          </div>
          <input id="score-slider" type="range" min="0" max="10" value="5" oninput="updateScoreVal(this.value)" class="w-full accent-emerald-500 cursor-pointer h-2 bg-[#0c1520] rounded-lg">
          <div class="flex justify-between text-xs text-emerald-400/60 px-1">
            <span>0</span><span>1</span><span>2</span><span>3</span><span>4</span><span>5</span><span>6</span><span>7</span><span>8</span><span>9</span><span>10</span>
          </div>
        </div>

        <!-- 숲의 우체통에서 온 편지 카드 -->
        <div class="bg-gradient-to-b from-[#183a2d] to-[#12281e] border-2 border-emerald-500/50 rounded-2xl p-6 shadow-xl relative overflow-hidden">
          <div class="flex items-center justify-between border-b border-emerald-600/40 pb-3 mb-4">
            <span class="text-emerald-200 font-bold flex items-center gap-1.5 text-lg">
              📬 숲의 우체통에서 온 편지
            </span>
            <button onclick="drawRandomQuote()" class="text-xs font-sans-kr bg-emerald-900/60 hover:bg-emerald-800 text-emerald-200 border border-emerald-700 px-2.5 py-1 rounded-lg transition cursor-pointer">
              다른 편지 열어보기 ↺
            </button>
          </div>

          <div id="postbox-quote-text" class="text-emerald-50 font-sans-kr text-base leading-relaxed whitespace-pre-line mb-3 font-normal min-h-[90px] flex items-center">
            <!-- 편지 문장 주입 -->
          </div>

          <div id="postbox-quote-source" class="text-right text-xs text-emerald-400/90 font-sans-kr font-medium">
            <!-- 출처 -->
          </div>
        </div>

        <!-- 다시 홈으로 버튼 -->
        <button onclick="goToHome()" class="w-full bg-[#2d6144] hover:bg-[#3b7a57] text-white py-3.5 px-6 rounded-2xl font-bold text-xl transition-all shadow-md active:scale-95 cursor-pointer">
          정원 입구로 돌아가기 🌲
        </button>
      </div>
    </section>

  </main>

  <!-- 하단 푸터 -->
  <footer class="w-full max-w-2xl px-6 py-6 text-center text-xs text-emerald-500/60 font-sans-kr border-t border-emerald-950/60 z-10 flex flex-col items-center gap-1.5">
    <div class="flex items-center gap-2 text-sm text-emerald-400/80">
      <span>🌲</span>
      <span>당신의 마음에 언제나 푸른 숲이 깃들기를</span>
      <span>⭐</span>
    </div>
  </footer>

  <!-- 자바스크립트 로직 -->
  <script>
    // ==========================================
    // 1. 공통 네비게이션 & 화면 전환
    // ==========================================
    const screens = ['screen-home', 'screen-breathing', 'screen-grounding', 'screen-shadow', 'screen-score'];

    function switchScreen(targetScreenId) {
      screens.forEach(id => {
        const el = document.getElementById(id);
        if (el) el.classList.add('hidden');
      });
      const target = document.getElementById(targetScreenId);
      if (target) {
        target.classList.remove('hidden');
        window.scrollTo({ top: 0, behavior: 'smooth' });
      }
    }

    function goToHome() {
      stopBreathing();
      switchScreen('screen-home');
    }

    function openScoreCheck() {
      stopBreathing();
      drawRandomQuote();
      switchScreen('screen-score');
    }

    // ==========================================
    // 2. 모바일 친화적 노션 링크 열기 & 복사 로직
    // ==========================================
    const NOTION_URL = "https://www.notion.so/3b8ad9816a198011805ff67aa4e8857b";

    function openNotionLink(url) {
      try {
        const isMobile = /iPhone|iPad|iPod|Android/i.test(navigator.userAgent);
        
        if (isMobile) {
          // 모바일 인앱 브라우저나 새창 차단 방지: 먼저 새 창 시도 후 실패 시 현재 창 전환
          const newWin = window.open(url, '_blank');
          if (!newWin || newWin.closed || typeof newWin.closed === 'undefined') {
            window.location.href = url;
          }
        } else {
          window.open(url, '_blank', 'noopener,noreferrer');
        }
      } catch (err) {
        window.location.href = url;
      }
    }

    function copyNotionLink(url) {
      if (navigator.clipboard && window.isSecureContext) {
        navigator.clipboard.writeText(url).then(() => {
          alert("노션 링크가 복사되었습니다! 사파리, 크롬 또는 노션 앱에 붙여넣어 주세요.");
        }).catch(() => fallbackCopy(url));
      } else {
        fallbackCopy(url);
      }
    }

    function fallbackCopy(text) {
      const input = document.createElement("input");
      input.value = text;
      document.body.appendChild(input);
      input.select();
      document.execCommand("copy");
      document.body.removeChild(input);
      alert("노션 링크가 복사되었습니다! 사파리, 크롬 또는 노션 앱에 붙여넣어 주세요.");
    }

    // ==========================================
    // 3. 호흡하기 모듈 (4초 들숨, 6초 날숨, 10회 반복)
    // ==========================================
    let breatheInterval = null;
    let breatheCycle = 1;
    let isBreathing = false;

    function startBreathing() {
      switchScreen('screen-breathing');
      document.getElementById('breathe-prep-box').classList.remove('hidden');
      document.getElementById('breathe-active-box').classList.add('hidden');
      breatheCycle = 1;
    }

    function runBreatheCycle() {
      document.getElementById('breathe-prep-box').classList.add('hidden');
      document.getElementById('breathe-active-box').classList.remove('hidden');
      isBreathing = true;
      breatheCycle = 1;
      executeSingleCycle();
    }

    function executeSingleCycle() {
      if (!isBreathing) return;
      if (breatheCycle > 10) {
        stopBreathing();
        openScoreCheck();
        return;
      }

      document.getElementById('breathe-cycle-count').innerText = breatheCycle;
      const circle = document.getElementById('breathe-circle');
      const phaseText = document.getElementById('breathe-phase-text');
      const timerText = document.getElementById('breathe-timer');
      const guideText = document.getElementById('breathe-guide-comment');
      const imgInhale = document.getElementById('img-inhale');
      const imgExhale = document.getElementById('img-exhale');

      // 1) 4초간 들이쉬기 (밤하늘 이미지 표시)
      imgInhale.classList.replace('opacity-0', 'opacity-100');
      imgExhale.classList.replace('opacity-100', 'opacity-0');
      circle.classList.remove('breathe-contract');
      circle.classList.add('breathe-expand');
      phaseText.innerText = "들이쉬기";
      guideText.innerText = "밤하늘의 맑은 별빛 기운을 천천히 들이마십니다.";

      let timeLeft = 4;
      timerText.innerText = timeLeft;

      breatheInterval = setInterval(() => {
        timeLeft--;
        if (timeLeft > 0) {
          timerText.innerText = timeLeft;
        } else {
          clearInterval(breatheInterval);
          if (!isBreathing) return;

          // 2) 6초간 내쉬기 (호수와 나무 이미지 표시)
          imgInhale.classList.replace('opacity-100', 'opacity-0');
          imgExhale.classList.replace('opacity-0', 'opacity-100');
          circle.classList.remove('breathe-expand');
          circle.classList.add('breathe-contract');
          phaseText.innerText = "내쉬기";
          guideText.innerText = "호수 물결에 무거운 마음을 실어 가볍게 내보냅니다.";

          let exhaleTime = 6;
          timerText.innerText = exhaleTime;

          breatheInterval = setInterval(() => {
            exhaleTime--;
            if (exhaleTime > 0) {
              timerText.innerText = exhaleTime;
            } else {
              clearInterval(breatheInterval);
              if (isBreathing) {
                breatheCycle++;
                executeSingleCycle();
              }
            }
          }, 1000);
        }
      }, 1000);
    }

    function stopBreathing() {
      isBreathing = false;
      if (breatheInterval) clearInterval(breatheInterval);
    }

    // ==========================================
    // 4. 그라운딩 (5-4-3-2-1) 모듈
    // ==========================================
    const groundingSteps = [
      {
        step: 5,
        title: "보이는 것 5가지 찾기",
        guide: "지금 보이는 것 5가지를 찾아, 색과 모양을 적어주세요.",
        placeholder: "예: 갈색 나무 책상 모서리, 노란색 연필, 하얀색 머그컵...",
        icon: "👁️"
      },
      {
        step: 4,
        title: "만져지는 것 4가지 찾기",
        guide: "손끝에 닿는 것 4가지의 질감(딱딱함·부드러움·차가움)을 느껴보세요.",
        placeholder: "예: 옷감의 부드러움, 스마트폰의 시원한 유리 질감, 의자의 단단함...",
        icon: "✋"
      },
      {
        step: 3,
        title: "들리는 소리 3가지 찾기",
        guide: "들리는 소리 3가지를 찾아보세요. 멀리 있는 소리도 좋습니다.",
        placeholder: "예: 시계 초침 소리, 창밖 바람 소리, 냉장고의 웅 하는 모터 소리...",
        icon: "👂"
      },
      {
        step: 2,
        title: "맡을 수 있는 냄새 2가지 찾기",
        guide: "맡을 수 있는 냄새 2가지를 찾아봅니다. 없다면 좋아하는 향을 떠올려도 됩니다.",
        placeholder: "예: 종이 냄새, 은은한 섬유유연제 향, 샌달우드 비누 향...",
        icon: "👃"
      },
      {
        step: 1,
        title: "느껴지는 맛 1가지 찾기",
        guide: "입안의 맛이나 물 한 모금의 감각 1가지에 집중해 보세요.",
        placeholder: "예: 방금 마신 시원한 물의 개운함, 차의 쌉싸름함...",
        icon: "👅"
      }
    ];

    let currentGroundingIdx = 0;
    const groundingAnswers = ["", "", "", "", ""];

    function startGrounding() {
      currentGroundingIdx = 0;
      switchScreen('screen-grounding');
      renderGroundingStep();
    }

    function renderGroundingStep() {
      const stepData = groundingSteps[currentGroundingIdx];
      document.getElementById('grounding-step-badge').innerText = `${currentGroundingIdx + 1}단계 / 총 5단계`;
      
      const container = document.getElementById('grounding-content-area');
      container.innerHTML = `
        <div class="space-y-3">
          <div class="flex items-center gap-2">
            <span class="text-3xl">${stepData.icon}</span>
            <h3 class="text-xl font-bold text-emerald-100 font-['Gaegu'] text-2xl">${stepData.title}</h3>
          </div>
          <p class="text-emerald-300 font-medium text-base">${stepData.guide}</p>
          <textarea id="grounding-input" rows="4" 
            class="w-full bg-[#0c1520] border border-emerald-700/60 rounded-xl p-3.5 text-white placeholder-emerald-700/70 focus:outline-none focus:border-emerald-400 text-sm leading-relaxed" 
            placeholder="${stepData.placeholder}">${groundingAnswers[currentGroundingIdx] || ""}</textarea>
        </div>
      `;

      // 이전 버튼 비활성화 여부
      const prevBtn = document.getElementById('grounding-prev-btn');
      if (currentGroundingIdx === 0) {
        prevBtn.classList.add('opacity-40', 'pointer-events-none');
      } else {
        prevBtn.classList.remove('opacity-40', 'pointer-events-none');
      }

      // 다음/완료 버튼 라벨
      const nextBtn = document.getElementById('grounding-next-btn');
      if (currentGroundingIdx === 4) {
        nextBtn.innerHTML = "그라운딩 완료하고 점수 체크 ➔";
      } else {
        nextBtn.innerHTML = "다음 감각으로 ➔";
      }
    }

    function saveCurrentGroundingInput() {
      const inputEl = document.getElementById('grounding-input');
      if (inputEl) {
        groundingAnswers[currentGroundingIdx] = inputEl.value;
      }
    }

    function prevGroundingStep() {
      saveCurrentGroundingInput();
      if (currentGroundingIdx > 0) {
        currentGroundingIdx--;
        renderGroundingStep();
      }
    }

    function nextGroundingStep() {
      saveCurrentGroundingInput();
      if (currentGroundingIdx < 4) {
        currentGroundingIdx++;
        renderGroundingStep();
      } else {
        openScoreCheck();
      }
    }

    // ==========================================
    // 5. 그림자 탈출 매뉴얼 모듈
    // ==========================================
    function startShadowEscape() {
      switchScreen('screen-shadow');
      document.getElementById('shadow-step-1').classList.remove('hidden');
      document.getElementById('shadow-step-2').classList.add('hidden');
    }

    function backToEmotionSelect() {
      document.getElementById('shadow-step-1').classList.remove('hidden');
      document.getElementById('shadow-step-2').classList.add('hidden');
    }

    function selectEmotion(type) {
      document.getElementById('shadow-step-1').classList.add('hidden');
      const detailStep = document.getElementById('shadow-step-2');
      detailStep.classList.remove('hidden');

      const contentBox = document.getElementById('shadow-detail-content');

      if (type === 'depression') {
        renderDepressionMenu(contentBox);
      } else if (type === 'anxiety') {
        renderAnxietyMenu(contentBox);
      } else if (type === 'lethargy') {
        renderLethargyMenu(contentBox);
      } else if (type === 'denial') {
        renderDenialMenu(contentBox);
      }
    }

    // 5-1. 우울 메뉴
    function renderDepressionMenu(el) {
      el.innerHTML = `
        <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 space-y-4">
          <div class="border-b border-emerald-800/40 pb-3">
            <h3 class="text-2xl font-bold text-white font-['Gaegu'] text-3xl">🌧️ 우울 - 마음의 이유 들여다보기</h3>
            <p class="text-xs text-emerald-400 font-sans-kr mt-1">지금 마음에 닿는 이유를 하나 골라보세요.</p>
          </div>
          <div class="space-y-3 font-sans-kr text-sm">
            <button onclick="showDepressionDetail(1)" class="w-full text-left p-3.5 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (1) 불안해서 우울하다
            </button>
            <button onclick="showDepressionDetail(2)" class="w-full text-left p-3.5 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (2) 삶의 이유를 몰라서 우울하다
            </button>
            <button onclick="showDepressionDetail(3)" class="w-full text-left p-3.5 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (3) 완벽하지 못한 내가 너무 싫어서 우울하다
            </button>
          </div>
          <div id="depression-sub-result" class="mt-4 font-sans-kr"></div>
        </div>
      `;
    }

    function showDepressionDetail(idx) {
      const res = document.getElementById('depression-sub-result');
      if (idx === 1) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3">
            <h4 class="font-bold text-emerald-200 text-base">🌱 잘못된 패턴을 알아차리고 무엇을 하면 되는지 생각하기</h4>
            <blockquote class="bg-[#0f1f17] p-4 rounded-xl text-emerald-100/90 text-sm leading-relaxed border-l-4 border-emerald-500">
              “이런 잘못된 패턴이 감지되면 ‘아 망했어, 나는 또 우울해졌어, 여전히 나는 불안해, 결코 나는 좋아지지 않을 거야, 나는 틀렸어’라고 말하기보다 <strong>‘음 내가 또 이전 패턴대로 하고 있었구나, 지금부터 다르게 살아야지’</strong>라고 생각하고, 올바른 행동을 다시 연습하고 실천하면 된다.”
              <div class="text-right text-xs text-emerald-400 mt-2">— 이번 생은 망한 것 같아? 2회차 인생! 『잠 못 드는 당신을 위한 밤의 심리학』</div>
            </blockquote>
            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 2) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3">
            <h4 class="font-bold text-emerald-200 text-base">🌸 좋아하는 일 한 가지 해보기</h4>
            <p class="text-sm text-emerald-200/90 leading-relaxed">
              거창한 목표나 삶의 거대한 이유를 지금 당장 찾지 않아도 괜찮습니다. 오늘 나를 기분 좋게 해주는 소박한 일 하나를 선물해 보세요.
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-2 text-xs text-emerald-200 mt-2">
              <div class="p-2.5 bg-[#0f241a] rounded-lg border border-emerald-800/60">📖 차분하게 독서하기</div>
              <div class="p-2.5 bg-[#0f241a] rounded-lg border border-emerald-800/60">🏃‍♀️ 좋아하는 노래 들으며 러닝하기</div>
              <div class="p-2.5 bg-[#0f241a] rounded-lg border border-emerald-800/60">🏊‍♀️ 물살을 가르며 수영하기</div>
              <div class="p-2.5 bg-[#0f241a] rounded-lg border border-emerald-800/60">🪵 따뜻한 샌달우드 향으로 샤워하기</div>
              <div class="p-2.5 bg-[#0f241a] rounded-lg border border-emerald-800/60 col-span-1 sm:col-span-2">🧶 편안한 드라마 보며 손뜨개질하기</div>
            </div>
            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 3) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3">
            <h4 class="font-bold text-emerald-200 text-base">📝 사고기록지 작성하기</h4>
            <p class="text-sm text-emerald-200/90 leading-relaxed">
              생각을 종이나 기록장에 풀어내어 객관적인 관찰자의 시선으로 바라봅니다.<br>
              <strong>흐름:</strong> 사건 ➔ 신체 반응 ➔ 자동적 사고 ➔ 감정 ➔ 지지 증거와 반대 증거 ➔ 대안적 신념 ➔ 균형 잡힌 사고 ➔ 재평가
            </p>
            
            <!-- 모바일 최적화 노션 링크 버튼 영역 -->
            <div class="flex flex-col sm:flex-row gap-2 mt-4 w-full justify-center items-center">
              <button type="button" 
                      onclick="openNotionLink('${NOTION_URL}')" 
                      class="w-full sm:w-auto inline-flex items-center justify-center gap-2 bg-[#2d6144] hover:bg-[#3b7a57] text-white px-5 py-3 rounded-xl font-bold shadow-md active:scale-95 transition-all text-sm cursor-pointer">
                <span>📓 모바일 노션에서 사고기록지 열기</span>
                <span class="text-xs bg-white/20 px-2 py-0.5 rounded-full">새 창</span>
              </button>
              <button type="button" 
                      onclick="copyNotionLink('${NOTION_URL}')" 
                      class="w-full sm:w-auto inline-flex items-center justify-center gap-1.5 bg-[#14261c] hover:bg-[#1d3829] text-emerald-300 border border-emerald-700/60 px-4 py-3 rounded-xl text-xs font-medium transition-all active:scale-95 cursor-pointer">
                <span>📋 링크 복사</span>
              </button>
            </div>

            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#1d3d2c] hover:bg-[#28573e] text-emerald-200 py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      }
    }

    // 5-2. 불안 메뉴
    function renderAnxietyMenu(el) {
      el.innerHTML = `
        <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 space-y-4">
          <div class="border-b border-emerald-800/40 pb-3">
            <h3 class="text-2xl font-bold text-white font-['Gaegu'] text-3xl">⚡ 불안 - 마음의 파도 다독이기</h3>
            <p class="text-xs text-emerald-400 font-sans-kr mt-1">어떤 이유로 마음이 요동치고 있나요?</p>
          </div>
          <div class="space-y-2.5 font-sans-kr text-sm">
            <button onclick="showAnxietyDetail(1)" class="w-full text-left p-3 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (1) 실수한 일을 반추하고 있다
            </button>
            <button onclick="showAnxietyDetail(2)" class="w-full text-left p-3 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (2) “나는 무능력한 사람이다” 버튼이 눌림
            </button>
            <button onclick="showAnxietyDetail(3)" class="w-full text-left p-3 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (3) 일어나지 않은 일을 걱정하고 있다
            </button>
            <button onclick="showAnxietyDetail(4)" class="w-full text-left p-3 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (4) 사람들이 나를 싫어할까 불안하다
            </button>
            <button onclick="showAnxietyDetail(5)" class="w-full text-left p-3 rounded-xl bg-[#173024] hover:bg-[#1f4232] border border-emerald-700/50 text-emerald-100 font-medium transition cursor-pointer">
              (5) 남들보다 뒤처졌다고 생각한다
            </button>
          </div>
          <div id="anxiety-sub-result" class="mt-4 font-sans-kr"></div>
        </div>
      `;
    }

    function showAnxietyDetail(idx) {
      const res = document.getElementById('anxiety-sub-result');
      if (idx === 1) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-4 text-sm leading-relaxed">
            <div class="bg-[#0f241a] p-4 rounded-xl border border-emerald-700/40 text-emerald-200">
              <strong class="text-yellow-300 block mb-2 text-base">⚠️ 사후 처리의 악순환 알아차리기</strong>
              사후 처리는 특정한 사회적 경험이 머릿속에 떠오르면서 시작됩니다. 그러면 자신이 한 말이나 행동이 당신이나 타인에게 해를 끼쳤을지도 모른다는 의심과 불확실성이 커집니다.<br><br>
              이런 의심이나 불확실성은 불안감과 걱정을 키웁니다. 이를 해소하기 위해 자신이나 남에게 해를 끼쳤음을 암시하는 단서를 찾기 위해 기억을 더듬어보게 됩니다.<br><br>
              이런 기억을 되새길수록 불안과 걱정이 더욱 커지는 악순환에서 빠져나올 수 없게 되고, 당시의 경험이 더욱 강렬하고 힘들게 느껴집니다. 결국 사후 처리에 몰입할수록 불안과 걱정이 줄어들지 않고 괴로움만 커집니다.
            </div>

            <div class="bg-[#12281e] p-4 rounded-xl border border-emerald-600/40 space-y-2 text-emerald-100">
              <strong class="text-white text-base block">💡 ACTION 모델로 반추 끊어내기</strong>
              <ul class="space-y-1.5 text-xs sm:text-sm">
                <li><strong class="text-emerald-300">• Assessment (평가):</strong> 지금 내가 하려는 반추가 '회피'인가, 내게 도움 되는 '대처/가치 기반 행동'인가?</li>
                <li><strong class="text-emerald-300">• Choose (선택):</strong> 반추 말고 나에게 진짜 도움이 되는 건강한 행동을 하나 선택하기</li>
                <li><strong class="text-emerald-300">• Try (시도):</strong> 되든 안 되든 일단 가볍게 시도해 보기</li>
                <li><strong class="text-emerald-300">• Integrate (통합):</strong> 반추를 더 빨리 알아차리고 끊어낼 수 있도록 일상에서 신호를 만들어 습관화하기</li>
                <li><strong class="text-emerald-300">• Observation (관찰):</strong> 스스로를 비난하거나 평가하지 말고 그저 한 걸음 물러서서 관찰하기</li>
                <li><strong class="text-emerald-300">• Never give up (지속):</strong> 조급해하지 말고 부드럽게 계속 연습해 나가기</li>
              </ul>
            </div>
            <button onclick="openScoreCheck()" class="w-full bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 2) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3">
            <h4 class="font-bold text-emerald-200 text-base">📝 사고기록지로 자동적 사고 점검하기</h4>
            <p class="text-sm text-emerald-200/90 leading-relaxed">
              "나는 무능력하다"라는 생각은 사실이 아니라, 순간적으로 튀어나온 <strong>'마음의 왜곡된 필터'</strong>일 뿐입니다. 객관적인 증거를 기록해 보세요.
            </p>
            
            <!-- 모바일 최적화 노션 링크 버튼 -->
            <div class="flex flex-col sm:flex-row gap-2 mt-4 w-full justify-center items-center">
              <button type="button" 
                      onclick="openNotionLink('${NOTION_URL}')" 
                      class="w-full sm:w-auto inline-flex items-center justify-center gap-2 bg-[#2d6144] hover:bg-[#3b7a57] text-white px-5 py-3 rounded-xl font-bold shadow-md active:scale-95 transition-all text-sm cursor-pointer">
                <span>📓 모바일 노션에서 사고기록지 열기</span>
                <span class="text-xs bg-white/20 px-2 py-0.5 rounded-full">새 창</span>
              </button>
              <button type="button" 
                      onclick="copyNotionLink('${NOTION_URL}')" 
                      class="w-full sm:w-auto inline-flex items-center justify-center gap-1.5 bg-[#14261c] hover:bg-[#1d3829] text-emerald-300 border border-emerald-700/60 px-4 py-3 rounded-xl text-xs font-medium transition-all active:scale-95 cursor-pointer">
                <span>📋 링크 복사</span>
              </button>
            </div>

            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#1d3d2c] hover:bg-[#28573e] text-emerald-200 py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 3) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3 text-sm">
            <h4 class="font-bold text-emerald-200 text-base">🎯 통제 가능한 것과 불가능한 것의 구분</h4>
            <div class="space-y-2 text-emerald-100/90">
              <div class="p-3 bg-[#0f241a] rounded-xl border border-emerald-800">
                🛑 <strong>불안해서 확인하는 물음 즉시 중단하기!</strong><br>
                “혹시 잘못되면 어쩌지?”, “괜찮을까?” 끝없이 확인하려는 시도는 불안을 가라앉히지 못하고 연료를 더해줄 뿐입니다.
              </div>
              <div class="p-3 bg-[#0f241a] rounded-xl border border-emerald-800">
                🌱 <strong>과도한 책임감 내려놓기</strong><br>
                미래의 모든 변수를 내가 통제할 수는 없습니다. 내가 통제할 수 없는 것은 수용하고, 지금 내가 바로 할 수 있는 작은 일에 집중해 환기해 보세요.
              </div>
            </div>
            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 4) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3 text-sm leading-relaxed">
            <h4 class="font-bold text-emerald-200 text-base">🗣️ 소리 내어 읽고 할 일에 집중하기</h4>
            <div class="space-y-2.5 text-emerald-100">
              <div class="bg-[#0f241a] p-3 rounded-xl border border-emerald-800">
                “다른 사람과의 관계에서 내가 할 수 있는 일은 <strong>‘그 사람에게 최선을 다하는 것’</strong>까지다. 그 이상의 것은 ‘It’s none of my business’, 내가 할 수 있는 일이 아니다. 내가 좋아하는 모두가 나를 좋아하게 만드는 것은 불가능하다. 내가 할 수 있는 일은 내가 좋아하는 사람에게 정성을 다해 내 마음을 보여주는 것까지다.”
              </div>
              <div class="bg-[#0f241a] p-3 rounded-xl border border-emerald-800">
                <em>“역시 내 생각만큼 나쁜 일은 잘 일어나지 않아. 일어난다고 해도 생각보다 별것 없어.”</em>
              </div>
              <div class="bg-[#0f241a] p-3 rounded-xl border border-emerald-800">
                “모든 사람이 나의 모든 것을 좋아해야 한다는 생각을 놓는 순간, 세상살이는 좀 더 편해진다.”
                <span class="block text-right text-xs text-emerald-400 mt-1">— 『잠 못 드는 당신을 위한 밤의 심리학』</span>
              </div>
              <div class="bg-[#0f241a] p-3 rounded-xl border border-emerald-800">
                “누군가 나를 매일매일 100퍼센트 좋아해줄 필요도 없고, 나 역시 누군가를 매일매일 신뢰할 만한 사람으로 생각할 필요도 없다.”
                <span class="block text-right text-xs text-emerald-400 mt-1">— 『나도 아직 나를 모른다』</span>
              </div>
            </div>
            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      } else if (idx === 5) {
        res.innerHTML = `
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3 text-sm">
            <h4 class="font-bold text-emerald-200 text-base">⏳ 지금-여기에서 할 수 있는 것 찾기</h4>
            <p class="text-emerald-200/90 leading-relaxed">
              과거를 후회하는 대신 아래의 문장을 조용히 완성해 보세요:
            </p>
            <div class="bg-[#0f241a] p-4 rounded-xl border border-emerald-700/60 space-y-2 text-emerald-100">
              <p>① 나는 [ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]을(를) 생각하느라 너무 많은 시간을 보냈다.</p>
              <p>② 나는 [ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]을(를) 하는 데 충분한 시간을 보내지 않았다.</p>
              <p>③ 만약 시간을 되돌릴 수 있다면 내가 달리 행동하고 싶은 것은 [ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]이다.</p>
            </div>
            <p class="text-xs text-emerald-300">
              💡 ‘아 내가 이전에 좋지 않았던 패턴대로 또 살기 시작했구나’를 알아차리고, 2회차 삶의 방식을 지금 다시 시작하면 곧 좋아집니다.
            </p>
            <button onclick="openScoreCheck()" class="w-full mt-3 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
              마음 점수 체크하러 가기 ➔
            </button>
          </div>
        `;
      }
    }

    // 5-3. 우울+불안+무기력 메뉴
    function renderLethargyMenu(el) {
      el.innerHTML = `
        <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 space-y-4">
          <div class="border-b border-emerald-800/40 pb-3">
            <h3 class="text-2xl font-bold text-white font-['Gaegu'] text-3xl">🥀 우울, 불안에 무기력까지 겹쳤을 때</h3>
            <p class="text-xs text-emerald-400 font-sans-kr mt-1">에너지가 바닥났을 때는 억지로 힘내지 않아도 됩니다.</p>
          </div>
          <div class="space-y-3 font-sans-kr text-sm">
            <div class="p-3.5 bg-[#172e21] rounded-xl border border-emerald-700/50">
              <span class="text-emerald-300 font-bold block mb-1">내 몸의 신호 확인하기:</span>
              <ul class="list-disc list-inside text-emerald-100 space-y-1 text-xs sm:text-sm">
                <li>심장에 묵직한 통증이나 두근거림이 있다</li>
                <li>온종일 잠만 자고 싶다</li>
                <li>분명 할 일이 있는데도 계속 누워만 있게 된다</li>
              </ul>
            </div>

            <div class="space-y-2 pt-2">
              <span class="text-white font-bold text-sm block">지금 당장 나를 돕는 세 가지 처방:</span>
              <button onclick="startBreathing()" class="w-full text-left p-3 rounded-xl bg-[#142938] hover:bg-[#1a384e] border border-emerald-600/50 text-emerald-100 flex items-center justify-between cursor-pointer">
                <span>🌬️ (1) 호흡하기 메뉴로 이동하여 4·6 호흡하기</span>
                <span class="text-emerald-400 text-xs">이동 ➔</span>
              </button>
              <div class="p-3 rounded-xl bg-[#142938] border border-emerald-700/40 text-emerald-100 text-xs sm:text-sm">
                🛁 <strong>(2) 좋아하는 향(샌달우드)으로 가볍게 샤워하기</strong>
                <p class="text-xs text-emerald-300/80 mt-0.5">따뜻한 물줄기로 지친 몸의 감각을 깨워줍니다.</p>
              </div>
              <div class="p-3 rounded-xl bg-[#142938] border border-emerald-700/40 text-emerald-100 text-xs sm:text-sm">
                ☕ <strong>(3) 좋아하는 커피를 내려 일단 자리에 앉아 계획 세우기</strong>
                <p class="text-xs text-emerald-300/80 mt-0.5">실행하지 않아도 좋습니다. 일단 의자에 앉아 한 모금 마시는 것부터 시작합니다.</p>
              </div>
            </div>
          </div>
          <button onclick="openScoreCheck()" class="w-full mt-4 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
            마음 점수 체크하러 가기 ➔
          </button>
        </div>
      `;
    }

    // 5-4. 감정 부정 메뉴
    function renderDenialMenu(el) {
      el.innerHTML = `
        <div class="bg-[#12222e] border border-emerald-800/60 rounded-3xl p-6 space-y-4 font-sans-kr">
          <div class="border-b border-emerald-800/40 pb-3">
            <h3 class="text-2xl font-bold text-white font-['Gaegu'] text-3xl">🌫️ 내가 내 감정을 부정하고 있을 때</h3>
            <p class="text-xs text-emerald-400 mt-1">느끼지 않으려 억누를수록 감정은 더 큰 그림자를 만듭니다.</p>
          </div>
          <div class="bg-[#172e21] border border-emerald-600/50 rounded-2xl p-5 space-y-3">
            <h4 class="font-bold text-emerald-200 text-base">🏷️ 감정에 다정하게 이름 붙이기</h4>
            <p class="text-sm text-emerald-100/90 leading-relaxed">
              이 감정이 내가 무언가 소중히 여기는 가치와 맞닿아 있음을 인정하고 너그럽게 품어주세요.
            </p>
            <div class="space-y-2 bg-[#0f241a] p-4 rounded-xl border border-emerald-700/50 text-emerald-200 text-sm">
              <p>“오늘(지금)은 <strong>[ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]</strong> 같은 감정을 느끼고 있구나.”</p>
              <p>“아, 나는 <strong>[ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]</strong>하고 싶어서 <strong>[ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ]</strong> 같이 느끼는구나.”</p>
            </div>
            <p class="text-xs text-emerald-400 leading-relaxed">
              부정적인 감정 또한 나를 보호하고 소중한 것을 알려주기 위해 찾아온 손님입니다. 내치지 말고 옆자리를 살며시 내어주세요.
            </p>
          </div>
          <button onclick="openScoreCheck()" class="w-full mt-4 bg-[#2d6144] hover:bg-[#3b7a57] text-white py-2.5 rounded-xl font-bold text-sm cursor-pointer">
            마음 점수 체크하러 가기 ➔
          </button>
        </div>
      `;
    }

    // ==========================================
    // 6. 감정 점수 체크 & 숲의 우체통 (11개 문장)
    // ==========================================
    const forestQuotes = [
      {
        text: "내 인생에서 지금 이 순간이 제일 어린 시간이니, 한번 다르게 살아보겠다는 마음가짐 말이다. 엄청 거창한 것이 아니어도 된다. (중략) ‘2회차 삶이 시작된다면 이렇게 할 텐데’를, 지금 여기서 하는 것이다.",
        source: "— 이번 생은 망한 것 같아? 2회차 인생! 『잠 못 드는 당신을 위한 밤의 심리학』"
      },
      {
        text: "마음먹은 것을 가능한 꾸준히, 그냥 하는 것이 중요하다.\n너무나 기대했던 일들이 눈앞에서 좌절되었다고 너무 오래는 슬퍼 마세요.",
        source: "— 실패로 힘들어하는 이에게"
      },
      {
        text: "‘이렇게 액땜한 거지!’ 하고 호기롭게 큰소리 한번 치고는 다시 행동을 개시하세요. 10년 후, 후회하지 않을 행동을 하세요.",
        source: "— 실패로 힘들어하는 이에게"
      },
      {
        text: "부정적 감정을 마음 안에서 제거하는 것은 불가능한 목표입니다. 그래서 부정적인 그 무엇도 느끼지 않으려 하는 것을 ‘죽은 사람의 목표’라고도 말합니다. 죽은 이가 산 자보다 더 잘할 수 있는 일은 아무것도 느끼지 않는 것이니까요. 살아있는 사람들, 그 중에도 지혜로운 사람들은 마침내 부정적인 감정을 마음 안에 모두 품어버립니다. 살아있는 내가 끌어안아 버리면 안아지는, 내 측은한 나의 기억과 감정들입니다.",
        source: "— 마음 안의 지옥을 다루는 법"
      },
      {
        text: "사라지지 않을 슬픔을 다루는 자신만의 지혜를 찾으셨다면 언젠가는 그 지혜를 저 혹은 다른 누군가에게 나누어주실 수도 있겠지요. 저도 이곳에 팁을 하나 두고 갑니다. 저는 제 마음 안 지옥에게 어른이 되어 주기로 결심했습니다. 어린 시절부터 품고 있었던 좋은 어른의 모습을 떠올려 내 안의 상실감과 슬픔을 대하고자 했습니다.",
        source: "— 마음 안의 지옥을 다루는 법"
      },
      {
        text: "사실 사람이 매일 하는 일은 비슷합니다. 우리는 자신에게 매일 하는 비판을 계속 반복해서 하고 있는지도요. 그동안 마음속에 사는 작은 아이는 얼마나 용서가 고팠을까요? 그 마음을 다정히 알아주세요.",
        source: "— 『우울은 초록의 마음』"
      },
      {
        text: "어른이 된 우리는 자신에게 \"나는 이런 사람이 되어야 한다.\"라고 너무 자주 말하고 있는지도 모릅니다. 당신은 어떤 존재가 되거나 이뤄 내지 않아도 좋습니다. 그 자체로 충분합니다. 비록 수많은 실패를 했어도 그것이 사랑받지 못할 이유는 되지 않습니다.",
        source: "— 『우울은 초록의 마음』"
      },
      {
        text: "부정적이었던 것들을 성취의 기억으로 긍정적으로 재해석하다 보면, 긍정 회로가 돌기 시작하여 사고의 흐름이 바뀔 것이고 그 흐름이 앞으로의 미래를 더욱더 발전적인 방향으로 이끌어 줄 것입니다. 그러니 '시간 관리'라는 것은 현재와 미래만 조율하는 것이 아니라 내 인생 전체를 좌지우지하는 것일 수밖에요.",
        source: "— 『마일리지 아워』"
      },
      {
        text: "그럴 때마다 나는 내가 얼마나 스스로 행복해질 수 있는 사람인지 일깨워주어야 한다. 그것은 내가 나로 살아가는 동안 마땅히 해야 할 의무이자 최소한의 도리인 것이다. 그래서 그 비장의 무기를 찾기 위해 내 삶을 즐겁고 행복하게 만드는 것들에 대해 마구잡이로 떠올려 본다.",
        source: "— 『멋있게 좀 살자 우리』"
      },
      {
        text: "좋아하는 것에 이름을 지어주는 일은 내 시간을 선물하겠다는 의미라고 생각한다. 이름을 부를 때마다 함께 하는 시간. 멀리서도 그 이름을 떠올리는 순간에 함께 있는 것 같다.",
        source: "— 『조금 더 사랑하는 쪽으로』"
      },
      {
        text: "만약 그때의 저를 만날 수 있다면 이렇게 얘기해 주고 싶어요.\n지금도 충분히 잘하고 있다고, 너는 네가 생각하는 것보다 생각이 많고 경험을 통해 배우며 잘 성장하고 있다고 말이에요. 물론 쉽지 않은 일도 많을 테고, 실패도 많이 할 거라는 얘기도 빼놓지 않을 거예요. 하지만 채찍을 내려놓고 네가 너의 가장 든든한 지원군이 되면 어떤 일이 생겨도 무너지지 않고 다시 일어날 수 있을 거라고 토닥여 주고 싶어요. 그러니 불안해하지 말라고 말이죠.",
        source: "— 『나는 나를 돌봅니다』"
      }
    ];

    function updateScoreVal(val) {
      document.getElementById('score-display').innerText = `${val}점`;
    }

    function drawRandomQuote() {
      const randIdx = Math.floor(Math.random() * forestQuotes.length);
      const q = forestQuotes[randIdx];
      document.getElementById('postbox-quote-text').innerText = q.text;
      document.getElementById('postbox-quote-source').innerText = q.source;
    }

    // 초기화
    window.addEventListener('DOMContentLoaded', () => {
      drawRandomQuote();
    });
  </script>
</body>
</html>
