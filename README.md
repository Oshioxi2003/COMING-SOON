# Coming Soon Page - Trang Sắp Ra Mắt 🚀

Một trang "Coming Soon" chuyên nghiệp với giao diện tối hiện đại, hoàn toàn responsive và đầy đủ tính năng.

## ✨ Tính Năng Chính

### 🎨 Giao Diện
- **Thiết kế tối hiện đại** với gradient xanh-tím
- **Particles bay lơ lửng** tạo hiệu ứng động
- **Animation mượt mà** khi tải trang và tương tác
- **Glass morphism** cho các thành phần UI
- **Responsive design** tối ưu mọi thiết bị

### ⏰ Đồng Hồ Đếm Ngược
- Tự động đếm ngược 30 ngày từ thời điểm hiện tại
- Hiển thị: Ngày - Giờ - Phút - Giây
- Cập nhật real-time mỗi giây
- Tự động hiển thị "Đã Ra Mắt!" khi hết thời gian

### 📧 Form Đăng Ký Email
- Input email với validation
- Hiệu ứng thành công khi submit
- Animation hover và focus
- UI feedback cho người dùng

### 🌐 Liên Kết Mạng Xã Hội
- Icons cho Facebook, Instagram, Twitter, LinkedIn
- Hover effects với shadow và transform
- Dễ dàng thay đổi link và thêm platform mới

## 🚀 Cài Đặt & Sử Dụng

### 1. Triển Khai Cơ Bản
```bash
# Chỉ cần tải file HTML và mở trực tiếp trong trình duyệt
# Không cần server hay dependencies
```

### 2. Tùy Chỉnh Nội Dung

**Thay đổi tiêu đề:**
```html
<h1 class="main-title">TÊN CÔNG TY</h1>
<h2 class="subtitle">Slogan Của Bạn</h2>
```

**Sửa mô tả:**
```html
<p class="description">
    Mô tả về sản phẩm hoặc dịch vụ sắp ra mắt...
</p>
```

**Thay đổi thời gian đếm ngược:**
```javascript
// Trong function updateCountdown()
targetDate.setDate(targetDate.getDate() + 30); // 30 ngày
// Hoặc set ngày cụ thể:
const targetDate = new Date('2024-12-31');
```

### 3. Tùy Chỉnh Logo
```html
<div class="logo"></div>
```
```css
.logo::before {
    content: '🚀'; /* Thay emoji hoặc thêm ảnh */
}
```

### 4. Cập Nhật Links Mạng Xã Hội
```html
<a href="https://facebook.com/yourpage" class="social-link">📘</a>
<a href="https://instagram.com/yourpage" class="social-link">📷</a>
<a href="https://twitter.com/yourpage" class="social-link">🐦</a>
<a href="https://linkedin.com/company/yourcompany" class="social-link">💼</a>
```

## 🎨 Tùy Chỉnh Giao Diện

### Thay Đổi Màu Chính
```css
/* Gradient chính */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Màu text gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
```

### Màu Particles
```css
.particle:nth-child(odd) {
    background: rgba(64, 224, 208, 0.3); /* Xanh ngọc */
}

.particle:nth-child(3n) {
    background: rgba(255, 105, 180, 0.3); /* Hồng */
}
```

### Font Chữ
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

body {
    font-family: 'Poppins', sans-serif;
}
```

## ⚙️ Tích Hợp Backend

### Kết Nối Form Email
```javascript
document.getElementById('emailForm').addEventListener('submit', async function(e) {
    e.preventDefault();
    const email = document.getElementById('emailInput').value;
    
    try {
        const response = await fetch('/api/subscribe', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({ email: email })
        });
        
        if (response.ok) {
            // Hiển thị thành công
        }
    } catch (error) {
        console.error('Error:', error);
    }
});
```

### Google Analytics
```html
<!-- Thêm vào <head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

## 📱 Responsive Breakpoints

```css
/* Mobile */
@media (max-width: 768px) {
    .main-title {
        font-size: 3rem;
    }
    
    .countdown {
        gap: 15px;
    }
    
    .email-form {
        flex-direction: column;
    }
}

/* Tablet */
@media (max-width: 1024px) {
    .container {
        padding: 40px 20px;
    }
}
```

## 🌟 Thêm Tính Năng

### 1. Progress Bar
```html
<div class="progress-container">
    <div class="progress-bar" style="width: 65%"></div>
    <span class="progress-text">65% Hoàn Thành</span>
</div>
```

### 2. Newsletter Popup
```javascript
// Hiện popup sau 30 giây
setTimeout(() => {
    document.getElementById('newsletter-popup').style.display = 'flex';
}, 30000);
```

### 3. Dark/Light Mode Toggle
```javascript
function toggleTheme() {
    document.body.classList.toggle('light-theme');
    localStorage.setItem('theme', document.body.classList.contains('light-theme') ? 'light' : 'dark');
}
```

## 🛠️ Troubleshooting

### Particles Không Hiển Thị
- Kiểm tra JavaScript console có lỗi không
- Đảm bảo `createParticles()` được gọi

### Countdown Không Chạy
- Kiểm tra timezone của server
- Verify target date format

### Form Email Không Hoạt Động
- Kiểm tra preventDefault() được gọi
- Verify email validation

## 📄 Browser Support

- ✅ Chrome (80+)
- ✅ Firefox (75+) 
- ✅ Safari (13+)
- ✅ Edge (80+)
- ❌ Internet Explorer


**Phiên bản:** 1.0  
**Cập nhật:** Tháng 8, 2025  
**Tác giả:** Claude AI Assistant
