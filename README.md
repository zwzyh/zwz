<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>宸风优选货源站防失联引导页</title>
    <link rel="icon" href="about:blank">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        ::selection {
            background: rgba(255,255,255,0.2);
            color: #fff;
        }

        :root {
            --color-primary: #1a73e8;
            --color-primary-dark: #0066cc;
            --color-gradient-start: #0f4c81;
            --color-gradient-end: #1a73e8;
            --color-warning: #ffcc00;
            --radius: 12px;
            --transition: all 0.2s ease;
        }

        html, body {
            height: 100%;
        }

        body {
            background: linear-gradient(135deg, var(--color-gradient-start), var(--color-gradient-end));
            color: #fff;
            padding: 20px;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            min-height: 100vh;
            line-height: 1.6;
            user-select: none;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            font-weight: 400;
            animation: pageFadeIn 0.5s ease forwards;
        }

        @keyframes pageFadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .tip {
            background: #ffcc00;
            color: #222;
            padding: 12px;
            border-radius: 10px;
            text-align: center;
            font-weight: bold;
            margin-bottom: 24px;
            font-size: 15px;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
            padding: 20px 0;
        }

        .header {
            margin-bottom: 36px;
        }

        .header h1 {
            font-size: clamp(24px, 5vw, 32px);
            margin-bottom: 12px;
            font-weight: 600;
        }

        .header p {
            font-size: clamp(15px, 3vw, 17px);
            opacity: 0.92;
            line-height: 1.7;
        }

        .btn-group {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .btn {
            background: var(--color-primary);
            color: white;
            border: none;
            padding: 17px 20px;
            font-size: clamp(16px, 3.5vw, 18px);
            border-radius: var(--radius);
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            font-weight: 500;
            box-shadow: 0 3px 8px rgba(0,0,0,0.1);
            outline: none;
            min-height: 56px;
        }

        .btn:hover {
            background: var(--color-primary-dark);
        }

        .btn:active {
            transform: scale(0.97);
        }

        .btn.copy {
            background: #00c851;
            cursor: pointer;
        }

        .footer-banner {
            margin-top: 44px;
            background: var(--color-warning);
            color: #222;
            padding: 20px;
            border-radius: var(--radius);
        }

        .footer-banner .title {
            font-weight: bold;
            font-size: clamp(16px, 3.5vw, 19px);
            margin-bottom: 14px;
        }

        .enter-btn {
            display: inline-block;
            background: var(--color-primary-dark);
            color: white;
            padding: 12px 26px;
            font-size: 16px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            outline: none;
        }

        .enter-btn:hover {
            background: #005bb5;
        }

        .copy-tip {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: #00c851;
            color: #fff;
            padding: 9px 18px;
            border-radius: 6px;
            font-size: 14px;
            opacity: 0;
            pointer-events: none;
            transition: 0.3s;
        }
        .copy-tip.show {
            opacity: 1;
            top: 30px;
        }

        .copyright {
            margin-top: 20px;
            font-size: 12px;
            opacity: 0.6;
            text-align: center;
        }
    </style>
</head>

<body>
    <div class="copy-tip" id="copyTip">复制成功！请收藏防失联</div>

    <div class="container">
        <div class="tip">⚠️ 宸风优选 · 请收藏本页，防止找不到主站 ⚠️</div>

        <div class="header">
            <h1>宸风优选货源站防失联引导页</h1>
            <p>优质严选低价货源平台<br>24小时真人客服在线处理卡密问题</p >
        </div>

        <div class="btn-group">
            ☁ 备用线路一
            
            
            
            
            
            <div class="btn copy" id="copyBtn">📋 复制本页防失联链接</div>
        </div>

        <div class="footer-banner">
            <div class="title">宸风优选 · 咱老百姓自己的货源站</div>
            
        </div>

        <div class="copyright">© 2026 宸风优选 版权所有</div>
    </div>

    <script>
        const copyTip = document.getElementById('copyTip');
        document.getElementById('copyBtn').onclick = async () => {
            try {
                await navigator.clipboard.writeText("https://这里改成你自己的防失联网址.com");
                copyTip.classList.add('show');
                setTimeout(() => copyTip.classList.remove('show'), 1600);
            } catch (e) {
                alert("复制失败，请手动复制地址");
            }
        };
    </script>
</body>
</html>
