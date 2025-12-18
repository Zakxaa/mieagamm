# Food Ordering and Tracking System

A complete food ordering and delivery tracking web application powered by Google Sheets as the database and Google Apps Script as the backend API. No traditional server or database required!

![Project Status](https://img.shields.io/badge/status-ready-success)
![License](https://img.shields.io/badge/license-MIT-blue)

## 🌟 Features

### Customer Features
- 📱 **Browse Menu** - Beautiful, categorized menu with images and descriptions
- 🛒 **Shopping Cart** - Add/remove items with quantity controls
- 📝 **Easy Ordering** - Simple checkout form with no authentication required
- 📍 **Order Tracking** - Real-time order status tracking with visual progress
- 💾 **Cart Persistence** - Cart saved in browser localStorage
- 📲 **Responsive Design** - Works perfectly on mobile, tablet, and desktop

### Admin Features
- 🔐 **Password Protected** - Secure admin access with authentication
- 📊 **Order Management** - View all orders with filtering by status
- ✏️ **Status Updates** - Update order status in real-time
- 🍽️ **Menu Management** - Add, edit, delete menu items
- ⚙️ **Settings** - Customize restaurant name, contact info, and branding
- 🔄 **Auto-Refresh** - Orders automatically refresh every 30 seconds

### Technical Features
- ☁️ **No Server Required** - Uses Google Sheets as database
- 🚀 **Free Hosting** - Deploy on GitHub Pages or any static hosting
- 🎨 **Modern Design** - Glassmorphism effects, gradients, smooth animations
- 🌙 **Dark Theme** - Beautiful dark mode interface
- ⚡ **Fast & Lightweight** - Pure JavaScript, no heavy frameworks

## 📁 Project Structure

```
food-ordering-app/
├── index.html          # Customer menu page
├── track.html          # Order tracking page
├── admin.html          # Admin panel (password protected)
├── styles.css          # Main stylesheet
├── admin.css           # Admin panel styles
├── app.js              # Customer app JavaScript
├── track.js            # Order tracking JavaScript
├── admin.js            # Admin panel JavaScript
├── Code.gs             # Google Apps Script backend
├── README.md           # This file
└── SETUP.md            # Detailed setup instructions
```

## 🚀 Quick Start

### Prerequisites
- Google Account
- Web browser
- Basic understanding of copy-paste 😊

### Setup (15-20 minutes)

1. **Create Google Sheet Database**
   - Follow instructions in [SETUP.md](SETUP.md)
   - Create 4 sheets: Config, Menu, Orders, OrderItems

2. **Deploy Google Apps Script**
   - Copy `Code.gs` to Google Apps Script
   - Deploy as web app
   - Copy the deployment URL

3. **Configure Web App**
   - Update `API_URL` in `app.js`, `track.js`, and `admin.js`
   - Replace with your Apps Script URL

4. **Set Admin Password**
   - In Google Sheet Config tab, set `admin_password` value

5. **Deploy Website**
   - Upload all HTML/CSS/JS files to GitHub Pages
   - Or use any static hosting service

**Full setup guide:** [SETUP.md](SETUP.md)

## 🎯 Usage

### For Customers
1. Visit your website (e.g., `username.github.io/food-ordering-app`)
2. Browse menu and add items to cart
3. Click checkout and enter delivery details
4. Receive order ID and track order status

### For Admins
1. Visit `admin.html`
2. Enter admin password (set in Google Sheet)
3. View and manage orders
4. Update order status
5. Manage menu items and settings

## 🖼️ Screenshots

### Customer Interface
- **Menu Page** - Beautiful grid layout with categories
- **Shopping Cart** - Smooth sidebar with quantity controls
- **Order Tracking** - Visual status progress with order details

### Admin Panel
- **Login Screen** - Password-protected access
- **Orders Dashboard** - Table view with filters
- **Menu Management** - Add/edit menu items
- **Settings** - Customize restaurant info

## 🛠️ Technology Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Backend:** Google Apps Script
- **Database:** Google Sheets
- **Hosting:** GitHub Pages (or any static hosting)
- **Design:** Inter font, CSS gradients, Flexbox/Grid

## 📊 Database Schema

### Config Sheet
- Restaurant settings (name, phone, address, logo, admin password)

### Menu Sheet
- id, name, description, price, category, image_url, available

### Orders Sheet
- order_id, order_date, customer info, items (JSON), total, status, notes

### OrderItems Sheet
- order_id, item_id, item_name, quantity, price

## 🔧 Configuration

### Update API URL
In all JS files, replace:
```javascript
API_URL: 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE'
```

### Set Admin Password
In Google Sheet Config tab:
```
key: admin_password
value: your_secure_password
```

### Customize Branding
Edit Config sheet or use Admin Settings panel to update:
- Restaurant name
- Logo URL
- Contact information
- Colors (in styles.css)

## 🎨 Customization

### Change Colors
Edit `styles.css` CSS variables:
```css
:root {
    --primary-color: #ff6b35;
    --secondary-color: #004e89;
    --accent-color: #1a8fe3;
}
```

### Add Menu Categories
Update category options in:
- `admin.html` (select dropdown)
- `index.html` (category filter buttons)

### Modify Order Statuses
Edit status flow in:
- `Code.gs` (backend validation)
- `admin.html` (status select)
- `track.html` (progress steps)

## 🔒 Security Notes

⚠️ **Current Limitations:**
- Admin password stored in plain text in Google Sheet
- Simple token-based authentication (not JWT)
- No rate limiting on API endpoints
- Customer data visible to anyone with order ID

✅ **For Production:**
- Consider implementing Google Sign-In
- Add HTTPS enforcement
- Implement proper session management
- Add rate limiting in Apps Script
- Encrypt sensitive data

## 📈 Limitations

- **Google Apps Script Quotas:**
  - 6 minutes max execution time
  - 20,000 URL fetches/day
  - Rate limiting applies

- **Scalability:**
  - Suitable for small to medium traffic
  - Not recommended for high-volume operations
  - Google Sheets has row limits (~5M cells)

## 🤝 Contributing

This is a complete, working system! Feel free to:
- Add new features
- Improve the UI/UX
- Enhance security
- Optimize performance
- Add payment integration
- Implement notifications (email/SMS)

## 📝 License

MIT License - feel free to use for personal or commercial projects!

## 🆘 Support

Having issues? Check:
1. [SETUP.md](SETUP.md) for detailed setup instructions
2. Browser console (F12) for JavaScript errors
3. Google Apps Script logs for backend errors
4. Verify API_URL is correctly configured
5. Check Google Sheet permissions (Anyone with link)

## 🎉 Credits

Built with modern web technologies and powered by Google's free infrastructure. Perfect for small restaurants, food trucks, or learning web development!

---

**Made with ❤️ for the food delivery revolution!** 🍕🚀
