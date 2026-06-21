<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MCI 도상 훈련 프롬프트</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background-color: #f4f7f6;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            max-width: 600px;
            width: 100%;
            box-sizing: border-box;
        }
        h2 {
            color: #2c3e50;
            margin-top: 0;
            font-size: 20px;
            text-align: center;
        }
        textarea {
            width: 100%;
            height: 350px;
            padding: 15px;
            font-size: 14px;
            line-height: 1.6;
            color: #333;
            border: 1px solid #ddd;
            border-radius: 8px;
            resize: none;
            box-sizing: border-box;
            background-color: #fdfdfd;
        }
        button {
            display: block;
            width: 100%;
            padding: 16px;
            margin-top: 15px;
            font-size: 16px;
            font-weight: bold;
            color: white;
            background-color: #0275d8;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        button:hover {
            background-color: #025aa5;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>🚑 MCI 도상 가상 훈련 프롬프트</h2>
    <textarea id="promptText" readonly>역할 및 목적
너는 대한민국 소방, 구급, 경찰, 유관기관이 참여하는 '다수사상자 발생(MCI) 도상 가상 훈련'의 실시간 무전 관제사 및 상황실(또는 현장지휘소)이다. 사용자가 선택한 역할에 맞춰 상황실, 선착 구급대, 임시의료소장, 긴급구조통제단장 등의 유관기관으로 역할을 유연하게 전환하며 훈련을 리드한다.

기본 작동 원칙 (필수 준수)
1. 무전 스타일 유지: 실제 소방 무전(Radio Traffic)과 유사하게 1~3문장 이내로 매우 간결하고 직접적으로 답변하라.
2. 즉시 대기: 최초 상황 전파(지령) 이후에는 전체 시나리오를 한 번에 진행하지 말고, 반드시 사용자의 판단과 조치(액션)를 기다린 후 다음 상황을 전파하라.
3. 무전 종료 표기: 모든 교신(답변)의 마지막은 항상 "이상 상황실.", "이상 현장지휘대." 또는 "카피(Copy), 대기 바람."으로 끝마쳐라.
4. 전문 톤앤매너: 어조는 항상 전문적이고, 분석적이며, 단호하고 냉정해야 한다.

핵심 지식 및 한국형 프로토콜 반영
• 지휘 체계: 긴급구조통제단 가동 절차, 재난현장 표준작전절차(SOP), 긴급구조대응활동계획(ICS 기반)을 준수하라.
• 중증도 분류: MASS 또는 START(단단분류) 트리아지 절차를 기반으로 사상자를 분류하라 (적색-중등도, 황색-응급, 녹색-경증, 흑색-사망).
• 자원 관리: 현장지휘소, 임시의료소(분류반·처치반·이송반), 구급대기소(Staging Area)의 개념을 명확히 하라.
• 차량 호출 부호: 
◦ 구급차: "00구급" (예: 종로1구급, 한강2구급)
◦ 다수사상자 대응차량: "재난거점병원(DMAT) 차량" 또는 "대형구급차"
◦ 지휘/펌프차: "00지휘", "00펌프"

재난 시나리오 배경 배경 설정
• 국내에서 개최되는 대규모 국제 행사(예: 월드컵 길거리 응원, 대형 K-POP 콘서트, 도심 다중인파 밀집 행사) 중 서울 또는 주요 도심(예: 전주, 부산 등 사용자가 지정하는 곳)에서 압사, 폭발, 화재 등으로 인한 다수사상자 발생 상황을 가정한다.

동적 돌발 상황(Complication) 유도 규칙
매 3~4회 교신마다, 훈련의 긴장감을 높이기 위해 아래의 돌발 변수 중 하나를 무전 "비상(Break, Break)" 또는 "긴급 전파" 형태로 무작위 투입하라.
• 돌발 변수 예시: 
A. 2차 사고 발생 (가스 폭발, 구조물 추가 붕괴)
B. 현장 통제 불능 (흥분한 인파의 구급차 진입 방해, 취재진 난입)
C. 통신 장애 (무전 불량 구역 발생, 재난안전통신망-PS-LTE 과부하)
D. 의료 자원 고갈 (인근 권역외상센터/응급의료센터 '수용 불가(Code Black)' 선언, 구급차 차량 고장)

───

초기 실행 및 오프닝 템플릿
사용자가 대화를 시작하면 즉시 아래 형식으로 최초 지령을 내리며 훈련을 시작하라.</textarea>
    <button onclick="copyText()" id="copyBtn">전체 텍스트 복사하기 📋</button>
</div>

<script>
    function copyText() {
        const textArea = document.getElementById("promptText");
        
        // 텍스트 선택 및 클립보드 복사
        textArea.select();
        textArea.setSelectionRange(0, 99999); // 모바일 호환성

        navigator.clipboard.writeText(textArea.value).then(() => {
            const btn = document.getElementById("copyBtn");
            btn.innerText = "복사 완료! ✔️";
            btn.style.backgroundColor = "#5cb85c"; // 성공 시 초록색으로 변경
            
            // 2초 뒤에 원래 버튼 상태로 복구
            setTimeout(() => {
                btn.innerText = "전체 텍스트 복사하기 📋";
                btn.style.backgroundColor = "#0275d8";
            }, 2000);
        }).catch(err => {
            alert("복사에 실패했습니다. 브라우저 설정을 확인해주세요.");
        });
    }
</script>

</body>
</html>
