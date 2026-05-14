# Restaurant Food Ordering System - Complete Setup Guide

## 🎯 Project Overview
A complete **JSP-based Restaurant Food Ordering System** with beautiful UI designs, admin panel, and Oracle 11g XE database integration.

---

## 📋 Prerequisites

### Software Requirements:
1. **JDK 8 or higher**
2. **Apache Tomcat 8.5 or higher**
3. **Oracle Database 11g Express Edition (XE)**
4. **Oracle JDBC Driver (ojdbc6.jar)**
5. **Eclipse IDE / NetBeans / IntelliJ IDEA** (Optional)

---

## 🚀 Installation Steps

### Step 1: Install Oracle 11g XE
1. Download Oracle 11g XE from Oracle website
2. Install with default settings
3. Remember your system password
4. Default Port: **1521**
5. Default SID: **xe**

### Step 2: Create Database Schema
1. Open **SQL*Plus** or **SQL Developer**
2. Login as system user:
   ```
   Username: system
   Password: [your_password]
   ```
3. Run the complete SQL script: `database_schema.sql`
4. Verify tables created:
   ```sql
   SELECT table_name FROM user_tables;
   ```

### Step 3: Setup Tomcat Server
1. Download Apache Tomcat 8.5+
2. Extract to a folder (e.g., `C:\tomcat`)
3. Set environment variable:
   ```
   CATALINA_HOME = C:\tomcat
   ```

### Step 4: Add Oracle JDBC Driver
1. Download `ojdbc6.jar` for Oracle 11g
2. Copy to Tomcat lib folder:
   ```
   C:\tomcat\lib\ojdbc6.jar
   ```

### Step 5: Deploy JSP Project
1. Create project folder structure:
   ```
   RestaurantSystem/
   ├── index.jsp
   ├── login.jsp
   ├── register.jsp
   ├── menu.jsp
   ├── cart.jsp
   ├── orders.jsp
   ├── admin-dashboard.jsp
   ├── view-orders.jsp
   ├── add-menu.jsp
   ├── edit-menu.jsp
   ├── logout.jsp
   ├── dbconnection.jsp
   ├── header.jsp
   └── footer.jsp
   ```

2. Copy all JSP files to the project folder

3. Deploy to Tomcat:
   - **Option A**: Copy project folder to `C:\tomcat\webapps\`
   - **Option B**: Use IDE deployment feature

### Step 6: Configure Database Connection
1. Open `dbconnection.jsp`
2. Update database credentials:
   ```jsp
   String url = "jdbc:oracle:thin:@localhost:1521:xe";
   String username = "system";  // Your Oracle username
   String password = "oracle";  // Your Oracle password
   ```

---

## ▶️ Running the Application

### Start Oracle Database:
```
# Windows
sqlplus / as sysdba
startup;

# Or use Oracle Services
Services → Start OracleServiceXE
```

### Start Tomcat Server:
```
# Windows
C:\tomcat\bin\startup.bat

# Linux/Mac
./catalina.sh run
```

### Access Application:
```
http://localhost:8080/RestaurantSystem/index.jsp
```

---

## 👤 Default Login Credentials

### Admin Login:
- **Email**: admin@gmail.com
- **Password**: admin123
- **Access**: Auto-redirects to Admin Dashboard

### User Registration:
- Register new user with Gmail address
- Only `@gmail.com` addresses allowed
- Email must be unique

---

## 🎨 Project Features

### User Module:
✅ Beautiful landing page with animated gradients  
✅ Gmail-only registration system  
✅ Single login page (auto role detection)  
✅ Browse menu with modern card layout  
✅ Add items to cart  
✅ Update cart quantities  
✅ Place orders  
✅ View order history with status tracking  

### Admin Module:
✅ Luxury dark theme admin dashboard  
✅ Live order statistics (Total, Pending, Preparing, Delivered)  
✅ Real-time order count updates  
✅ View all user orders  
✅ Update order status (Pending → Preparing → Delivered)  
✅ Add new menu items  
✅ Edit existing menu items  
✅ Delete menu items  

### Key Functionality:
✅ **Instant Order Visibility**: User orders appear immediately in admin panel  
✅ **Auto Status Detection**: Orders default to "Pending" status  
✅ **Live Dashboard Counts**: Refresh to see updated statistics  
✅ **Session-based Authentication**: Secure login system  
✅ **No External CSS**: All styles in JSP files  

---

## 📂 Database Tables

| Table Name | Description |
|------------|-------------|
| `users` | User registration data |
| `admin` | Admin credentials |
| `menu` | Food items catalog |
| `cart` | User shopping cart |
| `orders` | Completed orders with status |

---

## 🎯 Order Flow

1. **User** adds items to cart from menu
2. **User** places order from cart
3. **Order** saved with status = "Pending"
4. **Admin** sees new order immediately in dashboard
5. **Admin** updates status: Pending → Preparing → Delivered
6. **User** sees updated status in "My Orders"

---

## 🔧 Troubleshooting

### Database Connection Error:
```
Check:
1. Oracle service is running
2. Database credentials in dbconnection.jsp
3. ojdbc6.jar is in Tomcat lib folder
```

### Page Not Found (404):
```
Check:
1. Tomcat is running
2. Project deployed correctly
3. URL path is correct
```

### Session Issues:
```
Solution:
- Clear browser cookies
- Restart Tomcat server
```

---

## 📱 Browser Compatibility
- ✅ Chrome (Recommended)
- ✅ Firefox
- ✅ Edge
- ✅ Safari

---

## 🎓 Academic Project Ready
This project is **complete and ready** for:
- Final year projects
- Academic submissions
- Portfolio demonstration
- Learning JSP + Oracle integration

---

## 📞 Support Notes

### Default Ports:
- Tomcat: 8080
- Oracle: 1521

### Important Files:
- `dbconnection.jsp` → Database configuration
- `login.jsp` → Single login for admin & user
- `admin-dashboard.jsp` → Admin statistics

---

## ✨ Unique Features

1. **Animated Landing Page** - Premium gradient animations
2. **Dual UI Themes** - User (Purple/Pink) vs Admin (Dark/Gold)
3. **Auto Role Detection** - One login page for all
4. **Real-time Updates** - Orders visible instantly
5. **Modern Card Layouts** - Professional design

---

## 🎨 Color Schemes

### User Interface:
- Primary: Purple/Pink gradients
- Accent: #f5576c

### Admin Interface:
- Primary: Dark theme (#0f0f1e)
- Accent: Gold (#ffd700)

---

## 📄 License
Academic/Educational Use Only

---

## 🙏 Credits
Created for academic demonstration purposes using:
- JSP (JavaServer Pages)
- Oracle 11g XE Database
- Bootstrap 5.3
- Font Awesome 6.4

---

**End of Documentation** 🎉
