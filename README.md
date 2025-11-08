# 🍛 Hotel Food Management - South Indian Cuisine

A beautiful, modern React application for managing hotel food items with a focus on South Indian cuisine. Features full CRUD operations, online image integration, and a responsive design that works on desktop and mobile devices.

## ✨ Features

- **CRUD Operations**: Create, Read, Update, and Delete food items
- **South Indian Cuisine**: Pre-loaded with popular South Indian dishes
- **Online Images**: Automatic image fetching from Unsplash
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Search & Filter**: Find food items by name or category
- **Availability Toggle**: Mark items as available/unavailable
- **Local Storage**: Data persists in browser local storage
- **Modern UI**: Beautiful gradient design with glassmorphism effects

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd hotel-food-management
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:3000`

## 📦 Building for Production

To build the application for production:

```bash
npm run build
```

The built files will be in the `dist` directory. You can preview the production build with:

```bash
npm run preview
```

## 📱 Mobile Usage

The application is fully responsive and works great on mobile devices. You can:

1. **Deploy to GitHub Pages**: 
   - See detailed instructions in [DEPLOYMENT.md](./DEPLOYMENT.md)
   - GitHub Actions workflow is included for automatic deployment
   - Build the app: `npm run build`
   - Deploy the `dist` folder to GitHub Pages

2. **Use Locally on Mobile**:
   - Make sure your computer and mobile are on the same network
   - Start the dev server: `npm run dev`
   - Find your local IP address (e.g., `192.168.1.100`)
   - Access from mobile: `http://192.168.1.100:3000`

3. **Deploy to Vercel/Netlify**:
   - See detailed instructions in [DEPLOYMENT.md](./DEPLOYMENT.md)
   - Connect your GitHub repository
   - Deploy automatically on push

## 🎨 Features in Detail

### Food Management
- Add new food items with name, category, price, description, and image
- Edit existing food items
- Delete food items with confirmation
- Toggle availability status
- Search food items by name or description
- Filter by category (Breakfast, Lunch, Dinner, Snacks, etc.)

### Categories
- Breakfast
- Lunch
- Dinner
- Snacks
- Curry
- Soup
- Main Course
- Dessert

### Pre-loaded South Indian Foods
- Dosa
- Idli
- Sambar
- Biryani
- Vada
- Rasam

## 🛠️ Technologies Used

- **React 18**: Modern React with hooks
- **React Router**: Navigation and routing
- **Vite**: Fast build tool and dev server
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Beautiful icon library
- **Local Storage**: Client-side data persistence

## 📝 Project Structure

```
hotel-food-management/
├── src/
│   ├── components/
│   │   ├── FoodList.jsx      # Main food listing component
│   │   └── FoodForm.jsx       # Add/Edit food form
│   ├── App.jsx                # Main app component with routing
│   ├── main.jsx               # React entry point
│   └── index.css              # Global styles
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── README.md
```

## 🎯 Usage

1. **View Menu**: Browse all food items on the home page
2. **Add Food**: Click "Add Food" button to create a new item
3. **Edit Food**: Click the edit icon on any food card
4. **Delete Food**: Click the delete icon (trash) on any food card
5. **Toggle Availability**: Click "Mark Available/Unavailable" button
6. **Search**: Use the search bar to find specific items
7. **Filter**: Use the category dropdown to filter by category

## 🔧 Customization

### Adding More Categories
Edit `src/components/FoodForm.jsx` and add to the `categories` array.

### Changing Colors
Edit `tailwind.config.js` to customize the color scheme.

### Changing Images
The app uses Unsplash images. You can:
- Enter custom image URLs in the form
- Click "Random" to get a random food image
- Modify the image URLs in the code

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📧 Support

For support, please open an issue in the GitHub repository.

---

Made with ❤️ for South Indian food lovers!

