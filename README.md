# 🏥 WeCureIT

A modern healthcare platform built with **Next.js 15**, **TypeScript**, **Prisma**, and **Supabase**.

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
npm install
```

### 3️⃣ Environment Setup
1. Copy the environment file:
   ```bash
   cp .env.example .env
   ```

2. Update the `.env` file with your Supabase credentials:
   ```env
   # Connect to Supabase via connection pooling
   DATABASE_URL="postgresql://postgres.[PROJECT_REF]:[YOUR_PASSWORD]@aws-[REGION].pooler.supabase.com:6543/postgres?pgbouncer=true"
   
   # Direct connection to the database (for migrations)
   DIRECT_URL="postgresql://postgres.[PROJECT_REF]:[YOUR_PASSWORD]@db.[PROJECT_REF].supabase.co:5432/postgres"
   ```
   
   > **Note:** Replace `[PROJECT_REF]`, `[YOUR_PASSWORD]`, and `[REGION]` with your actual Supabase project details.

### 4️⃣ Database Setup
```bash
# Generate Prisma client
npx prisma generate

# Push schema to database (if needed)
npx prisma db push
```

### 5️⃣ Test Database Connection
```bash
node test-database.js
```
You should see your admin users data if the connection is successful.

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
- **Backend:** Next.js API Routes
- **Database:** PostgreSQL (Supabase)
- **ORM:** Prisma
- **Authentication:** NextAuth.js (configured)
- **Styling:** Tailwind CSS

## 📁 Project Structure

```
WeCureIT/
├── src/
│   ├── app/                 # Next.js 15 App Router
│   │   ├── api/            # API endpoints
│   │   ├── globals.css     # Global styles
│   │   ├── layout.tsx      # Root layout
│   │   └── page.tsx        # Home page
│   └── generated/          # Generated Prisma client
├── prisma/
│   └── schema.prisma       # Database schema
├── public/                 # Static assets
├── .env                    # Environment variables
├── test-database.js        # Database connection test
└── README.md
```

## 🗄️ Database Schema

The application uses the following main table:

### `admin_users`
- `id` (BigInt, Auto-increment)
- `name` (String)
- `email` (String, Unique)

## 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm start            # Start production server
npm run lint         # Run ESLint
npx prisma studio    # Open Prisma Studio (database GUI)
npx prisma generate  # Generate Prisma client
npx prisma db push   # Push schema changes to database
```

## 🌐 API Endpoints

### Health Check
- **GET** `/api/health` - Check backend status

### Database Test
- **GET** `/api/db-test` - Test database connection

### Admin Users (Example)
- **GET** `/api/admin-users` - Get all users
- **POST** `/api/admin-users` - Create new user

## 📝 Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `DATABASE_URL` | Supabase connection string (pooled) | `postgresql://postgres...` |
| `DIRECT_URL` | Direct database connection (for migrations) | `postgresql://postgres...` |

## 🔍 Testing Database Connection

Run the test script to verify your database connection:

```bash
node test-database.js
```

Expected output:
```javascript
[
  { id: 1001n, name: 'William Blade', email: 'william.blade@gmail.com' },
  { id: 1002n, name: 'Alice John', email: 'alice.john@gmail.com' },
  { id: 1003n, name: 'Bob Marley', email: 'bob.marley@gmail.com' }
]
```

## 🚨 Common Issues & Solutions

### 1. Prisma Client Not Generated
```bash
Error: @prisma/client did not initialize yet
```
**Solution:** Run `npx prisma generate`

### 2. Database Connection Failed
```bash
Error: Can't reach database server
```
**Solution:** 
- Check your `.env` file
- Verify Supabase credentials
- Ensure your IP is whitelisted in Supabase

### 3. Module Not Found Error
**Solution:** Make sure you've run `npm install`

## 🔐 Security Notes

- Never commit `.env` files to version control
- Use environment variables for all sensitive data
- Keep your Supabase credentials secure
- Regularly rotate database passwords

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
2. Run the database test: `node test-database.js`
3. Open an issue on GitHub

---

**Happy Coding! 🎉**
