# VoltRide - E-Bike Business Website

A modern, responsive e-bike business website built with Next.js and Tailwind CSS, featuring a complete e-commerce experience for electric bicycles, accessories, and services.

## 🚀 Features

- **Product Catalog**: Browse VoltRide Urban, Sport, and Cargo e-bikes
- **E-commerce Integration**: Complete shopping cart and checkout system
- **Services Section**: Maintenance, warranty, delivery, and support services
- **Mobile App Integration**: Connect with VoltRide mobile app for GPS tracking and analytics
- **Cycle-to-Work Calculator**: Calculate savings for workplace cycling schemes
- **Responsive Design**: Optimized for all devices and screen sizes
- **Modern UI**: Beautiful gradient backgrounds with glassmorphism effects

## 🛠️ Tech Stack

- **Frontend**: Next.js 13+ with App Router
- **Styling**: Tailwind CSS
- **Deployment**: Vercel
- **UI Components**: Custom React components
- **Payment Processing**: Integrated checkout system

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v18 or higher)
- npm or yarn package manager
- Modern web browser

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd voltride-website
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_key
   STRIPE_SECRET_KEY=your_stripe_secret
   NEXT_PUBLIC_API_URL=your_api_endpoint
   ```

4. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000` to see the website

## 🎯 Usage

### Browse Products

1. **E-Bikes Section**
   - View VoltRide Urban ($2,499) - Perfect for daily commuting
   - VoltRide Sport ($2,899) - High-performance for modern riders
   - VoltRide Cargo ($3,299) - Built for load carrying

2. **Accessories**
   - Premium helmets, cargo baskets, phone mounts
   - Security locks, pannier bags, extra batteries
   - All accessories have "Add to Cart" functionality

3. **Services**
   - Maintenance & Repair with professional technicians
   - Extended warranty coverage
   - Home delivery and setup
   - 24/7 customer support

### Mobile App Features

- **GPS Tracking**: Real-time location tracking
- **Performance Analytics**: Monitor speed, distance, and battery
- **Smart Connectivity**: Connect with bike diagnostics
- **Route Planning**: Find optimal cycling routes

### Cycle-to-Work Benefits

- Save up to 40% on VoltRide purchases
- Tax-free employee benefit
- Reduce commute costs
- Built-in savings calculator

## 🛒 E-commerce Features

### Product Management
```typescript
// Example product structure
interface Product {
  id: string;
  name: string;
  price: number;
  category: 'ebike' | 'accessory';
  image: string;
  description: string;
  features: string[];
  deliveryTime: string;
}
```

### Cart Functionality
```typescript
const addToCart = (product: Product) => {
  // Add product to cart state
  setCart(prevCart => [...prevCart, product]);
};
```

### Checkout Process
- Order summary with itemized pricing
- Shipping information form
- Payment method selection
- Order confirmation

## 🎨 Design Features

### Color Scheme
- Primary: Blue gradient (#4F46E5 to #06B6D4)
- Background: Dynamic gradient overlay
- Cards: Glassmorphism with backdrop blur
- Text: High contrast for accessibility

### Responsive Design
- Mobile-first approach
- Tablet and desktop breakpoints
- Touch-friendly interface
- Optimized images for all devices

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your repository to Vercel
2. Configure environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Manual Deployment
```bash
npm run build
npm run start
```

## 🔐 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY` | Stripe public key for payments | Yes |
| `STRIPE_SECRET_KEY` | Stripe secret key for server-side | Yes |
| `NEXT_PUBLIC_API_URL` | Backend API endpoint | Yes |
| `NEXT_PUBLIC_APP_DOWNLOAD_URL` | Mobile app download link | No |

## 🐛 Troubleshooting

### Common Issues

1. **Cart not updating**
   - Check browser storage permissions
   - Verify cart state management
   - Clear browser cache

2. **Payment processing errors**
   - Validate Stripe keys in environment
   - Check network connectivity
   - Review payment form validation

3. **Mobile app connectivity**
   - Ensure app is installed and updated
   - Check device Bluetooth permissions
   - Verify bike is in pairing mode

4. **Build errors**
   - Clear node_modules and reinstall dependencies
   - Check Next.js version compatibility
   - Verify all environment variables are set

## 📊 Performance Metrics

- **Page Load Speed**: <2 seconds
- **Mobile Performance**: 95+ Lighthouse score
- **Accessibility**: WCAG 2.1 compliant
- **SEO Optimization**: Structured data for products

## 🔧 Customization Options

### Branding
- Update logo and colors in `tailwind.config.js`
- Modify product images in `public/images/`
- Customize typography and spacing

### Products
- Add new bike models in `utils/products.ts`
- Update pricing and specifications
- Configure delivery options

### Services
- Modify service offerings in components
- Update warranty terms and coverage
- Customize support contact information

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-bike-model`)
3. Commit your changes (`git commit -m 'Add new bike model'`)
4. Push to the branch (`git push origin feature/new-bike-model`)
5. Open a Pull Request
   
**VoltRide** - Revolutionizing urban transportation with premium electric bicycles and sustainable mobility solutions.
