# oceanmate
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>海工船务 - 专业船舶设备维护</title>
    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.bootcdn.net/ajax/libs/twitter-bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
    <!-- Font Awesome -->
    <link href="https://cdn.bootcdn.net/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        .navbar {
            background-color: #004d99;
        }
        
        .banner {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('ship-bg.jpg');
            background-size: cover;
            height: 600px;
            color: white;
        }

        .service-card {
            transition: transform 0.3s;
            border: 1px solid #e0e0e0;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .contact-section {
            background-color: #f8f9fa;
        }

        .news-card {
            border-left: 4px solid #004d99;
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">海工船务</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#home">首页</a></li>
                    <li class="nav-item"><a class="nav-link" href="#services">服务项目</a></li>
                    <li class="nav-item"><a class="nav-link" href="#products">设备产品</a></li>
                    <li class="nav-item"><a class="nav-link" href="#news">新闻动态</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">联系我们</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- 首页Banner -->
    <section id="home" class="banner d-flex align-items-center">
        <div class="container text-center">
            <h1 class="display-4 mb-4">专业船舶设备维护服务</h1>
            <p class="lead">24小时快速响应 | 认证工程师团队 | 原厂配件保障</p>
            <a href="#contact" class="btn btn-primary btn-lg mt-3">立即预约服务</a>
        </div>
    </section>

    <!-- 服务项目 -->
    <section id="services" class="py-5">
        <div class="container">
            <h2 class="text-center mb-5">我们的服务</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card service-card h-100">
                        <div class="card-body">
                            <i class="fas fa-tools fa-3x text-primary"></i>
                            <h3 class="mt-3">定期维护保养</h3>
                            <p>专业设备检测、润滑系统维护、零部件更换</p>
                        </div>
                    </div>
                </div>
                <!-- 其他服务卡片类似 -->
            </div>
        </div>
    </section>

    <!-- 产品展示 -->
    <section id="products" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-5">设备产品</h2>
            <div class="row align-items-center">
                <div class="col-md-6">
                    <img src="engine.jpg" alt="船舶发动机" class="img-fluid rounded">
                </div>
                <div class="col-md-6">
                    <h3>船舶动力系统</h3>
                    <p>提供主流品牌发动机维护和原厂配件更换</p>
                    <ul class="list-unstyled">
                        <li><i class="fas fa-check text-primary me-2"></i>柴油发动机大修</li>
                        <li><i class="fas fa-check text-primary me-2"></i>涡轮增压器维护</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系表单 -->
    <section id="contact" class="py-5 contact-section">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <h2>立即联系我们</h2>
                    <form id="contactForm">
                        <div class="mb-3">
                            <input type="text" class="form-control" placeholder="姓名" required>
                        </div>
                        <div class="mb-3">
                            <input type="email" class="form-control" placeholder="邮箱" required>
                        </div>
                        <div class="mb-3">
                            <textarea class="form-control" rows="5" placeholder="留言内容" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">提交申请</button>
                    </form>
                </div>
                <div class="col-md-6 mt-4 mt-md-0">
                    <h3>联系信息</h3>
                    <ul class="list-unstyled">
                        <li><i class="fas fa-map-marker-alt me-2"></i>上海市浦东新区船务路18号</li>
                        <li><i class="fas fa-phone me-2"></i>021-68881234</li>
                        <li><i class="fas fa-envelope me-2"></i>service@marine.com</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-4">
        <div class="container text-center">
            <p>&copy; 2023 海工船务 沪ICP备12345678号</p>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.bootcdn.net/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
    <script>
        // 表单提交处理
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('您的请求已提交，我们将尽快联系您！');
            this.reset();
        });

        // 导航栏滚动效果
        window.addEventListener('scroll', function() {
            if (window.scrollY > 50) {
                document.querySelector('.navbar').style.backgroundColor = '#004d99';
            } else {
                document.querySelector('.navbar').style.backgroundColor = 'transparent';
            }
        });
    </script>
</body>
</html>
