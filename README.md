# DevOps Bootcamp - Frontend Application

This repository contains the frontend application for the CloudMart e-commerce platform, developed as part of the DevOps Bootcamp project. This React-based application provides a modern user interface for a complete online shopping experience with AI integration.

## Features

- Interactive product catalog with search functionality
- Shopping cart with order placement
- User profile management
- Order history and tracking
- Admin dashboard for product and order management
- AI-powered customer support chat interface
- Embedded AI assistant for product recommendations

## Technology Stack

- **Framework**: React 18 with Vite
- **Routing**: React Router v6
- **Styling**: TailwindCSS
- **HTTP Client**: Axios
- **UI Icons**: Lucide React
- **Development**: ESLint, Vite dev server
- **Containerization**: Docker/Kubernetes ready

## Prerequisites

- Node.js (v14.x or later)
- npm (v6.x or later)
- Git

## Installation and Setup

1. Clone the repository:
   ```
   git clone https://github.com/beastmp/msc-devops-bootcamp-frontend.git
   cd msc-devops-bootcamp-frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up environment variables:
   - Create or modify the `.env` file in the root directory
   - Configure the API endpoint:
     ```
     VITE_API_BASE_URL=http://localhost:5000/api
     ```

4. Start the development server:
   ```
   npm run dev
   ```

The application should now be running on [http://localhost:5173](http://localhost:5173).

## Available Scripts

- `npm run dev` - Runs the app in development mode with hot reloading
- `npm run build` - Builds the app for production
- `npm run lint` - Runs ESLint to check code quality
- `npm run preview` - Previews the production build locally

## Project Structure

```
src/
├── components/           # UI components organized by feature
│   ├── AboutPage/        # About page component
│   ├── AdminPage/        # Admin product management interface
│   ├── AIAssistant/      # Floating AI chat component
│   ├── CartPage/         # Shopping cart interface
│   ├── Footer/           # Site footer component
│   ├── Header/           # Site header component
│   ├── LoadingSpinner/   # Loading indicator
│   ├── MainPage/         # Homepage with product catalog
│   ├── OrdersPage/       # Admin order management
│   ├── SupportPage/      # Customer support chat interface
│   ├── UserOrdersPage/   # User's order history
│   └── UserProfilePage/  # User profile management
├── config/               # Application configuration
│   └── axiosConfig.js    # API client configuration
├── utils/                # Utility functions
│   ├── cartUtils.js      # Shopping cart management
│   └── userUtils.js      # User management
├── App.jsx               # Main application component with routes
└── main.jsx              # Application entry point
```

## Key Features

### Product Catalog
- Display of all available products
- Product search functionality
- Add to cart capability

### Shopping Cart
- View and manage items in cart
- Update item quantities
- Checkout process with order confirmation

### User Management
- User profile creation and editing
- Order history viewing
- Streamlined anonymous user experience

### Admin Features
- Product management (add, edit, delete)
- Order management with status updates
- Order details viewing

### AI Integration
- Floating AI assistant for customer inquiries
- Support chat with conversation history
- AI-powered product recommendations

## API Integration

The frontend communicates with the backend API using Axios. The base URL is configured via environment variables:

```javascript
baseURL: import.meta.env.VITE_API_BASE_URL || 'http://localhost:5000/api'
```

## Deployment

### Docker and Kubernetes

The project includes Kubernetes deployment configuration in `cloudmart-frontend.yaml`:

```bash
# Build the Docker image
docker build -t cloudmart-frontend .

# Apply the Kubernetes configuration
kubectl apply -f cloudmart-frontend.yaml
```

### Environment Configuration

For production deployment, ensure the correct `VITE_API_BASE_URL` is set to the backend API endpoint.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Related Repositories

- [DevOps Bootcamp - Backend](https://github.com/beastmp/msc-devops-bootcamp-backend)
- [DevOps Bootcamp - Infrastructure](https://github.com/beastmp/msc-devops-bootcamp-infrastructure)
- [DevOps Bootcamp - Kubernetes](https://github.com/beastmp/msc-devops-bootcamp-kubernetes)
