<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KOSPI & KOSDAQ 라이브 브리핑 핵심 요약</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
body {
    background-color: #0F172A;
    color: #F8FAFC;
    font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
.chart-container {
    position: relative;
    width: 100%;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
    height: 350px;
    max-height: 400px;
}
@media (max-width: 768px) {
    .chart-container {
        height: 280px;
    }
}
.glass-card {
    background: rgba(30, 41, 59, 0.7);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
}
.text-gradient {
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-image: linear-gradient(to right, #06B6D4, #3B82F6, #EC4899);
}
</style>
</head>
<body class="antialiased min-h-screen pb-20">

<header class="pt-16 pb-12 px-6 text-center border-b border-slate-700 glass-card sticky top-0 z-50">
    <div class="max-w-5xl mx-auto">
        <div class="inline-block bg-blue-600 text-white text-xs font-bold px-3 py-1 rounded-full mb-4 animate-pulse">LIVE BROADCAST RECAP</div>
        <h1 class="text-4xl md:text-6xl font-extrabold mb-4 tracking-tight text-gradient">대한민국 증시 긴급 진단</h1>
        <p class="text-lg md:text-xl text-slate-300 max-w-2xl mx-auto">코스피 3,000 돌파 시나리오 및 코스닥 주도주(AI/반도체/바이오) 순환매 핵심 요약 보고서</p>
    </div>
</header>

<main class="max-w-6xl mx-auto px-6 mt-12 space-y-16">

    <section>
        <div class="mb-8">
            <h2 class="text-2xl md:text-3xl font-bold flex items-center text-white"><span class="text-cyan-400 mr-3">📊</span> 1. 양대 시장 핵심 지표 및 전망</h2>
            <p class="text-slate-400 mt-2 leading-relaxed">외국인 자금의 지속적인 유입과 기업 밸류업 프로그램의 성과가 맞물리며 코스피의 하방 지지력이 강력해졌습니다. 매크로 환경(금리 인하 기대감)이 우호적으로 전환됨에 따라 유동성 장세가 예고됩니다.</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="glass-card p-6 rounded-2xl shadow-xl text-center transform hover:scale-105 transition-transform">
                <p class="text-slate-400 text-sm font-semibold tracking-wider">KOSPI 단기 목표치</p>
                <div class="text-5xl font-black text-cyan-400 mt-2 mb-1">3,150.00</div>
                <p class="text-emerald-400 font-medium">+12.4% 상승 여력</p>
            </div>
            <div class="glass-card p-6 rounded-2xl shadow-xl text-center transform hover:scale-105 transition-transform">
                <p class="text-slate-400 text-sm font-semibold tracking-wider">KOSDAQ 단기 목표치</p>
                <div class="text-5xl font-black text-pink-400 mt-2 mb-1">980.50</div>
                <p class="text-emerald-400 font-medium">+15.2% 상승 여력</p>
            </div>
            <div class="glass-card p-6 rounded-2xl shadow-xl text-center transform hover:scale-105 transition-transform">
                <p class="text-slate-400 text-sm font-semibold tracking-wider">외국인 누적 순매수 (연초대비)</p>
                <div class="text-5xl font-black text-blue-400 mt-2 mb-1">21.5조</div>
                <p class="text-slate-300 font-medium">반도체/자동차 섹터 집중</p>
            </div>
        </div>
    </section>

    <section class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div>
            <h2 class="text-2xl md:text-3xl font-bold flex items-center text-white mb-4"><span class="text-pink-400 mr-3">🔥</span> 2. 핵심 주도 섹터 성장률 비교</h2>
            <p class="text-slate-400 leading-relaxed mb-6">현재 증시를 이끄는 쌍두마차는 단연 'AI 반도체(HBM)'와 'K-뷰티/바이오'입니다. 기존 주도주였던 이차전지는 캐즘(Chasm) 우려로 성장세가 다소 둔화되었으나, 저PBR 관련주(금융/지주)는 배당 확대 및 자사주 소각 기대로 꾸준한 수급이 유입되고 있습니다. 포트폴리오 비중 확대가 필요한 섹터를 명확히 구분해야 합니다.</p>
            <div class="flex flex-wrap gap-2">
                <span class="bg-slate-800 text-cyan-300 px-3 py-1 rounded border border-cyan-800 text-sm">Overweight: 반도체</span>
                <span class="bg-slate-800 text-pink-300 px-3 py-1 rounded border border-pink-800 text-sm">Overweight: 전력기기</span>
                <span class="bg-slate-800 text-slate-300 px-3 py-1 rounded border border-slate-600 text-sm">Neutral: 자동차</span>
            </div>
        </div>
        <div class="glass-card p-6 rounded-2xl shadow-xl">
            <div class="chart-container">
                <canvas id="sectorChart"></canvas>
            </div>
        </div>
    </section>

    <section class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="glass-card p-6 rounded-2xl shadow-xl order-2 lg:order-1">
            <div class="chart-container">
                <canvas id="demandChart"></canvas>
            </div>
        </div>
        <div class="order-1 lg:order-2">
            <h2 class="text-2xl md:text-3xl font-bold flex items-center text-white mb-4"><span class="text-blue-400 mr-3">📈</span> 3. 주체별 수급 동향 (스마트 머니의 이동)</h2>
            <p class="text-slate-400 leading-relaxed mb-6">개인 투자자들의 매도세가 이어지는 반면, 외국인과 연기금을 필두로 한 기관 투자자들은 지속적으로 물량을 매집하고 있습니다. 특히 환율이 1,350원 이하로 안정화되는 구간에서 외국인의 패시브 자금 유입이 가파르게 나타나는 'Buy Korea' 현상이 뚜렷합니다. 수급의 주체와 방향성이 일치하는 종목에 집중해야 할 시점입니다.</p>
        </div>
    </section>

    <section>
        <div class="mb-8 text-center">
            <h2 class="text-2xl md:text-3xl font-bold flex items-center justify-center text-white"><span class="text-emerald-400 mr-3">💰</span> 4. 전문가 제시 최적의 모델 포트폴리오</h2>
            <p class="text-slate-400 mt-2 leading-relaxed max-w-3xl mx-auto">라이브 방송에서 강조된 하반기 대비 최적의 자산 배분 비중입니다. 지수 상승을 견인할 대형 IT주를 코어 자산으로 가져가면서, 금리 인하 수혜를 볼 수 있는 바이오와 실적 호조가 지속되는 방산/조선주를 위성 자산으로 배치하는 전략을 권장합니다.</p>
        </div>
        <div class="glass-card p-8 rounded-2xl shadow-xl max-w-3xl mx-auto">
            <div class="chart-container h-[400px] max-h-[500px]">
                <canvas id="portfolioChart"></canvas>
            </div>
        </div>
    </section>

    <section class="glass-card p-8 rounded-2xl shadow-xl border-l-4 border-cyan-500">
        <h3 class="text-xl font-bold text-white mb-4">💡 라이브 방송 핵심 요약 결론 (Action Plan)</h3>
        <ul class="space-y-4 text-slate-300">
            <li class="flex items-start">
                <span class="text-cyan-400 mr-2 mt-1">✔</span>
                <p><strong class="text-white">반도체는 쉴 때 모아라:</strong> HBM 공급 부족 현상은 2026년 말까지 지속될 전망. 조정 시 비중 확대 전략 유효.</p>
            </li>
            <li class="flex items-start">
                <span class="text-cyan-400 mr-2 mt-1">✔</span>
                <p><strong class="text-white">밸류업은 배신하지 않는다:</strong> 정부의 밸류업 세제지원안 통과 기대감. 금융주 및 저PBR 지주사의 하방 경직성 확보.</p>
            </li>
            <li class="flex items-start">
                <span class="text-cyan-400 mr-2 mt-1">✔</span>
                <p><strong class="text-white">금리 인하의 최대 수혜주 찾기:</strong> 연준(Fed)의 금리 인하 사이클 진입 시 바이오 제약 및 헬스케어 섹터의 폭발적 랠리 가능성 대비.</p>
            </li>
        </ul>
    </section>

</main>

<footer class="text-center text-slate-500 py-8 mt-12 text-sm border-t border-slate-800">
    <p>본 인포그래픽은 전문가 라이브 방송 내용을 기반으로 재구성되었으며, 투자 결과에 대한 법적 책임 소재의 증빙자료로 사용될 수 없습니다.</p>
</footer>

<script>
const wrapText = (text) => {
    if (text.length <= 16) return text;
    const words = text.split(' ');
    const lines = [];
    let currentLine = '';
    for (let i = 0; i < words.length; i++) {
        if ((currentLine + words[i]).length > 16) {
            lines.push(currentLine.trim());
            currentLine = words[i] + ' ';
        } else {
            currentLine += words[i] + ' ';
        }
    }
    if (currentLine) {
        lines.push(currentLine.trim());
    }
    return lines;
};

const commonTooltip = {
    tooltip: {
        backgroundColor: 'rgba(15, 23, 42, 0.9)',
        titleFont: { size: 14, family: 'Pretendard' },
        bodyFont: { size: 13, family: 'Pretendard' },
        padding: 12,
        borderColor: 'rgba(6, 182, 212, 0.3)',
        borderWidth: 1,
        callbacks: {
            title: function(tooltipItems) {
                const item = tooltipItems[0];
                let label = item.chart.data.labels[item.dataIndex];
                if (Array.isArray(label)) {
                    return label.join(' ');
                } else {
                    return label;
                }
            }
        }
    },
    legend: {
        labels: {
            color: '#CBD5E1',
            font: { family: 'Pretendard', size: 12 }
        }
    }
};

Chart.defaults.color = '#94A3B8';
Chart.defaults.font.family = 'Pretendard';

const ctxSector = document.getElementById('sectorChart').getContext('2d');
const rawSectorLabels = [
    "AI 반도체 및 HBM 장비",
    "초고압 전력기기 및 전선",
    "저PBR 밸류업 (금융/지주)",
    "K-뷰티 및 화장품 수출",
    "이차전지 (소재/셀)",
    "플랫폼 및 인터넷 게임"
];
const sectorLabels = rawSectorLabels.map(wrapText);

new Chart(ctxSector, {
    type: 'bar',
    data: {
        labels: sectorLabels,
        datasets: [{
            label: '2026년 예상 영업이익 증가율 (%)',
            data: [85, 62, 25, 45, -15, 10],
            backgroundColor: [
                'rgba(6, 182, 212, 0.8)',
                'rgba(59, 130, 246, 0.8)',
                'rgba(139, 92, 246, 0.8)',
                'rgba(236, 72, 153, 0.8)',
                'rgba(100, 116, 139, 0.5)',
                'rgba(16, 185, 129, 0.8)'
            ],
            borderRadius: 6
        }]
    },
    options: {
        maintainAspectRatio: false,
        indexAxis: 'y',
        plugins: { ...commonTooltip },
        scales: {
            x: { grid: { color: 'rgba(255,255,255,0.05)' } },
            y: { grid: { display: false } }
        }
    }
});

const ctxDemand = document.getElementById('demandChart').getContext('2d');
const rawDemandLabels = ["1월", "2월", "3월", "4월", "5월", "6월", "7월", "8월", "9월", "10월"];
const demandLabels = rawDemandLabels.map(wrapText);

new Chart(ctxDemand, {
    type: 'line',
    data: {
        labels: demandLabels,
        datasets: [
            {
                label: '외국인 누적 순매수 (조 원)',
                data: [2, 5, 8, 7, 12, 15, 14, 18, 20, 21.5],
                borderColor: '#06B6D4',
                backgroundColor: 'rgba(6, 182, 212, 0.1)',
                borderWidth: 3,
                tension: 0.4,
                fill: true,
                pointBackgroundColor: '#06B6D4'
            },
            {
                label: '개인 누적 순매수 (조 원)',
                data: [-1, -3, -4, -2, -6, -8, -10, -12, -15, -16],
                borderColor: '#EC4899',
                borderWidth: 2,
                borderDash: [5, 5],
                tension: 0.4,
                pointBackgroundColor: '#EC4899'
            }
        ]
    },
    options: {
        maintainAspectRatio: false,
        plugins: { ...commonTooltip },
        scales: {
            y: { grid: { color: 'rgba(255,255,255,0.05)' } },
            x: { grid: { display: false } }
        },
        interaction: {
            mode: 'index',
            intersect: false,
        }
    }
});

const ctxPortfolio = document.getElementById('portfolioChart').getContext('2d');
const rawPortLabels = [
    "핵심주: IT/반도체 (대형주 중심)",
    "성장주: K-뷰티/바이오 제약",
    "방어주: 금융/지주사 (고배당)",
    "모멘텀: 우주항공/K-방산",
    "현금 및 단기 채권"
];
const portLabels = rawPortLabels.map(wrapText);

new Chart(ctxPortfolio, {
    type: 'doughnut',
    data: {
        labels: portLabels,
        datasets: [{
            data: [40, 20, 15, 15, 10],
            backgroundColor: [
                '#3B82F6',
                '#EC4899',
                '#8B5CF6',
                '#06B6D4',
                '#475569'
            ],
            borderWidth: 0,
            hoverOffset: 10
        }]
    },
    options: {
        maintainAspectRatio: false,
        cutout: '65%',
        plugins: {
            ...commonTooltip,
            legend: {
                position: 'right',
                labels: {
                    color: '#CBD5E1',
                    font: { family: 'Pretendard', size: 13 },
                    padding: 20
                }
            }
        }
    }
});
</script>
</body>
</html>
