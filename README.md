برای اینکه README خفن و حرفه‌ای به نظر برسه، باید اون رو به یک فایل `README.md` تبدیل کنی و توی ریپازیتوری گیت‌هاب قرار بدی. برای این کار:

## 1. فایل README رو ایجاد کن

```bash
cd /Users/mohammad/Desktop/thelast/myproject
nano README.md
```

## 2. محتوای زیر رو کپی کن داخل فایل:

```markdown
# 🚚 Barsoo - Cargo Management System

**Barsoo** is a comprehensive online platform designed to connect cargo owners with drivers. It streamlines the process of posting, finding, and assigning freight loads. The system features an OTP login system, automated SMS notifications, and a Progressive Web App (PWA) for mobile users.

🌐 **Live Demo:** [https://barsu.ir](https://barsu.ir)

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🔐 **OTP Login** | Secure phone number-based login using One-Time Password |
| 👥 **User Roles** | Separate panels for Admins and Drivers |
| 📦 **Load Management** | Admins can create, edit, and delete cargo loads |
| 👤 **Driver Management** | Admins can manage driver profiles and vehicle types |
| 🔍 **Smart Filtering** | Drivers can filter loads by their vehicle type |
| 🚦 **Load Status** | Track loads: `Pending` → `Assigned` → `In Progress` → `Delivered` |
| 📱 **PWA Support** | Install the app on your phone for native-like experience |
| 💬 **SMS Notifications** | Real-time SMS alerts for new loads and accepted assignments |
| 📊 **Dashboard** | Admin dashboard with statistics and recent activity |

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Backend | Django, Python |
| Database | SQLite / PostgreSQL |
| Frontend | HTML5, CSS3, Bootstrap, JavaScript |
| SMS Service | SMS.ir API |
| Deployment | Chabokan Cloud |
| Version Control | Git & GitHub |

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- pip
- Virtual environment (recommended)

### Installation Steps

```bash
# 1. Clone the repository
git clone https://github.com/MohammadMHB/Barsu.git
cd Barsu

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Create .env file
cat > .env << EOF
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
SMS_IR_API_KEY=your-api-key
SMS_IR_LINE_NUMBER=your-line-number
ADMIN_PHONE_NUMBER=admin-phone-number
EOF

# 5. Run migrations
python manage.py makemigrations loads
python manage.py migrate

# 6. Create superuser
python manage.py createsuperuser

# 7. Collect static files
python manage.py collectstatic --noinput

# 8. Run server
python manage.py runserver
```

---

## 👥 User Roles

### 👑 Admin Panel
- Access at `/admin/dashboard/`
- Create, edit, delete cargo loads
- Manage drivers (add, edit, activate/deactivate)
- View all loads and their statuses
- View statistics dashboard

### 🚛 Driver Panel
- Access at `/driver/dashboard/`
- View available loads (filter by vehicle type)
- Accept loads
- View accepted loads in "My Loads"
- Receive SMS notifications

---

## 📱 PWA Installation

### Android (Chrome)
1. Open `https://barsu.ir` in Chrome
2. Tap the three-dot menu ⋮
3. Select **"Install app"** or **"Add to Home screen"**
4. Confirm installation

### iOS (Safari)
1. Open `https://barsu.ir` in Safari
2. Tap the **Share** button ⬆️
3. Select **"Add to Home Screen"**
4. Tap **"Add"**

---

## 🔧 Environment Variables

| Variable | Description |
|----------|-------------|
| `SECRET_KEY` | Django secret key (required) |
| `DEBUG` | Debug mode (True/False) |
| `ALLOWED_HOSTS` | Comma-separated allowed hosts |
| `SMS_IR_API_KEY` | SMS.ir API key |
| `SMS_IR_LINE_NUMBER` | SMS.ir line number |
| `ADMIN_PHONE_NUMBER` | Admin phone for notifications |

---

## 📁 Project Structure

```
Barsu/
├── loads/                  # Main application
│   ├── templates/          # HTML templates
│   ├── static/             # CSS, JS, icons
│   ├── models.py           # Database models
│   ├── views.py            # Application logic
│   ├── forms.py            # Form definitions
│   ├── urls.py             # URL routing
│   └── kavenegar_sms.py    # SMS integration
├── myproject/              # Project configuration
│   ├── settings.py         # Django settings
│   └── urls.py             # Main URL config
├── static/                 # Global static files
├── templates/              # Global templates
├── manage.py               # Django CLI
├── requirements.txt        # Dependencies
├── Procfile                # Deployment config
├── runtime.txt             # Python version
└── README.md               # This file
```

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

- **Developer:** Mohammad MHB
- **GitHub:** [MohammadMHB](https://github.com/MohammadMHB)
- **Project:** [https://github.com/MohammadMHB/Barsu](https://github.com/MohammadMHB/Barsu)
- **Live Demo:** [https://barsu.ir](https://barsu.ir)

---

## 🙏 Acknowledgements

- [Django](https://www.djangoproject.com/) - Web framework
- [SMS.ir](https://sms.ir/) - SMS service
- [Bootstrap](https://getbootstrap.com/) - UI framework
- [Font Awesome](https://fontawesome.com/) - Icons
- [Chabokan](https://chabokan.net/) - Hosting platform

---

> Built with ❤️ for the logistics industry in Iran 🇮🇷
```

## 3. ذخیره و کامیت کن

```bash
# ذخیره فایل (Ctrl+X, Y, Enter در nano)

# اضافه کردن به گیت
git add README.md

# کامیت
git commit -m "Add professional README.md"

# پوش به گیت‌هاب
git push origin main
```
