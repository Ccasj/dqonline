[Uploading index.html.txt…]()
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>地球Online | 少女科技风</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&family=Orbitron:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Noto Sans SC', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f9e6ff, #ffd1f3, #e6ccff);
            color: #5a3a7a;
            min-height: 100vh;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        /* 粒子背景 */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            pointer-events: none;
        }
        
        .particle {
            position: absolute;
            background-color: rgba(200, 150, 255, 0.6);
            border-radius: 50%;
            animation: float linear infinite;
        }
        
        @keyframes float {
            to {
                transform: translateY(100vh);
            }
        }
        
        /* 霓虹线条装饰 */
        .neon-line {
            position: absolute;
            height: 1px;
            background: linear-gradient(90deg, transparent, #d88cff, transparent);
            box-shadow: 0 0 5px #d88cff, 0 0 10px #d88cff;
        }
        
        .container {
            position: relative;
            z-index: 2;
            text-align: center;
            width: 100%;
            max-width: 1200px;
            min-height: 90vh;
            padding: 20px;
            background: rgba(255, 245, 250, 0.85);
            border-radius: 25px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(180, 100, 220, 0.2);
            border: 1px solid rgba(230, 180, 255, 0.4);
            display: flex;
            flex-direction: column;
        }
        
        /* 右上角昵称 */
        .user-nickname {
            position: absolute;
            top: 20px;
            right: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(255, 255, 255, 0.7);
            padding: 8px 15px;
            border-radius: 50px;
            backdrop-filter: blur(5px);
            box-shadow: 0 4px 15px rgba(180, 100, 220, 0.15);
            z-index: 10;
        }
        
        .user-nickname input {
            background: transparent;
            border: none;
            color: #8a4bcf;
            font-weight: 500;
            font-size: 1.1rem;
            outline: none;
            width: 150px;
            text-align: center;
            font-family: 'Orbitron', sans-serif;
            border-bottom: 2px dashed #d88cff;
        }
        
        .user-nickname i {
            color: #d88cff;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .user-nickname i:hover {
            transform: scale(1.2);
        }
        
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.2rem;
            margin-bottom: 10px;
            color: #8a4bcf;
            font-weight: 500;
            letter-spacing: 2px;
            text-shadow: 0 0 10px rgba(216, 140, 255, 0.3);
            position: relative;
            display: inline-block;
        }
        
        h1::after {
            content: "";
            position: absolute;
            bottom: -8px;
            left: 10%;
            width: 80%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #d88cff, transparent);
        }
        
        p {
            font-size: 1rem;
            margin-bottom: 15px;
            line-height: 1.6;
            color: #7a5a9a;
            font-weight: 400;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(135deg, #d88cff, #b56cdf);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 0 15px rgba(216, 140, 255, 0.4);
            position: relative;
            overflow: hidden;
            margin: 8px;
            font-weight: 500;
            letter-spacing: 1px;
            font-family: 'Orbitron', sans-serif;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 25px rgba(216, 140, 255, 0.6);
        }
        
        .btn:active {
            transform: translateY(1px);
        }
        
        .btn::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255,255,255,0.3), rgba(255,255,255,0));
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .btn:hover::after {
            opacity: 1;
        }
        
        .earth {
            width: 80px;
            height: 80px;
            margin: 0 auto 15px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="45" fill="none" stroke="%23d88cff" stroke-width="2" stroke-dasharray="4 2"/><path d="M50,5 A45,45 0 1,1 50,95 A45,45 0 1,1 50,5 Z" fill="none" stroke="%23ffffff" stroke-width="1" opacity="0.7"/><circle cx="50" cy="50" r="40" fill="%23f9e6ff" stroke="%23b56cdf" stroke-width="1"/><path d="M30,35 Q45,25 60,35 T90,45" stroke="%23e080d0" stroke-width="1" fill="none"/><path d="M25,60 Q35,50 50,55 T75,65" stroke="%23e080d0" stroke-width="1" fill="none"/></svg>') no-repeat center;
            background-size: contain;
            animation: rotate 20s linear infinite;
            filter: drop-shadow(0 0 10px rgba(216, 140, 255, 0.4));
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        .screen {
            display: none;
            flex: 1;
            overflow: hidden;
        }
        
        .screen.active {
            display: flex;
            flex-direction: column;
            animation: fadeIn 0.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* 模式选择区域 - 左右划分 */
        .mode-container {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            margin: 20px 0;
            flex-wrap: wrap;
            flex: 1;
            overflow: hidden;
        }
        
        .mode {
            flex: 1;
            min-width: 300px;
            background: rgba(255, 240, 245, 0.8);
            border-radius: 20px;
            padding: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(180, 100, 220, 0.15);
            border: 1px solid rgba(230, 180, 255, 0.5);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }
        
        .mode::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #d88cff, #ffaae0);
        }
        
        .mode:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(216, 140, 255, 0.2);
            border-color: rgba(216, 140, 255, 0.6);
        }
        
        .mode h3 {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            margin-bottom: 15px;
            font-size: 1.5rem;
            font-weight: 500;
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3);
        }
        
        .mode .percentage {
            font-family: 'Orbitron', sans-serif;
            font-size: 2rem;
            margin-bottom: 10px;
            color: #ffaae0;
            text-shadow: 0 0 10px rgba(255, 170, 224, 0.3);
        }
        
        .mode ul {
            text-align: left;
            margin: 15px 0;
            padding-left: 15px;
            list-style-type: none;
            flex: 1;
        }
        
        .mode li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 25px;
            color: #7a5a9a;
            font-size: 0.95rem;
        }
        
        .mode li:before {
            content: "›";
            color: #d88cff;
            font-size: 1.5rem;
            position: absolute;
            left: 0;
            top: -5px;
        }
        
        .mode-btn {
            margin-top: 15px;
            padding: 10px 25px;
            font-size: 0.9rem;
        }
        
        /* 加载界面 */
        .loading-screen {
            text-align: center;
            padding: 30px 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100%;
        }
        
        .loading-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: #ffaae0;
            text-shadow: 0 0 10px rgba(255, 170, 224, 0.3);
        }
        
        .loading-text {
            font-size: 1.1rem;
            margin-bottom: 30px;
            color: #8a6aaf;
        }
        
        .progress-container {
            width: 100%;
            max-width: 400px;
            margin: 0 auto 30px;
            background: rgba(255, 240, 245, 0.8);
            border-radius: 10px;
            height: 15px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #b56cdf, #d88cff, #ffaae0);
            width: 0;
            transition: width 0.3s ease;
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }
        
        .progress-bar::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, 
                transparent, 
                rgba(255, 255, 255, 0.3), 
                transparent);
            animation: progressGlow 2s infinite;
        }
        
        @keyframes progressGlow {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        .progress-text {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.2rem;
            color: #d88cff;
            margin-top: 10px;
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3);
        }
        
        .loading-dots {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 8px;
        }
        
        .dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: #d88cff;
            animation: pulse 1.5s infinite ease-in-out;
        }
        
        .dot:nth-child(1) { animation-delay: 0s; }
        .dot:nth-child(2) { animation-delay: 0.3s; }
        .dot:nth-child(3) { animation-delay: 0.6s; }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.7; }
            50% { transform: scale(1.3); opacity: 1; }
        }
        
        /* 主界面 */
        .dashboard {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            gap: 15px;
            height: calc(100% - 70px);
            margin-top: 10px;
        }
        
        .module {
            background: rgba(255, 245, 250, 0.85);
            border-radius: 20px;
            padding: 15px;
            box-shadow: 0 5px 20px rgba(180, 100, 220, 0.15);
            border: 1px solid rgba(230, 180, 255, 0.5);
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            text-align: left;
            display: flex;
            flex-direction: column;
            min-height: 280px;
        }
        
        .module:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(216, 140, 255, 0.2);
            border-color: rgba(216, 140, 255, 0.6);
        }
        
        .module::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #d88cff, #ffaae0);
        }
        
        .module h3 {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            margin-bottom: 10px;
            font-size: 1.4rem;
            font-weight: 500;
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .module h3 i {
            color: #ffaae0;
        }
        
        .module-content {
            flex: 1;
            overflow: hidden;
            font-size: 0.9rem;
            display: flex;
            flex-direction: column;
        }
        
        .module.editable {
            background: rgba(255, 245, 250, 0.9);
            border: 2px dashed rgba(216, 140, 255, 0.5);
        }
        
        /* 地球online游戏攻略 */
        .guide-section {
            display: flex;
            flex-direction: column;
            gap: 10px;
            height: 100%;
            overflow-y: auto;
            padding-right: 5px;
        }
        
        .guide-item {
            background: rgba(255, 240, 245, 0.8);
            padding: 12px;
            border-radius: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s;
            border: 1px solid rgba(230, 180, 255, 0.4);
        }
        
        .guide-item:hover {
            background: rgba(255, 230, 240, 0.9);
        }
        
        .guide-text {
            font-size: 0.95rem;
            color: #7a5a9a;
            flex: 1;
        }
        
        .interaction {
            display: flex;
            gap: 8px;
        }
        
        .like-btn, .tip-btn, .delete-btn {
            padding: 6px 12px;
            border-radius: 20px;
            background: rgba(216, 140, 255, 0.2);
            color: #8a4bcf;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.85rem;
            transition: all 0.3s;
        }
        
        .like-btn:hover, .tip-btn:hover, .delete-btn:hover {
            background: rgba(216, 140, 255, 0.4);
        }
        
        .delete-btn {
            background: rgba(255, 100, 100, 0.2);
        }
        
        .delete-btn:hover {
            background: rgba(255, 100, 100, 0.4);
        }
        
        /* 文章弹窗 */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background: rgba(255, 245, 250, 0.95);
            border-radius: 25px;
            padding: 25px;
            width: 90%;
            max-width: 700px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 0 30px rgba(216, 140, 255, 0.4);
            border: 2px solid #d88cff;
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            color: #ffaae0;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .close-modal:hover {
            transform: rotate(90deg);
            color: #d88cff;
        }
        
        .modal-title {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            margin-bottom: 15px;
            font-size: 1.5rem;
            text-align: center;
        }
        
        .modal-body {
            font-size: 1rem;
            line-height: 1.7;
            color: #7a5a9a;
            margin-bottom: 20px;
            padding: 15px;
            background: rgba(255, 240, 245, 0.8);
            border-radius: 15px;
            border: 1px solid rgba(230, 180, 255, 0.4);
        }
        
        .interaction-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .tip-options {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-top: 15px;
        }
        
        .tip-option {
            padding: 8px 15px;
            background: rgba(216, 140, 255, 0.2);
            border-radius: 20px;
            border: none;
            color: #8a4bcf;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .tip-option:hover {
            background: rgba(216, 140, 255, 0.4);
        }
        
        /* 打赏成功提示 */
        .tip-success {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 245, 250, 0.95);
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 0 30px rgba(216, 140, 255, 0.5);
            border: 2px solid #d88cff;
            text-align: center;
            z-index: 2000;
            display: none;
            max-width: 450px;
            width: 90%;
            animation: tipSuccess 1s ease-out;
        }
        
        @keyframes tipSuccess {
            0% { transform: translate(-50%, -50%) scale(0.5); opacity: 0; }
            70% { transform: translate(-50%, -50%) scale(1.1); opacity: 1; }
            100% { transform: translate(-50%, -50%) scale(1); }
        }
        
        .tip-success h3 {
            color: #8a4bcf;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .tip-success p {
            color: #7a5a9a;
            font-size: 1.1rem;
            margin-bottom: 15px;
            line-height: 1.6;
        }
        
        /* 身份卡 */
        .card-sections {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            gap: 12px;
            height: 100%;
        }
        
        .card-section {
            background: rgba(255, 240, 245, 0.8);
            padding: 12px;
            border-radius: 12px;
            border: 1px solid rgba(230, 180, 255, 0.4);
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            display: flex;
            flex-direction: column;
        }
        
        .card-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(216, 140, 255, 0.2);
        }
        
        .card-section h4 {
            color: #d88cff;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 1.1rem;
        }
        
        .card-list {
            list-style: none;
            font-size: 0.9rem;
            flex: 1;
        }
        
        .card-list li {
            margin-bottom: 6px;
            padding-left: 20px;
            position: relative;
            color: #7a5a9a;
        }
        
        .card-list li::before {
            content: "•";
            position: absolute;
            left: 8px;
            color: #d88cff;
        }
        
        .image-preview {
            width: 100%;
            height: 80px;
            border-radius: 10px;
            background: rgba(255, 240, 245, 0.9);
            border: 1px solid rgba(230, 180, 255, 0.5);
            margin-top: 8px;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        
        .image-preview img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .upload-btn {
            position: absolute;
            bottom: 8px;
            right: 8px;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: rgba(216, 140, 255, 0.3);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #8a4bcf;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .upload-btn:hover {
            background: rgba(216, 140, 255, 0.5);
            transform: scale(1.1);
        }
        
        /* 外貌弹窗 */
        .appearance-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .appearance-content {
            background: rgba(255, 245, 250, 0.95);
            border-radius: 25px;
            padding: 30px;
            width: 90%;
            max-width: 900px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 0 30px rgba(216, 140, 255, 0.4);
            border: 2px solid #d88cff;
        }
        
        .appearance-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px dashed #d88cff;
        }
        
        .appearance-title {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            font-size: 1.8rem;
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3);
        }
        
        .appearance-body {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .appearance-images {
            flex: 1;
            min-width: 300px;
        }
        
        .image-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }
        
        .appearance-image {
            width: 100%;
            height: 200px; /* 增大图片区域 */
            border-radius: 15px;
            background: rgba(255, 240, 245, 0.8);
            border: 1px solid rgba(230, 180, 255, 0.4);
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }
        
        .appearance-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .appearance-image h3 {
            position: absolute;
            color: white;
            text-shadow: 0 0 5px rgba(0, 0, 0, 0.7);
        }
        
        /* 显化日记 */
        .diary-container {
            height: 100%;
            overflow-y: auto;
            padding-right: 8px;
            flex: 1;
        }
        
        .diary-entry {
            background: rgba(255, 240, 245, 0.8);
            padding: 10px;
            border-radius: 12px;
            margin-bottom: 10px;
            border: 1px solid rgba(230, 180, 255, 0.4);
        }
        
        .diary-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 6px;
            color: #d88cff;
            font-size: 0.8rem;
        }
        
        .diary-content {
            color: #7a5a9a;
            line-height: 1.4;
            font-size: 0.9rem;
        }
        
        .add-diary {
            margin-top: 15px;
        }
        
        .diary-input {
            width: 100%;
            padding: 12px;
            border-radius: 12px;
            background: rgba(255, 240, 245, 0.8);
            border: 1px solid rgba(230, 180, 255, 0.5);
            color: #7a5a9a;
            margin-bottom: 10px;
            resize: vertical;
            min-height: 60px;
            font-size: 0.9rem;
        }
        
        /* 爱世界 */
        .bubble-world {
            position: relative;
            height: 100%;
            overflow: hidden;
            border-radius: 15px;
            background: rgba(255, 240, 245, 0.8);
            border: 1px solid rgba(230, 180, 255, 0.4);
            flex: 1;
        }
        
        .bubble {
            position: absolute;
            background: rgba(216, 140, 255, 0.2);
            border: 1px solid rgba(255, 170, 224, 0.4);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px;
            text-align: center;
            font-size: 0.8rem;
            color: #7a5a9a;
            animation: floatBubble linear infinite;
            cursor: pointer;
            transition: all 0.3s;
            backdrop-filter: blur(2px);
            overflow: hidden;
        }
        
        .bubble:hover {
            background: rgba(216, 140, 255, 0.3);
            transform: scale(1.05);
            box-shadow: 0 0 15px rgba(216, 140, 255, 0.4);
        }
        
        @keyframes floatBubble {
            0%, 100% { transform: translate(0, 0); }
            25% { transform: translate(5px, -5px); }
            50% { transform: translate(0, 5px); }
            75% { transform: translate(-5px, 0); }
        }
        
        .add-bubble-btn {
            position: absolute;
            bottom: 15px;
            right: 15px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, #d88cff, #ffaae0);
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
            box-shadow: 0 0 15px rgba(216, 140, 255, 0.4);
            z-index: 10;
        }
        
        .bubble-form {
            position: absolute;
            bottom: 65px;
            right: 15px;
            background: rgba(255, 245, 250, 0.95);
            padding: 15px;
            border-radius: 15px;
            width: 250px;
            z-index: 20;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            border: 1px solid rgba(230, 180, 255, 0.5);
            display: none;
        }
        
        .bubble-input {
            width: 100%;
            padding: 12px;
            border-radius: 12px;
            background: rgba(255, 240, 245, 0.8);
            border: 1px solid rgba(230, 180, 255, 0.5);
            color: #7a5a9a;
            margin-bottom: 12px;
            resize: vertical;
            min-height: 80px;
            font-size: 0.9rem;
        }
        
        /* 基础模式结果界面 */
        .basic-result {
            text-align: center;
            padding: 30px;
            background: rgba(255, 245, 250, 0.9);
            border-radius: 25px;
            box-shadow: 0 10px 30px rgba(180, 100, 220, 0.2);
            border: 2px solid #d88cff;
            max-width: 600px;
            margin: auto;
        }
        
        .basic-result h2 {
            color: #8a4bcf;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .basic-result p {
            color: #7a5a9a;
            font-size: 1.1rem;
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        /* 图片上传区域 */
        .image-upload-container {
            margin-top: 15px;
            border: 2px dashed rgba(216, 140, 255, 0.5);
            border-radius: 15px;
            padding: 15px;
            background: rgba(255, 240, 245, 0.7);
        }
        
        .upload-area {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            cursor: pointer;
        }
        
        .upload-icon {
            font-size: 2rem;
            color: #d88cff;
        }
        
        .upload-text {
            color: #7a5a9a;
            text-align: center;
        }
        
        .uploaded-images {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
            max-height: 200px;
            overflow-y: auto;
        }
        
        .uploaded-image {
            width: 80px;
            height: 80px;
            border-radius: 10px;
            object-fit: cover;
            border: 1px solid rgba(216, 140, 255, 0.3);
        }
        
        /* 层级弹窗 */
        .sub-modal {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(255, 245, 250, 0.95);
            border-radius: 20px;
            padding: 30px;
            width: 90%;
            max-width: 900px;
            max-height: 90vh;
            overflow-y: auto;
            z-index: 2000;
            box-shadow: 0 0 30px rgba(216, 140, 255, 0.5);
            border: 2px solid #d88cff;
            display: none;
        }
        
        .sub-modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px dashed #d88cff;
        }
        
        .sub-modal-title {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            font-size: 1.8rem;
        }
        
        .sub-modal-content {
            display: flex;
            gap: 25px;
            height: 500px;
        }
        
        .text-content {
            flex: 1;
            padding: 20px;
            background: rgba(255, 240, 245, 0.8);
            border-radius: 15px;
            border: 1px solid rgba(230, 180, 255, 0.4);
            overflow-y: auto;
        }
        
        .feature-section {
            margin-bottom: 20px;
        }
        
        .feature-section h3 {
            color: #d88cff;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .feature-section textarea {
            width: 100%;
            min-height: 80px;
            padding: 12px;
            border-radius: 12px;
            background: rgba(255, 240, 245, 0.9);
            border: 1px solid rgba(230, 180, 255, 0.5);
            color: #7a5a9a;
            resize: vertical;
            font-size: 0.95rem;
            margin-bottom: 10px;
        }
        
        .image-content {
            flex: 1;
            padding: 20px;
            background: rgba(255, 240, 245, 0.8);
            border-radius: 15px;
            border: 1px solid rgba(230, 180, 255, 0.4);
            display: flex;
            flex-direction: column;
        }
        
        .image-content h3 {
            color: #d88cff;
            margin-bottom: 15px;
        }
        
        .modal-images {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            flex: 1;
            overflow-y: auto;
            padding: 10px;
        }
        
        .modal-image {
            width: 120px;
            height: 120px;
            border-radius: 15px;
            object-fit: cover;
            border: 1px solid rgba(216, 140, 255, 0.3);
            cursor: pointer;
        }
        
        .modal-add-image {
            width: 120px;
            height: 120px;
            border-radius: 15px;
            background: rgba(216, 140, 255, 0.2);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #8a4bcf;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 2rem;
        }
        
        .modal-add-image:hover {
            background: rgba(216, 140, 255, 0.4);
        }
        
        .audio-section {
            background: rgba(255, 240, 245, 0.8);
            border-radius: 15px;
            padding: 15px;
            margin-top: 20px;
            border: 1px solid rgba(230, 180, 255, 0.4);
        }
        
        .audio-section h3 {
            color: #d88cff;
            margin-bottom: 10px;
        }
        
        .audio-controls {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .audio-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(216, 140, 255, 0.3);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #8a4bcf;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .audio-btn:hover {
            background: rgba(216, 140, 255, 0.5);
            transform: scale(1.1);
        }
        
        .audio-name {
            flex: 1;
            font-size: 0.9rem;
            color: #7a5a9a;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
        }
        
        /* 弹幕效果 - 优化 */
        .danmu-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 5;
        }
        
        .danmu {
            position: absolute;
            white-space: nowrap;
            color: rgba(255, 255, 255, 0.7); /* 更浅的颜色 */
            font-size: 1rem; /* 稍小字体 */
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3); /* 调整阴影 */
            animation: danmuMove linear;
            font-weight: normal; /* 非粗体 */
            opacity: 0.8;
        }
        
        @keyframes danmuMove {
            from { transform: translateX(100%); }
            to { transform: translateX(-100%); }
        }
        
        /* 烟花效果 */
        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            pointer-events: none;
            animation: fireworkAnimation 1s ease-out forwards;
            z-index: 3000;
        }
        
        @keyframes fireworkAnimation {
            0% { transform: translate(0, 0); opacity: 1; }
            100% { transform: translate(var(--tx), var(--ty)); opacity: 0; }
        }
        
        /* 组图布局 */
        .image-text-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 20px;
        }
        
        .image-text-item {
            background: rgba(255, 240, 245, 0.8);
            border-radius: 15px;
            padding: 15px;
            text-align: center;
            border: 1px solid rgba(230, 180, 255, 0.4);
        }
        
        .image-text-item img {
            width: 100%;
            height: 150px;
            border-radius: 10px;
            object-fit: cover;
            margin-bottom: 10px;
        }
        
        .image-text-item p {
            color: #7a5a9a;
            font-size: 0.9rem;
            margin: 0;
        }
        
        .add-item-btn {
            width: 100%;
            padding: 10px;
            background: rgba(216, 140, 255, 0.2);
            border: 1px dashed rgba(216, 140, 255, 0.5);
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
        }
        
        .add-item-btn:hover {
            background: rgba(216, 140, 255, 0.3);
        }
        
        /* 财富弹窗 */
        .wealth-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .wealth-content {
            background: rgba(255, 245, 250, 0.95);
            border-radius: 25px;
            padding: 30px;
            width: 90%;
            max-width: 900px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 0 30px rgba(216, 140, 255, 0.4);
            border: 2px solid #d88cff;
        }
        
        .wealth-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px dashed #d88cff;
        }
        
        .wealth-title {
            font-family: 'Orbitron', sans-serif;
            color: #8a4bcf;
            font-size: 1.8rem;
            text-shadow: 0 0 5px rgba(216, 140, 255, 0.3);
        }
        
        .wealth-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .wealth-btn {
            padding: 15px;
            background: rgba(255, 240, 245, 0.8);
            border: 1px solid rgba(230, 180, 255, 0.4);
            border-radius: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .wealth-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(216, 140, 255, 0.2);
        }
        
        .wealth-btn i {
            font-size: 2rem;
            color: #d88cff;
            margin-bottom: 10px;
        }
        
        .wealth-btn h4 {
            color: #8a4bcf;
            font-size: 1.2rem;
        }
        
        /* 自媒体弹窗 */
        .social-media-modal {
            background: white;
            border-radius: 15px;
            width: 90%;
            max-width: 400px;
            padding: 20px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }
        
        .social-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .social-title {
            font-size: 1.4rem;
            color: #8a4bcf;
        }
        
        .social-content {
            max-height: 500px;
            overflow-y: auto;
        }
        
        .social-message {
            background: #f0f0f0;
            border-radius: 10px;
            padding: 10px;
            margin-bottom: 10px;
            animation: fadeIn 0.3s;
        }
        
        .social-message.new {
            background: #e6f7ff;
            border-left: 3px solid #1890ff;
        }
        
        .social-message .sender {
            font-weight: bold;
            color: #8a4bcf;
        }
        
        .social-message .time {
            font-size: 0.8rem;
            color: #999;
            margin-left: 10px;
        }
        
        .social-message .content {
            margin-top: 5px;
        }
        
        /* 商务邀约弹窗 */
        .business-modal {
            background: white;
            border-radius: 15px;
            width: 90%;
            max-width: 400px;
            padding: 0;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }
        
        .business-header {
            background: #8a4bcf;
            color: white;
            padding: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .business-header i {
            font-size: 1.5rem;
        }
        
        .business-chat-list {
            height: 500px;
            overflow-y: auto;
            padding: 10px;
        }
        
        .chat-item {
            display: flex;
            padding: 10px;
            border-bottom: 1px solid #eee;
            cursor: pointer;
        }
        
        .chat-item:hover {
            background: #f9f0ff;
        }
        
        .chat-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: #d88cff;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .chat-info {
            flex: 1;
            margin-left: 10px;
        }
        
        .chat-name {
            font-weight: bold;
            color: #5a3a7a;
        }
        
        .chat-preview {
            color: #999;
            font-size: 0.9rem;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .chat-time {
            font-size: 0.8rem;
            color: #999;
        }
        
        .unread-badge {
            background: #ff4d4f;
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 0.7rem;
            margin-top: 5px;
        }
        
        .chat-window {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            max-width: 400px;
            height: 600px;
            background: white;
            border-radius: 15px;
            z-index: 3000;
            box-shadow: 0 5px 30px rgba(0,0,0,0.2);
            flex-direction: column;
        }
        
        .chat-header {
            background: #8a4bcf;
            color: white;
            padding: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-radius: 15px 15px 0 0;
        }
        
        .chat-messages {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            background: #f5f5f5;
        }
        
        .message {
            max-width: 80%;
            padding: 10px;
            margin-bottom: 15px;
            border-radius: 10px;
            position: relative;
        }
        
        .message.received {
            background: white;
            align-self: flex-start;
            border: 1px solid #eee;
        }
        
        .message.sent {
            background: #d6e9ff;
            align-self: flex-end;
            margin-left: auto;
        }
        
        .message-text {
            font-size: 0.95rem;
        }
        
        .message-time {
            font-size: 0.7rem;
            color: #999;
            text-align: right;
            margin-top: 5px;
        }
        
        .chat-input-area {
            display: flex;
            padding: 10px;
            background: white;
            border-top: 1px solid #eee;
            border-radius: 0 0 15px 15px;
        }
        
        .chat-options {
            display: flex;
            gap: 10px;
            padding: 10px;
            background: white;
            border-top: 1px solid #eee;
        }
        
        .chat-option {
            flex: 1;
            padding: 10px;
            background: #f0f0f0;
            border-radius: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .chat-option:hover {
            background: #e0e0e0;
        }
        
        .disabled {
            opacity: 0.5;
            pointer-events: none;
        }
        
        /* 图片弹窗 */
        .image-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 3000;
            justify-content: center;
            align-items: center;
        }
        
        .image-modal-content {
            max-width: 90%;
            max-height: 90%;
        }
        
        .image-modal-content img {
            max-width: 100%;
            max-height: 90vh;
            border-radius: 10px;
        }
        
        /* 响应式设计 */
        @media (max-width: 900px) {
            .mode-container {
                flex-direction: column;
            }
            
            .mode {
                min-width: 100%;
            }
            
            .dashboard {
                grid-template-columns: 1fr;
                grid-auto-rows: minmax(280px, auto);
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .earth {
                width: 70px;
                height: 70px;
            }
            
            .sub-modal-content {
                flex-direction: column;
                height: auto;
            }
            
            .image-text-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 15px;
                min-height: 95vh;
            }
            
            h1 {
                font-size: 1.5rem;
            }
            
            p {
                font-size: 0.9rem;
            }
            
            .mode {
                padding: 15px;
            }
            
            .mode h3 {
                font-size: 1.3rem;
            }
            
            .mode .percentage {
                font-size: 1.8rem;
            }
            
            .module {
                padding: 15px;
            }
            
            .loading-title {
                font-size: 1.5rem;
            }
            
            .loading-text {
                font-size: 1rem;
            }
            
            .card-sections {
                grid-template-columns: 1fr;
                grid-auto-rows: minmax(120px, auto);
            }
            
            .user-nickname {
                top: 10px;
                right: 10px;
                padding: 6px 10px;
                font-size: 0.9rem;
            }
            
            .user-nickname input {
                width: 100px;
                font-size: 0.9rem;
            }
            
            .appearance-body {
                flex-direction: column;
            }
            
            .sub-modal {
                padding: 20px;
            }
            
            .image-text-grid {
                grid-template-columns: 1fr;
            }
            
            .wealth-buttons {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- 粒子背景 -->
    <div class="particles" id="particles"></div>
    
    <!-- 霓虹装饰线 -->
    <div class="neon-line" style="top: 15%; left: 5%; width: 30%;"></div>
    <div class="neon-line" style="bottom: 20%; right: 5%; width: 25%;"></div>
    
    <!-- 右上角昵称 -->
    <div class="user-nickname">
        <input type="text" id="nickname-input" placeholder="点击设置昵称" value="宇宙少女">
        <i class="fas fa-edit" id="edit-nickname"></i>
    </div>
    
    <div class="container">
        <!-- 登录界面 -->
        <div class="screen active" id="login-screen">
            <div class="earth"></div>
            <h1>欢迎来到地球🌏ONLINE</h1>
            <p>大型沉浸式虚拟现实游戏</p>
            <button class="btn" id="login-btn">登录</button>
        </div>
        
        <!-- 自由度选择界面 -->
        <div class="screen" id="mode-screen">
            <h1>玩家自由度选择</h1>
            
            <div class="mode-container">
                <div class="mode">
                    <h3>基础模式</h3>
                    <div class="percentage">0%</div>
                    <p>自由操作权限</p>
                    <ul>
                        <li>金钱匮乏</li>
                        <li>关系失控</li>
                        <li>情绪崩溃</li>
                        <li>健康卡顿</li>
                    </ul>
                    <button class="btn mode-btn" data-mode="basic">获得</button>
                </div>
                
                <div class="mode">
                    <h3>高级模式</h3>
                    <div class="percentage">100%</div>
                    <p>自由操作权限</p>
                    <ul>
                        <li>自由、精致、松弛、真实</li>
                        <li>无穷的爱与善意</li>
                        <li>轻盈健康的身体</li>
                        <li>富足与幸福的生活</li>
                    </ul>
                    <button class="btn mode-btn" data-mode="advanced">获得</button>
                </div>
            </div>
        </div>
        
        <!-- 基础模式结果界面 -->
        <div class="screen" id="basic-result-screen">
            <div class="basic-result">
                <h2>经高我检测</h2>
                <p>您已是高级玩家，不再受外界任何事物的限制，轻松富足的生活，源源不断的金钱和幸福随时等待您的支配，新的秩序由您来定义</p>
                <p>祝您在地球🌏online中玩的愉快</p>
                <button class="btn" id="return-btn">返回</button>
            </div>
        </div>
        
        <!-- 加载界面 -->
        <div class="screen" id="loading-screen">
            <div class="loading-screen">
                <h2 class="loading-title">正在激活高级权限</h2>
                <p class="loading-text">正在为您配置高级自由操作环境...</p>
                
                <div class="progress-container">
                    <div class="progress-bar" id="progress-bar"></div>
                </div>
                
                <div class="progress-text" id="progress-text">0%</div>
                
                <div class="loading-dots">
                    <div class="dot"></div>
                    <div class="dot"></div>
                    <div class="dot"></div>
                </div>
            </div>
        </div>
        
        <!-- 主界面 -->
        <div class="screen" id="main-screen">
            <h1><i class="fas fa-crown"></i> 我的地球Online控制台</h1>
            <p>欢迎回来，大女主！请开始定制您的专属世界</p>
            
            <div class="dashboard">
                <!-- 地球online游戏攻略 -->
                <div class="module editable">
                    <h3><i class="fas fa-book"></i> 地球Online游戏攻略</h3>
                    <div class="module-content guide-section" id="guide-section">
                        <div class="guide-item" data-title="爱自己通关秘籍" data-content="爱自己是通关的第一步，也是最重要的一步。每天花15分钟与自己对话，肯定自己的价值，感恩自己的存在。当你的内心充满爱，整个世界都会为你让路。">
                            <div class="guide-text">爱自己通关秘籍</div>
                            <div class="interaction">
                                <button class="like-btn"><i class="fas fa-heart"></i> <span class="like-count">42</span></button>
                                <button class="tip-btn"><i class="fas fa-gift"></i> 打赏</button>
                                <button class="delete-btn"><i class="fas fa-trash"></i></button>
                            </div>
                        </div>
                        <div class="guide-item" data-title="财富自由指南" data-content="财富自由的关键在于改变你对金钱的信念系统。每天重复肯定语：'我是金钱的磁铁，财富源源不断地流向我'。同时，想象自己已经拥有富足生活的感觉，让这种频率吸引现实中的财富。">
                            <div class="guide-text">财富自由指南</div>
                            <div class="interaction">
                                <button class="like-btn"><i class="fas fa-heart"></i> <span class="like-count">35</span></button>
                                <button class="tip-btn"><i class="fas fa-gift"></i> 打赏</button>
                                <button class="delete-btn"><i class="fas fa-trash"></i></button>
                            </div>
                        </div>
                        <div class="guide-item" data-title="人际关系升级" data-content="健康的人际关系始于自我边界。学会说'不'，同时无条件地给予爱而不期待回报。当你尊重自己，他人也会尊重你。记住：你吸引的人反映了你对自己的信念。">
                            <div class="guide-text">人际关系升级</div>
                            <div class="interaction">
                                <button class="like-btn"><i class="fas fa-heart"></i> <span class="like-count">28</span></button>
                                <button class="tip-btn"><i class="fas fa-gift"></i> 打赏</button>
                                <button class="delete-btn"><i class="fas fa-trash"></i></button>
                            </div>
                        </div>
                    </div>
                    <button class="btn" id="add-article-btn" style="margin-top: 10px; width: 100%;">发布新攻略</button>
                </div>
                
                <!-- 身份卡 -->
                <div class="module editable">
                    <h3><i class="fas fa-id-card"></i> 身份卡</h3>
                    <div class="module-content card-sections">
                        <div class="card-section" data-card="appearance" id="appearance-card">
                            <h4><i class="fas fa-user"></i> 外貌</h4>
                            <ul class="card-list" id="appearance-text">
                                <li>捏脸</li>
                                <li>身材</li>
                                <li>发质</li>
                                <li>皮肤</li>
                            </ul>
                        </div>
                        
                        <div class="card-section" data-card="wealth" id="wealth-card">
                            <h4><i class="fas fa-coins"></i> 财富</h4>
                            <ul class="card-list" id="wealth-text">
                                <li>银行卡账户</li>
                                <li>自媒体</li>
                                <li>商务邀约</li>
                            </ul>
                        </div>
                        
                        <div class="card-section" data-card="relationships" id="relationships-card">
                            <h4><i class="fas fa-users"></i> 人物关系</h4>
                            <ul class="card-list" id="relationships-text">
                                <li>家人</li>
                                <li>朋友</li>
                                <li>恋人</li>
                            </ul>
                        </div>
                        
                        <div class="card-section" data-card="self-talk">
                            <h4><i class="fas fa-comment-dots"></i> 对自己说的话</h4>
                            <div class="image-preview" id="self-talk-preview">
                                <div style="padding: 10px; color: #7a5a9a; font-style: italic;" id="self-talk-text" contenteditable="true">
                                    我是宇宙的宠儿，我值得所有美好！
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- 显化日记 -->
                <div class="module">
                    <h3><i class="fas fa-feather-alt"></i> 显化日记</h3>
                    <div class="module-content">
                        <div class="diary-container" id="diary-container">
                            <div class="diary-entry">
                                <div class="diary-header">
                                    <span>小仙女</span>
                                    <span>2023-10-15</span>
                                </div>
                                <div class="diary-content">今天成功显化了理想的收入，宇宙真的在回应我的每一个愿望！</div>
                            </div>
                            <div class="diary-entry">
                                <div class="diary-header">
                                    <span>能量女王</span>
                                    <span>2023-10-14</span>
                                </div>
                                <div class="diary-content">专注于自我提升的一天，感觉内在力量越来越强大了。</div>
                            </div>
                            <div class="diary-entry">
                                <div class="diary-header">
                                    <span>宇宙宠儿</span>
                                    <span>2023-10-13</span>
                                </div>
                                <div class="diary-content">今天收到了意外的礼物，感恩宇宙的慷慨！</div>
                            </div>
                        </div>
                        <div class="add-diary">
                            <textarea class="diary-input" id="diary-input" placeholder="写下您的显化日记..."></textarea>
                            <button class="btn" id="publish-diary">发布</button>
                        </div>
                    </div>
                </div>
                
                <!-- 爱世界 -->
                <div class="module">
                    <h3><i class="fas fa-heart"></i> 爱世界</h3>
                    <div class="module-content">
                        <div class="bubble-world" id="bubble-world">
                            <div class="bubble" style="width: 100px; height: 100px; top: 15%; left: 10%;">爱自己是终身浪漫的开始</div>
                            <div class="bubble" style="width: 90px; height: 90px; top: 35%; left: 65%;">我的能量由我定义</div>
                            <div class="bubble" style="width: 110px; height: 110px; top: 55%; left: 25%;">专注自我，世界为我让路</div>
                            <div class="bubble" style="width: 80px; height: 80px; top: 15%; left: 55%;">我是宇宙的宠儿</div>
                            <div class="bubble" style="width: 95px; height: 95px; top: 65%; left: 60%;">每一天都更爱自己</div>
                            <div class="bubble" style="width: 105px; height: 105px; top: 40%; left: 40%;">我值得所有美好</div>
                            
                            <div class="add-bubble-btn" id="add-bubble-btn">
                                <i class="fas fa-plus"></i>
                            </div>
                            
                            <div class="bubble-form" id="bubble-form">
                                <textarea class="bubble-input" id="bubble-input" placeholder="写下您对世界的爱..."></textarea>
                                <button class="btn" id="publish-bubble">发布泡泡</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- 文章弹窗 -->
    <div class="modal" id="article-modal">
        <div class="modal-content">
            <span class="close-modal" id="close-modal">&times;</span>
            <h2 class="modal-title">创建新攻略</h2>
            <div class="modal-body">
                <input type="text" id="article-title" placeholder="攻略标题" style="width: 100%; padding: 12px; border-radius: 12px; background: rgba(255, 240, 245, 0.8); border: 1px solid rgba(230, 180, 255, 0.5); color: #7a5a9a; margin-bottom: 15px; font-size: 1rem;">
                <textarea id="article-content" placeholder="在这里输入您的攻略内容..." style="width: 100%; height: 200px; padding: 15px; border-radius: 15px; background: rgba(255, 240, 245, 0.8); border: 1px solid rgba(230, 180, 255, 0.5); color: #7a5a9a; font-size: 1rem; resize: vertical;"></textarea>
                
                <div class="image-upload-container">
                    <div class="upload-area" id="image-upload-area">
                        <i class="fas fa-cloud-upload-alt upload-icon"></i>
                        <p class="upload-text">点击或拖拽图片到此处上传<br>支持多图上传</p>
                        <input type="file" id="article-images" accept="image/*" multiple style="display:none">
                    </div>
                    <div class="uploaded-images" id="uploaded-images"></div>
                </div>
                
                <div style="margin-top: 15px;">
                    <button class="btn" id="publish-article">发布攻略</button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- 外貌弹窗 -->
    <div class="appearance-modal" id="appearance-modal">
        <div class="appearance-content">
            <div class="appearance-header">
                <h2 class="appearance-title"><i class="fas fa-user"></i> 外貌档案</h2>
                <span class="close-modal" id="close-appearance-modal">&times;</span>
            </div>
            
            <div class="appearance-body">
                <div class="appearance-images">
                    <div class="image-grid">
                        <div class="appearance-image" id="face-btn" data-type="face">
                            <i class="fas fa-smile" style="font-size: 3rem; color: #d88cff;"></i>
                            <h3>捏脸</h3>
                        </div>
                        <div class="appearance-image" id="body-btn" data-type="body">
                            <i class="fas fa-running" style="font-size: 3rem; color: #d88cff;"></i>
                            <h3>身材</h3>
                        </div>
                        <div class="appearance-image" id="hair-btn" data-type="hair">
                            <i class="fas fa-cut" style="font-size: 3rem; color: #d88cff;"></i>
                            <h3>发质</h3>
                        </div>
                        <div class="appearance-image" id="skin-btn" data-type="skin">
                            <i class="fas fa-spa" style="font-size: 3rem; color: #d88cff;"></i>
                            <h3>皮肤</h3>
                        </div>
                    </div>
                </div>
            </div>
            <div class="danmu-container" id="appearance-danmu"></div>
        </div>
    </div>
    
    <!-- 外貌细节弹窗 -->
    <div class="sub-modal" id="face-modal">
        <div class="sub-modal-header">
            <h2 class="sub-modal-title"><i class="fas fa-smile"></i> 捏脸详情</h2>
            <span class="close-modal" id="close-face-modal">&times;</span>
        </div>
        <div class="sub-modal-content">
            <div class="text-content">
                <div class="feature-section">
                    <h3>描述</h3>
                    <textarea placeholder="添加捏脸描述...">冷萌女高幼态猫系狐系</textarea>
                </div>
            </div>
            <div class="image-content">
                <h3><i class="fas fa-images"></i> 图片</h3>
                <div class="modal-images" id="face-images">
                    <div class="modal-add-image" id="add-face-image">
                        <i class="fas fa-plus"></i>
                    </div>
                </div>
            </div>
            <div class="danmu-container" id="face-danmu"></div>
        </div>
    </div>
    
    <!-- 财富弹窗 -->
    <div class="wealth-modal" id="wealth-modal">
        <div class="wealth-content">
            <div class="wealth-header">
                <h2 class="wealth-title"><i class="fas fa-coins"></i> 财富档案</h2>
                <span class="close-modal" id="close-wealth-modal">&times;</span>
            </div>
            
            <div class="wealth-buttons">
                <div class="wealth-btn" id="bank-balance-btn">
                    <i class="fas fa-credit-card"></i>
                    <h4>银行卡账户</h4>
                </div>
                <div class="wealth-btn" id="social-media-btn">
                    <i class="fas fa-users"></i>
                    <h4>自媒体</h4>
                </div>
                <div class="wealth-btn" id="business-btn">
                    <i class="fas fa-handshake"></i>
                    <h4>商务邀约</h4>
                </div>
            </div>
            
            <div class="danmu-container" id="wealth-danmu"></div>
        </div>
    </div>
    
    <!-- 银行卡账户弹窗 -->
    <div class="sub-modal" id="bank-modal">
        <div class="sub-modal-header">
            <h2 class="sub-modal-title"><i class="fas fa-credit-card"></i> 银行卡账户</h2>
            <span class="close-modal" id="close-bank-modal">&times;</span>
        </div>
        <div class="sub-modal-content">
            <div class="text-content">
                <div class="feature-section">
                    <h3>账户信息</h3>
                    <div style="background: #f9f0ff; padding: 15px; border-radius: 10px;">
                        <p><strong>账户名称:</strong> 宇宙少女</p>
                        <p><strong>账号:</strong> 6225 8888 6666 7777</p>
                        <p><strong>余额:</strong> ¥999,999.00</p>
                        <p><strong>开户行:</strong> 宇宙银行</p>
                    </div>
                </div>
                
                <div class="feature-section">
                    <h3>交易记录</h3>
                    <div style="background: #f9f0ff; padding: 15px; border-radius: 10px; max-height: 200px; overflow-y: auto;">
                        <p>2023-10-20 收入 +¥50,000.00 自媒体收益</p>
                        <p>2023-10-19 支出 -¥2,500.00 购物消费</p>
                        <p>2023-10-18 收入 +¥20,000.00 商务合作</p>
                        <p>2023-10-17 支出 -¥1,200.00 餐饮消费</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- 自媒体弹窗 -->
    <div class="sub-modal" id="social-media-modal">
        <div class="sub-modal-header">
            <h2 class="sub-modal-title"><i class="fas fa-users"></i> 自媒体账号</h2>
            <span class="close-modal" id="close-social-media-modal">&times;</span>
        </div>
        <div class="sub-modal-content">
            <div class="social-media-modal">
                <div class="social-header">
                    <h3 class="social-title">@宇宙少女</h3>
                </div>
                <div class="social-content" id="social-messages">
                    <div class="social-message">
                        <div><span class="sender">系统消息</span><span class="time">刚刚</span></div>
                        <div class="content">您有新的粉丝关注！</div>
                    </div>
                    <div class="social-message">
                        <div><span class="sender">用户小星星</span><span class="time">2分钟前</span></div>
                        <div class="content">姐姐的分享太棒了！学到了很多！</div>
                    </div>
                    <div class="social-message">
                        <div><span class="sender">系统消息</span><span class="time">5分钟前</span></div>
                        <div class="content">您的视频获得了1000次播放！</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- 商务邀约弹窗 -->
    <div class="sub-modal" id="business-modal">
        <div class="sub-modal-header">
            <h2 class="sub-modal-title"><i class="fas fa-handshake"></i> 商务邀约</h2>
            <span class="close-modal" id="close-business-modal">&times;</span>
        </div>
        <div class="sub-modal-content">
            <div class="business-modal">
                <div class="business-header">
                    <i class="fas fa-comments"></i>
                    <h3>品牌邀约</h3>
                </div>
                <div class="business-chat-list" id="business-chat-list">
                    <div class="chat-item" data-brand="gucci">
                        <div class="chat-avatar">G</div>
                        <div class="chat-info">
                            <div class="chat-name">Gucci</div>
                            <div class="chat-preview">我们诚挚邀请您参加新品发布会...</div>
                        </div>
                        <div class="chat-time">10:20</div>
                        <div class="unread-badge">3</div>
                    </div>
                    <div class="chat-item" data-brand="dior">
                        <div class="chat-avatar">D</div>
                        <div class="chat-info">
                            <div class="chat-name">Dior</div>
                            <div class="chat-preview">期待与您合作春季限定系列...</div>
                        </div>
                        <div class="chat-time">09:45</div>
                        <div class="unread-badge">1</div>
                    </div>
                    <div class="chat-item" data-brand="lv">
                        <div class="chat-avatar">L</div>
                        <div class="chat-info">
                            <div class="chat-name">Louis Vuitton</div>
                            <div class="chat-preview">您的风格非常适合我们的品牌...</div>
                        </div>
                        <div class="chat-time">昨天</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- 聊天窗口 -->
    <div class="chat-window" id="chat-window">
        <div class="chat-header">
            <i class="fas fa-arrow-left" id="back-to-chats"></i>
            <h3 id="chat-brand">Gucci</h3>
        </div>
        <div class="chat-messages" id="chat-messages">
            <div class="message received">
                <div class="message-text">尊敬的宇宙少女，我们诚挚邀请您参加11月15日在上海举办的Gucci 2023冬季新品发布会。我们将为您提供丰厚的报酬，并承担所有差旅费用。</div>
                <div class="message-time">10:20</div>
            </div>
        </div>
        <div class="chat-options" id="chat-options">
            <div class="chat-option" id="option-accept">我对你们家的产品和理念很感兴趣，我会准时参加的</div>
            <div class="chat-option" id="option-decline">抱歉，我最近的档期已满，期待下次合作</div>
        </div>
    </div>
    
    <!-- 图片弹窗 -->
    <div class="image-modal" id="image-modal">
        <div class="image-modal-content">
            <img id="modal-image" src="" alt="预览图片">
        </div>
    </div>
    
    <!-- 打赏成功提示 -->
    <div class="tip-success" id="tip-success">
        <h3>打赏成功</h3>
        <p>感谢您的打赏，丰盛的频率被检测到，10倍返现将打款到您的银行卡账户中</p>
        <button class="btn" id="close-tip">确定</button>
    </div>

    <script>
        // 创建粒子背景
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 80;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // 随机大小
                const size = Math.random() * 3 + 1;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // 随机位置
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `-${size}px`;
                
                // 随机动画时间和延迟
                const duration = Math.random() * 20 + 10;
                particle.style.animationDuration = `${duration}s`;
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                // 随机颜色
                const colors = ['#ff9ff3', '#f368e0', '#d88cff', '#ffaae0'];
                const color = colors[Math.floor(Math.random() * colors.length)];
                particle.style.backgroundColor = color;
                
                particlesContainer.appendChild(particle);
            }
        }
        
        // 创建烟花效果
        function createFireworks(x, y, count = 30) {
            for (let i = 0; i < count; i++) {
                const firework = document.createElement('div');
                firework.className = 'firework';
                
                // 随机颜色
                const colors = ['#ff9ff3', '#f368e0', '#d88cff', '#ffaae0', '#ff6b9c', '#b56cdf'];
                const color = colors[Math.floor(Math.random() * colors.length)];
                firework.style.backgroundColor = color;
                
                // 随机大小
                const size = Math.random() * 3 + 1;
                firework.style.width = `${size}px`;
                firework.style.height = `${size}px`;
                
                // 随机方向
                const angle = Math.random() * Math.PI * 2;
                const distance = Math.random() * 100 + 50;
                const tx = Math.cos(angle) * distance;
                const ty = Math.sin(angle) * distance;
                
                firework.style.setProperty('--tx', `${tx}px`);
                firework.style.setProperty('--ty', `${ty}px`);
                
                // 设置位置
                firework.style.left = `${x}px`;
                firework.style.top = `${y}px`;
                
                document.body.appendChild(firework);
                
                // 动画结束后移除元素
                setTimeout(() => {
                    firework.remove();
                }, 1000);
            }
        }
        
        // 弹幕内容库
        const danmuContent = [
            "哇！这颜值太能打了吧！",
            "仙女下凡辛苦了！",
            "这气质绝了！",
            "姐姐的颜值是真实存在的吗？",
            "美到让人窒息！",
            "这是什么神仙颜值！",
            "一眼万年！",
            "建模脸！太完美了！",
            "气质这块拿捏得死死的！",
            "这皮肤状态我慕了！",
            "姐姐的头发也太好了吧！",
            "身材比例太绝了！",
            "这是什么神仙姐姐！",
            "美得不像真人！",
            "这颜值是真实存在的吗？",
            "气质女神！爱了爱了！",
            "姐姐我可以！",
            "这发量我酸了！",
            "皮肤好好啊！",
            "这是什么神仙颜值！",
            "气质绝了！",
            "姐姐杀我！",
            "美到犯规！",
            "这颜值是真实存在的吗？",
            "仙女本仙！"
        ];
        
        // 创建弹幕
        function createDanmu(containerId, contentArray = danmuContent) {
            const container = document.getElementById(containerId);
            if (!container) return;
            
            const danmu = document.createElement('div');
            danmu.className = 'danmu';
            danmu.textContent = contentArray[Math.floor(Math.random() * contentArray.length)];
            
            // 随机位置
            const top = Math.floor(Math.random() * 90) + 5;
            danmu.style.top = `${top}%`;
            
            // 随机速度
            const duration = Math.floor(Math.random() * 15) + 10;
            danmu.style.animationDuration = `${duration}s`;
            
            container.appendChild(danmu);
            
            // 动画结束后移除元素
            setTimeout(() => {
                danmu.remove();
            }, duration * 1000);
        }
        
        // 初始化
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // 获取DOM元素
            const loginBtn = document.getElementById('login-btn');
            const loginScreen = document.getElementById('login-screen');
            const modeScreen = document.getElementById('mode-screen');
            const loadingScreen = document.getElementById('loading-screen');
            const mainScreen = document.getElementById('main-screen');
            const progressBar = document.getElementById('progress-bar');
            const progressText = document.getElementById('progress-text');
            const addBubbleBtn = document.getElementById('add-bubble-btn');
            const bubbleForm = document.getElementById('bubble-form');
            const publishBubbleBtn = document.getElementById('publish-bubble');
            const bubbleInput = document.getElementById('bubble-input');
            const publishDiaryBtn = document.getElementById('publish-diary');
            const diaryInput = document.getElementById('diary-input');
            const diaryContainer = document.getElementById('diary-container');
            const articleModal = document.getElementById('article-modal');
            const closeModal = document.getElementById('close-modal');
            const addArticleBtn = document.getElementById('add-article-btn');
            const publishArticleBtn = document.getElementById('publish-article');
            const articleContent = document.getElementById('article-content');
            const articleTitle = document.getElementById('article-title');
            const nicknameInput = document.getElementById('nickname-input');
            const editNickname = document.getElementById('edit-nickname');
            const tipSuccess = document.getElementById('tip-success');
            const closeTip = document.getElementById('close-tip');
            const basicResultScreen = document.getElementById('basic-result-screen');
            const returnBtn = document.getElementById('return-btn');
            const appearanceCard = document.getElementById('appearance-card');
            const appearanceModal = document.getElementById('appearance-modal');
            const closeAppearanceModal = document.getElementById('close-appearance-modal');
            const imageUploadArea = document.getElementById('image-upload-area');
            const articleImagesInput = document.getElementById('article-images');
            const uploadedImages = document.getElementById('uploaded-images');
            
            // 外貌弹窗按钮
            const faceBtn = document.getElementById('face-btn');
            const bodyBtn = document.getElementById('body-btn');
            const hairBtn = document.getElementById('hair-btn');
            const skinBtn = document.getElementById('skin-btn');
            
            // 外貌细节弹窗
            const faceModal = document.getElementById('face-modal');
            const closeFaceModal = document.getElementById('close-face-modal');
            
            // 财富弹窗
            const wealthCard = document.getElementById('wealth-card');
            const wealthModal = document.getElementById('wealth-modal');
            const closeWealthModal = document.getElementById('close-wealth-modal');
            
            // 财富按钮
            const bankBalanceBtn = document.getElementById('bank-balance-btn');
            const socialMediaBtn = document.getElementById('social-media-btn');
            const businessBtn = document.getElementById('business-btn');
            
            // 银行卡弹窗
            const bankModal = document.getElementById('bank-modal');
            const closeBankModal = document.getElementById('close-bank-modal');
            
            // 自媒体弹窗
            const socialMediaModal = document.getElementById('social-media-modal');
            const closeSocialMediaModal = document.getElementById('close-social-media-modal');
            
            // 商务邀约弹窗
            const businessModal = document.getElementById('business-modal');
            const closeBusinessModal = document.getElementById('close-business-modal');
            
            // 聊天窗口
            const chatWindow = document.getElementById('chat-window');
            const backToChats = document.getElementById('back-to-chats');
            const chatMessages = document.getElementById('chat-messages');
            const chatOptions = document.getElementById('chat-options');
            const optionAccept = document.getElementById('option-accept');
            const optionDecline = document.getElementById('option-decline');
            const chatBrand = document.getElementById('chat-brand');
            
            // 图片弹窗
            const imageModal = document.getElementById('image-modal');
            const modalImage = document.getElementById('modal-image');
            
            // 存储数据
            let appData = {
                nickname: localStorage.getItem('nickname') || "宇宙少女",
                articles: JSON.parse(localStorage.getItem('articles')) || [
                    { title: "爱自己通关秘籍", content: "爱自己是通关的第一步，也是最重要的一步。每天花15分钟与自己对话，肯定自己的价值，感恩自己的存在。当你的内心充满爱，整个世界都会为你让路。", likes: 42 },
                    { title: "财富自由指南", content: "财富自由的关键在于改变你对金钱的信念系统。每天重复肯定语：'我是金钱的磁铁，财富源源不断地流向我'。同时，想象自己已经拥有富足生活的感觉，让这种频率吸引现实中的财富。", likes: 35 },
                    { title: "人际关系升级", content: "健康的人际关系始于自我边界。学会说'不'，同时无条件地给予爱而不期待回报。当你尊重自己，他人也会尊重你。记住：你吸引的人反映了你对自己的信念。", likes: 28 }
                ],
                diaryEntries: JSON.parse(localStorage.getItem('diaryEntries')) || [
                    { user: "小仙女", date: "2023-10-15", content: "今天成功显化了理想的收入，宇宙真的在回应我的每一个愿望！" },
                    { user: "能量女王", date: "2023-10-14", content: "专注于自我提升的一天，感觉内在力量越来越强大了。" },
                    { user: "宇宙宠儿", date: "2023-10-13", content: "今天收到了意外的礼物，感恩宇宙的慷慨！" }
                ],
                bubbles: JSON.parse(localStorage.getItem('bubbles')) || [
                    { text: "爱自己是终身浪漫的开始", top: "15%", left: "10%", width: 100, height: 100 },
                    { text: "我的能量由我定义", top: "35%", left: "65%", width: 90, height: 90 },
                    { text: "专注自我，世界为我让路", top: "55%", left: "25%", width: 110, height: 110 },
                    { text: "我是宇宙的宠儿", top: "15%", left: "55%", width: 80, height: 80 },
                    { text: "每一天都更爱自己", top: "65%", left: "60%", width: 95, height: 95 },
                    { text: "我值得所有美好", top: "40%", left: "40%", width: 105, height: 105 }
                ],
                appearanceImages: {
                    face: [],
                    body: [],
                    hair: [],
                    skin: []
                }
            };
            
            // 初始化昵称
            nicknameInput.value = appData.nickname;
            
            // 渲染攻略
            function renderArticles() {
                const guideSection = document.getElementById('guide-section');
                guideSection.innerHTML = '';
                
                appData.articles.forEach((article, index) => {
                    const articleItem = document.createElement('div');
                    articleItem.className = 'guide-item';
                    articleItem.setAttribute('data-index', index);
                    articleItem.innerHTML = `
                        <div class="guide-text">${article.title}</div>
                        <div class="interaction">
                            <button class="like-btn"><i class="fas fa-heart"></i> <span class="like-count">${article.likes}</span></button>
                            <button class="tip-btn"><i class="fas fa-gift"></i> 打赏</button>
                            <button class="delete-btn"><i class="fas fa-trash"></i></button>
                        </div>
                    `;
                    
                    guideSection.appendChild(articleItem);
                    
                    // 添加点击事件
                    articleItem.addEventListener('click', function(e) {
                        if(e.target.classList.contains('like-btn') || 
                           e.target.classList.contains('tip-btn') || 
                           e.target.classList.contains('delete-btn')) {
                            return;
                        }
                        
                        showArticleDetail(index);
                    });
                    
                    // 点赞功能
                    const likeBtn = articleItem.querySelector('.like-btn');
                    likeBtn.addEventListener('click', function() {
                        const likeCount = this.querySelector('.like-count');
                        let count = parseInt(likeCount.textContent);
                        count++;
                        likeCount.textContent = count;
                        
                        // 更新数据
                        appData.articles[index].likes = count;
                        saveData();
                        
                        // 添加动画效果
                        this.style.transform = 'scale(1.2)';
                        setTimeout(() => {
                            this.style.transform = 'scale(1)';
                        }, 300);
                    });
                    
                    // 打赏功能
                    const tipBtn = articleItem.querySelector('.tip-btn');
                    tipBtn.addEventListener('click', function(e) {
                        e.stopPropagation();
                        tipSuccess.style.display = 'block';
                        
                        // 烟花效果
                        const rect = this.getBoundingClientRect();
                        createFireworks(rect.left + rect.width/2, rect.top + rect.height/2);
                        
                        // 10倍返现效果
                        const tipAmount = Math.floor(Math.random() * 9000) + 1000;
                        tipSuccess.querySelector('p').innerHTML = 
                            `感谢您的打赏，丰盛的频率被检测到，<br><strong>¥${tipAmount.toLocaleString()}</strong> 返现已打款到您的银行卡账户中`;
                    });
                    
                    // 删除功能
                    const deleteBtn = articleItem.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', function(e) {
                        e.stopPropagation();
                        appData.articles.splice(index, 1);
                        saveData();
                        renderArticles();
                    });
                });
            }
            
            // 渲染日记
            function renderDiary() {
                const diaryContainer = document.getElementById('diary-container');
                diaryContainer.innerHTML = '';
                
                appData.diaryEntries.forEach(entry => {
                    const diaryEntry = document.createElement('div');
                    diaryEntry.className = 'diary-entry';
                    diaryEntry.innerHTML = `
                        <div class="diary-header">
                            <span>${entry.user}</span>
                            <span>${entry.date}</span>
                        </div>
                        <div class="diary-content">${entry.content}</div>
                    `;
                    
                    diaryContainer.appendChild(diaryEntry);
                });
            }
            
            // 渲染泡泡
            function renderBubbles() {
                const bubbleWorld = document.getElementById('bubble-world');
                
                // 清除现有泡泡（保留按钮）
                const existingBubbles = bubbleWorld.querySelectorAll('.bubble');
                existingBubbles.forEach(bubble => {
                    if (!bubble.classList.contains('add-bubble-btn')) {
                        bubble.remove();
                    }
                });
                
                // 添加泡泡
                appData.bubbles.forEach(bubble => {
                    const bubbleEl = document.createElement('div');
                    bubbleEl.className = 'bubble';
                    bubbleEl.textContent = bubble.text;
                    bubbleEl.style.top = bubble.top;
                    bubbleEl.style.left = bubble.left;
                    bubbleEl.style.width = `${bubble.width}px`;
                    bubbleEl.style.height = `${bubble.height}px`;
                    
                    // 随机动画时间和延迟
                    const duration = Math.floor(Math.random() * 20) + 10;
                    bubbleEl.style.animationDuration = `${duration}s`;
                    bubbleEl.style.animationDelay = `${Math.random() * 5}s`;
                    
                    bubbleWorld.insertBefore(bubbleEl, bubbleWorld.firstChild);
                });
            }
            
            // 显示文章详情
            function showArticleDetail(index) {
                const article = appData.articles[index];
                
                // 创建详情弹窗
                const modalContent = `
                    <div class="modal-content">
                        <span class="close-modal" id="close-article-detail">&times;</span>
                        <h2 class="modal-title">${article.title}</h2>
                        <div class="modal-body">
                            ${article.content.replace(/\n/g, '<br>')}
                            ${article.images && article.images.length > 0 ? 
                                `<div class="image-grid" style="margin-top: 15px;">
                                    ${article.images.map(img => `
                                        <div class="appearance-image">
                                            <img src="${img}" alt="攻略图片">
                                        </div>
                                    `).join('')}
                                </div>` : ''}
                        </div>
                        <div class="interaction-buttons">
                            <button class="like-btn" style="padding: 10px 20px;"><i class="fas fa-heart"></i> <span class="like-count">${article.likes}</span></button>
                            <button class="tip-btn" style="padding: 10px 20px;"><i class="fas fa-gift"></i> 打赏</button>
                        </div>
                        <div class="tip-options">
                            <button class="tip-option">7元</button>
                            <button class="tip-option">17元</button>
                            <button class="tip-option">77元</button>
                            <button class="tip-option">777元</button>
                        </div>
                    </div>
                `;
                
                const modal = document.createElement('div');
                modal.className = 'modal';
                modal.style.display = 'flex';
                modal.innerHTML = modalContent;
                document.body.appendChild(modal);
                
                // 关闭详情弹窗
                modal.querySelector('.close-modal').addEventListener('click', function() {
                    modal.remove();
                });
                
                // 点赞功能
                const likeBtn = modal.querySelector('.like-btn');
                likeBtn.addEventListener('click', function() {
                    const likeCount = this.querySelector('.like-count');
                    let count = parseInt(likeCount.textContent);
                    count++;
                    likeCount.textContent = count;
                    
                    // 更新数据
                    appData.articles[index].likes = count;
                    saveData();
                    
                    // 更新主界面点赞数
                    document.querySelector(`.guide-item[data-index="${index}"] .like-count`).textContent = count;
                    
                    // 添加动画效果
                    this.style.transform = 'scale(1.2)';
                    setTimeout(() => {
                        this.style.transform = 'scale(1)';
                    }, 300);
                });
                
                // 打赏功能
                modal.querySelectorAll('.tip-option').forEach(option => {
                    option.addEventListener('click', function() {
                        const amount = this.textContent;
                        tipSuccess.style.display = 'block';
                        
                        // 烟花效果
                        const rect = this.getBoundingClientRect();
                        createFireworks(rect.left + rect.width/2, rect.top + rect.height/2);
                        
                        // 10倍返现效果
                        const tipAmount = parseInt(amount.replace('元', '')) * 10;
                        tipSuccess.querySelector('p').innerHTML = 
                            `感谢您的打赏，丰盛的频率被检测到，<br><strong>¥${tipAmount.toLocaleString()}</strong> 返现已打款到您的银行卡账户中`;
                    });
                });
            }
            
            // 保存数据到localStorage
            function saveData() {
                localStorage.setItem('nickname', appData.nickname);
                localStorage.setItem('articles', JSON.stringify(appData.articles));
                localStorage.setItem('diaryEntries', JSON.stringify(appData.diaryEntries));
                localStorage.setItem('bubbles', JSON.stringify(appData.bubbles));
                localStorage.setItem('appearanceImages', JSON.stringify(appData.appearanceImages));
            }
            
            // 初始化渲染
            renderArticles();
            renderDiary();
            renderBubbles();
            
            // 登录按钮点击事件
            loginBtn.addEventListener('click', function() {
                loginScreen.classList.remove('active');
                modeScreen.classList.add('active');
            });
            
            // 模式选择按钮点击事件
            document.querySelectorAll('[data-mode]').forEach(btn => {
                btn.addEventListener('click', function() {
                    const mode = this.getAttribute('data-mode');
                    
                    if (mode === 'basic') {
                        // 基础模式显示结果界面
                        modeScreen.classList.remove('active');
                        basicResultScreen.classList.add('active');
                    } else {
                        // 高级模式显示加载界面
                        modeScreen.classList.remove('active');
                        loadingScreen.classList.add('active');
                        
                        // 模拟进度条加载
                        let progress = 0;
                        const interval = setInterval(() => {
                            progress += Math.floor(Math.random() * 5) + 1;
                            if (progress > 100) progress = 100;
                            
                            progressBar.style.width = `${progress}%`;
                            progressText.textContent = `${progress}%`;
                            
                            if (progress >= 100) {
                                clearInterval(interval);
                                
                                // 加载完成后进入主界面
                                setTimeout(() => {
                                    loadingScreen.classList.remove('active');
                                    mainScreen.classList.add('active');
                                }, 800);
                            }
                        }, 200);
                    }
                });
            });
            
            // 返回按钮事件
            returnBtn.addEventListener('click', function() {
                basicResultScreen.classList.remove('active');
                modeScreen.classList.add('active');
            });
            
            // 添加气泡按钮
            addBubbleBtn.addEventListener('click', function() {
                bubbleForm.style.display = 'block';
            });
            
            // 发布泡泡
            publishBubbleBtn.addEventListener('click', function() {
                if (bubbleInput.value.trim() !== '') {
                    // 创建新泡泡
                    const newBubble = {
                        text: bubbleInput.value,
                        top: `${Math.floor(Math.random() * 70)}%`,
                        left: `${Math.floor(Math.random() * 80)}%`,
                        width: Math.floor(Math.random() * 50) + 70,
                        height: Math.floor(Math.random() * 50) + 70
                    };
                    
                    appData.bubbles.push(newBubble);
                    saveData();
                    renderBubbles();
                    
                    // 清空输入框
                    bubbleInput.value = '';
                    
                    // 隐藏表单
                    bubbleForm.style.display = 'none';
                }
            });
            
            // 发布日记
            publishDiaryBtn.addEventListener('click', function() {
                if (diaryInput.value.trim() !== '') {
                    const now = new Date();
                    const dateStr = `${now.getFullYear()}-${String(now.getMonth()+1).padStart(2, '0')}-${String(now.getDate()).padStart(2, '0')}`;
                    
                    const newEntry = {
                        user: appData.nickname,
                        date: dateStr,
                        content: diaryInput.value
                    };
                    
                    appData.diaryEntries.unshift(newEntry);
                    saveData();
                    renderDiary();
                    
                    // 清空输入框
                    diaryInput.value = '';
                }
            });
            
            // 添加新文章按钮
            addArticleBtn.addEventListener('click', function() {
                articleModal.style.display = 'flex';
                articleTitle.value = '';
                articleContent.value = '';
                uploadedImages.innerHTML = '';
            });
            
            // 关闭文章弹窗
            closeModal.addEventListener('click', function() {
                articleModal.style.display = 'none';
            });
            
            // 点击弹窗外部关闭
            window.addEventListener('click', function(event) {
                if (event.target === articleModal) {
                    articleModal.style.display = 'none';
                }
                if (event.target === appearanceModal) {
                    appearanceModal.style.display = 'none';
                }
                if (event.target === wealthModal) {
                    wealthModal.style.display = 'none';
                }
                if (event.target === socialMediaModal) {
                    socialMediaModal.style.display = 'none';
                }
                if (event.target === businessModal) {
                    businessModal.style.display = 'none';
                }
                if (event.target === bankModal) {
                    bankModal.style.display = 'none';
                }
                if (event.target === imageModal) {
                    imageModal.style.display = 'none';
                }
            });
            
            // 发布新文章
            publishArticleBtn.addEventListener('click', function() {
                if (articleTitle.value.trim() !== '' && articleContent.value.trim() !== '') {
                    // 收集上传的图片
                    const images = [];
                    const imgElements = uploadedImages.querySelectorAll('img');
                    imgElements.forEach(img => {
                        images.push(img.src);
                    });
                    
                    // 创建新文章对象
                    const newArticle = {
                        title: articleTitle.value,
                        content: articleContent.value,
                        images: images,
                        likes: 0
                    };
                    
                    appData.articles.push(newArticle);
                    saveData();
                    renderArticles();
                    
                    // 清空输入框
                    articleTitle.value = '';
                    articleContent.value = '';
                    uploadedImages.innerHTML = '';
                    
                    // 关闭弹窗
                    articleModal.style.display = 'none';
                }
            });
            
            // 图片上传区域点击
            imageUploadArea.addEventListener('click', function() {
                articleImagesInput.click();
            });
            
            // 图片上传处理
            articleImagesInput.addEventListener('change', function(e) {
                if (this.files && this.files.length > 0) {
                    for (let i = 0; i < this.files.length; i++) {
                        const file = this.files[i];
                        const reader = new FileReader();
                        
                        reader.onload = function(event) {
                            const img = document.createElement('img');
                            img.className = 'uploaded-image';
                            img.src = event.target.result;
                            img.onclick = function() {
                                modalImage.src = this.src;
                                imageModal.style.display = 'flex';
                            };
                            
                            uploadedImages.appendChild(img);
                        };
                        
                        reader.readAsDataURL(file);
                    }
                }
            });
            
            // 编辑昵称
            editNickname.addEventListener('click', function() {
                nicknameInput.focus();
            });
            
            // 保存昵称
            nicknameInput.addEventListener('blur', function() {
                appData.nickname = this.value.trim() || "宇宙少女";
                saveData();
            });
            
            // 关闭打赏成功提示
            closeTip.addEventListener('click', function() {
                tipSuccess.style.display = 'none';
            });
            
            // 外貌卡片点击事件
            appearanceCard.addEventListener('click', function() {
                appearanceModal.style.display = 'flex';
                
                // 启动外貌弹窗的弹幕
                const danmuInterval = setInterval(() => {
                    createDanmu('appearance-danmu');
                }, 2000);
                
                // 关闭弹窗时清除弹幕
                closeAppearanceModal.addEventListener('click', function() {
                    clearInterval(danmuInterval);
                });
            });
            
            // 关闭外貌弹窗
            closeAppearanceModal.addEventListener('click', function() {
                appearanceModal.style.display = 'none';
            });
            
            // 外貌弹窗按钮点击事件
            faceBtn.addEventListener('click', function() {
                faceModal.style.display = 'block';
                
                // 启动弹幕
                const danmuInterval = setInterval(() => {
                    createDanmu('face-danmu');
                }, 1500);
                
                // 关闭弹窗时清除弹幕
                closeFaceModal.addEventListener('click', function() {
                    clearInterval(danmuInterval);
                });
            });
            
            // 关闭子弹窗
            closeFaceModal.addEventListener('click', function() {
                faceModal.style.display = 'none';
            });
            
            // 财富卡片点击事件
            wealthCard.addEventListener('click', function() {
                wealthModal.style.display = 'flex';
                
                // 启动财富弹窗的弹幕
                const danmuInterval = setInterval(() => {
                    createDanmu('wealth-danmu');
                }, 2000);
                
                // 关闭弹窗时清除弹幕
                closeWealthModal.addEventListener('click', function() {
                    clearInterval(danmuInterval);
                });
            });
            
            // 关闭财富弹窗
            closeWealthModal.addEventListener('click', function() {
                wealthModal.style.display = 'none';
            });
            
            // 银行卡按钮点击
            bankBalanceBtn.addEventListener('click', function() {
                wealthModal.style.display = 'none';
                bankModal.style.display = 'block';
            });
            
            // 关闭银行卡弹窗
            closeBankModal.addEventListener('click', function() {
                bankModal.style.display = 'none';
            });
            
            // 自媒体按钮点击
            socialMediaBtn.addEventListener('click', function() {
                wealthModal.style.display = 'none';
                socialMediaModal.style.display = 'block';
                
                // 启动社交媒体弹幕
                const danmuInterval = setInterval(() => {
                    createDanmu('social-danmu');
                }, 1500);
                
                // 关闭弹窗时清除弹幕
                closeSocialMediaModal.addEventListener('click', function() {
                    clearInterval(danmuInterval);
                });
                
                // 模拟粉丝和点赞增长
                setInterval(() => {
                    const socialMessages = document.getElementById('social-messages');
                    
                    const messages = [
                        { sender: "系统消息", content: "您有新的粉丝关注！" },
                        { sender: "用户小星星", content: "姐姐的分享太棒了！学到了很多！" },
                        { sender: "系统消息", content: "您的视频获得了1000次播放！" },
                        { sender: "用户宇宙粉", content: "期待姐姐的下次更新！" },
                        { sender: "系统消息", content: "您的帖子被推荐到首页！" }
                    ];
                    
                    const randomMessage = messages[Math.floor(Math.random() * messages.length)];
                    
                    const newMessage = document.createElement('div');
                    newMessage.className = 'social-message new';
                    newMessage.innerHTML = `
                        <div><span class="sender">${randomMessage.sender}</span><span class="time">刚刚</span></div>
                        <div class="content">${randomMessage.content}</div>
                    `;
                    
                    socialMessages.insertBefore(newMessage, socialMessages.firstChild);
                    
                    // 移除new类
                    setTimeout(() => {
                        newMessage.classList.remove('new');
                    }, 3000);
                }, 5000);
            });
            
            // 关闭社交媒体弹窗
            closeSocialMediaModal.addEventListener('click', function() {
                socialMediaModal.style.display = 'none';
            });
            
            // 商务邀约按钮点击
            businessBtn.addEventListener('click', function() {
                wealthModal.style.display = 'none';
                businessModal.style.display = 'block';
            });
            
            // 关闭商务邀约弹窗
            closeBusinessModal.addEventListener('click', function() {
                businessModal.style.display = 'none';
            });
            
            // 聊天项点击
            document.querySelectorAll('.chat-item').forEach(item => {
                item.addEventListener('click', function() {
                    const brand = this.getAttribute('data-brand');
                    chatBrand.textContent = brand.charAt(0).toUpperCase() + brand.slice(1);
                    chatWindow.style.display = 'flex';
                    
                    // 清除之前的消息
                    chatMessages.innerHTML = `
                        <div class="message received">
                            <div class="message-text">尊敬的宇宙少女，我们诚挚邀请您参加11月15日在上海举办的${brand.charAt(0).toUpperCase() + brand.slice(1)} 2023冬季新品发布会。我们将为您提供丰厚的报酬，并承担所有差旅费用。</div>
                            <div class="message-time">10:20</div>
                        </div>
                    `;
                    
                    // 启用选项按钮
                    chatOptions.classList.remove('disabled');
                    optionAccept.classList.remove('disabled');
                    optionDecline.classList.remove('disabled');
                });
            });
            
            // 返回聊天列表
            backToChats.addEventListener('click', function() {
                chatWindow.style.display = 'none';
            });
            
            // 接受邀请
            optionAccept.addEventListener('click', function() {
                const brand = chatBrand.textContent;
                const newMessage = document.createElement('div');
                newMessage.className = 'message sent';
                newMessage.innerHTML = `
                    <div class="message-text">我对你们家的产品和理念很感兴趣，我会准时参加的</div>
                    <div class="message-time">${getCurrentTime()}</div>
                `;
                chatMessages.appendChild(newMessage);
                
                // 禁用选项
                chatOptions.classList.add('disabled');
                
                // 品牌回复
                setTimeout(() => {
                    const reply = document.createElement('div');
                    reply.className = 'message received';
                    reply.innerHTML = `
                        <div class="message-text">对于您的到来深感荣幸，我们将为您提供最好的出行安排，最舒适的房间，以及最优质的服务，期待您的到来</div>
                        <div class="message-time">${getCurrentTime()}</div>
                    `;
                    chatMessages.appendChild(reply);
                    chatMessages.scrollTop = chatMessages.scrollHeight;
                }, 1000);
            });
            
            // 拒绝邀请
            optionDecline.addEventListener('click', function() {
                const brand = chatBrand.textContent;
                const newMessage = document.createElement('div');
                newMessage.className = 'message sent';
                newMessage.innerHTML = `
                    <div class="message-text">抱歉，我最近的档期已满，期待下次合作</div>
                    <div class="message-time">${getCurrentTime()}</div>
                `;
                chatMessages.appendChild(newMessage);
                
                // 禁用选项
                chatOptions.classList.add('disabled');
                
                // 品牌回复
                setTimeout(() => {
                    const reply = document.createElement('div');
                    reply.className = 'message received';
                    reply.innerHTML = `
                        <div class="message-text">深感遗憾，但我们这边随时期待您的到来，期待下次合作</div>
                        <div class="message-time">${getCurrentTime()}</div>
                    `;
                    chatMessages.appendChild(reply);
                    chatMessages.scrollTop = chatMessages.scrollHeight;
                }, 1000);
            });
            
            // 获取当前时间
            function getCurrentTime() {
                const now = new Date();
                return `${String(now.getHours()).padStart(2, '0')}:${String(now.getMinutes()).padStart(2, '0')}`;
            }
            
            // 模拟泡泡点击效果
            document.addEventListener('click', function(e) {
                if (e.target.classList.contains('bubble')) {
                    e.target.style.backgroundColor = 'rgba(216, 140, 255, 0.4)';
                    e.target.style.boxShadow = '0 0 20px rgba(255, 170, 224, 0.5)';
                    
                    setTimeout(() => {
                        e.target.style.backgroundColor = 'rgba(216, 140, 255, 0.2)';
                        e.target.style.boxShadow = 'none';
                    }, 1000);
                }
            });
            
            // 自动保存编辑内容
            document.querySelectorAll('[contenteditable="true"]').forEach(element => {
                element.addEventListener('blur', function() {
                    saveData();
                });
            });
            
            // 每10秒添加新的聊天
            setInterval(() => {
                const brands = ["Chanel", "Prada", "Hermes", "Cartier", "Rolex"];
                const randomBrand = brands[Math.floor(Math.random() * brands.length)];
                
                const chatList = document.getElementById('business-chat-list');
                
                const newChat = document.createElement('div');
                newChat.className = 'chat-item';
                newChat.setAttribute('data-brand', randomBrand.toLowerCase());
                newChat.innerHTML = `
                    <div class="chat-avatar">${randomBrand.charAt(0)}</div>
                    <div class="chat-info">
                        <div class="chat-name">${randomBrand}</div>
                        <div class="chat-preview">新的合作邀约，期待您的回复...</div>
                    </div>
                    <div class="chat-time">刚刚</div>
                    <div class="unread-badge">1</div>
                `;
                
                chatList.insertBefore(newChat, chatList.firstChild);
                
                // 添加点击事件
                newChat.addEventListener('click', function() {
                    const brand = this.getAttribute('data-brand');
                    chatBrand.textContent = brand.charAt(0).toUpperCase() + brand.slice(1);
                    chatWindow.style.display = 'flex';
                    
                    // 清除之前的消息
                    chatMessages.innerHTML = `
                        <div class="message received">
                            <div class="message-text">尊敬的宇宙少女，我们诚挚邀请您参加11月15日在上海举办的${brand.charAt(0).toUpperCase() + brand.slice(1)} 2023冬季新品发布会。我们将为您提供丰厚的报酬，并承担所有差旅费用。</div>
                            <div class="message-time">${getCurrentTime()}</div>
                        </div>
                    `;
                    
                    // 启用选项按钮
                    chatOptions.classList.remove('disabled');
                    optionAccept.classList.remove('disabled');
                    optionDecline.classList.remove('disabled');
                });
            }, 10000);
            
            // 初始化弹幕
            setInterval(() => {
                createDanmu('appearance-danmu');
            }, 2000);
        });
    </script>
</body>
</html>
