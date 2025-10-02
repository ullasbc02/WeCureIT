# 🏥 WeCureIT

A modern healthcare platform built with **Next.js 15** and **TypeScript**.

## 🚀 Quick Setup & Installation

### Prerequisites
- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **Git**

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/ullasbc02/WeCureIT.git
cd WeCureIT
```

### 2️⃣ Install Dependencies
```bash
cd frontend
npm install
```

### 3️⃣ Environment Setup (Optional)
1. Copy the environment file:
   ```bash
   cp .env.example .env
   ```

2. Update the `.env` file with your configuration as needed.

## 🏃‍♂️ Running the Application

### Development Mode
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build
```bash
npm run build
npm start
```

## 🛠️ Tech Stack

- **Frontend:** Next.js 15, TypeScript, React 19, Tailwind CSS
- **Backend:** Java Spring Boot (to be done)
- **Authentication:** NextAuth.js (available)
- **Styling:** Tailwind CSS

## 📁 Project Structure

```
WeCureIT/
├── src/
│   └── app/                 # Next.js 15 App Router
│       ├── globals.css     # Global styles
│       ├── layout.tsx      # Root layout
│       └── page.tsx        # Home page
├── public/                 # Static assets
├── .env                    # Environment variables (optional)
└── README.md
```

## 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm start            # Start production server
npm run lint         # Run ESLint
```

## 🚨 Common Issues & Solutions

### 1. Module Not Found Error
**Solution:** Make sure you've run `npm install`

### 2. Port Already in Use
```bash
Error: Port 3000 is already in use
```
**Solution:** Kill the process using port 3000 or use a different port

## 🔐 Security Notes

- Never commit `.env` files to version control
- Use environment variables for sensitive data
- Keep API keys and secrets secure

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

If you encounter any issues:
1. Check the [Common Issues](#-common-issues--solutions) section
2. Open an issue on GitHub

---

**Happy Coding! 🎉**
