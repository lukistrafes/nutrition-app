# Clinical Nutrition Catalog App

A comprehensive offline web application for managing nutritional supplements in a hospital pharmacy setting.

## Features

### 🔐 User Authentication
- **Two user roles:**
  - **Pharmacy (farmacia)** - Administrator with full CRUD permissions
  - **Nutrition (nutricion)** - Viewer with read-only access

### 📦 Product Categories
1. **Oral Supplements (SON)** - Standard and specialized formulas for oral intake
2. **Enteral Nutrition (NE)** - Tube feeding solutions
3. **Parenteral Nutrition (NP)** - IV administration nutrients

### ✨ Administrator Capabilities (farmacia user)
- Add new products to any category
- Edit existing product details
- Delete products
- All changes saved locally in browser

### 👁️ Viewer Capabilities (nutricion user)
- Browse all products across all categories
- View detailed product information
- Search and filter products
- Cannot add, edit, or delete products

## Login Credentials

### Administrator Account
- **Username:** `farmacia`
- **Password:** `admin123`
- **Permissions:** Full CRUD access

### Viewer Account
- **Username:** `nutricion`
- **Password:** `user123`
- **Permissions:** Read-only access

## How to Use

### Initial Setup
1. Open `login.html` in any modern web browser
2. Enter credentials for either the pharmacy or nutrition user
3. Click "Sign In" to access the system

### Navigation
- After login, you'll see the main page with three product categories
- Click "View Category" on any card to browse that category's products
- Use the navigation menu to switch between categories
- Click "Home" to return to the main page
- Click "Logout" to sign out

### Managing Products (Admin Only)
1. Navigate to any category page (Oral, Enteral, or Parenteral)
2. Click the "Add Product" button in the header
3. Fill in the product details:
   - Product Name
   - Manufacturer
   - Description
   - Energy (kcal/ml)
   - Protein (g)
   - Volume (ml)
   - Fiber (optional for Oral/Enteral) or Osmolarity (optional for Parenteral)
   - Stock Status
   - Image URL (optional)
4. Click "Save Product"

### Editing Products (Admin Only)
1. Hover over any product card
2. Click the edit icon (pencil) that appears
3. Modify the details
4. Click "Save Product"

### Deleting Products (Admin Only)
1. Hover over any product card
2. Click the delete icon (trash) that appears
3. Confirm the deletion

## Data Storage

### Offline Operation
- All data is stored in the browser's localStorage
- No internet connection required after initial page load
- Data persists between sessions on the same computer/browser

### Data Persistence
- **Oral Products:** Stored in `localStorage` key: `oralProducts`
- **Enteral Products:** Stored in `localStorage` key: `enteralProducts`
- **Parenteral Products:** Stored in `localStorage` key: `parenteralProducts`
- **User Session:** Stored in `sessionStorage` key: `currentUser`

### Important Notes
- ⚠️ Data is stored per browser/computer - changes on one device won't sync to others
- ⚠️ Clearing browser data will delete all products
- ⚠️ Each browser on each computer will have its own independent data
- ⚠️ Session expires when browser tab is closed (user must login again)

## File Structure

```
clinical-nutrition-app/
├── login.html          # Login page
├── index.html          # Main landing page
├── oral.html           # Oral supplements catalog
├── enteral.html        # Enteral nutrition catalog
├── parenteral.html     # Parenteral nutrition catalog
└── README.md           # This file
```

## Default Products

Each category comes with sample products:

### Oral Supplements
- Ensure Plus (Abbott Nutrition)
- Glucerna 1.5 Cal (Nestlé Health Science)
- Fortisip Compact Protein (Nutricia)

### Enteral Nutrition
- Jevity 1.5 Cal (Abbott Nutrition)
- Nutrison Advanced (Nutricia)

### Parenteral Nutrition
- Kabiven Central (Fresenius Kabi)
- Clinimix E (Baxter)

## Browser Compatibility

Works with all modern browsers:
- Google Chrome (recommended)
- Mozilla Firefox
- Microsoft Edge
- Safari

## Technical Details

### Technologies Used
- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript (no frameworks)
- localStorage API for data persistence
- sessionStorage API for authentication

### No Server Required
This is a completely client-side application. Simply open the HTML files in a browser to use.

## Troubleshooting

### Can't login?
- Make sure you're using the exact credentials shown on the login page
- Usernames and passwords are case-sensitive

### Products not saving?
- Make sure you're logged in as the "farmacia" (admin) user
- Check that your browser allows localStorage
- Try using an incognito/private window to test

### Lost all products?
- Browser data was likely cleared
- Each browser/device has independent data
- Consider exporting/backing up localStorage manually if needed

## Future Enhancements (Not Included)

If you need these features, you would need a backend server:
- Multi-device synchronization
- Cloud backup
- User management
- Email notifications
- Advanced reporting
- Product history/audit logs

## Support

For questions or issues, contact your IT department or the app developer.

---

**Version:** 1.0  
**Last Updated:** February 2026  
**For:** Hospital Pharmacy Department
