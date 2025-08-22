# FSW Delivery 🍔

A modern food delivery platform built with Next.js 15, featuring restaurant menus, shopping cart functionality, and order management.

## 🚀 Features

### Core Functionality

- **Restaurant Discovery**: Browse available restaurants with their details
- **Menu Management**: View restaurant menus organized by categories
- **Shopping Cart**: Add/remove products, adjust quantities, and manage cart state
- **Order Processing**: Complete orders with customer information and consumption method
- **Order Tracking**: View order history and status by CPF (Brazilian ID)
- **Responsive Design**: Mobile-first approach with modern UI components

### Order System

- **Consumption Methods**: Choose between Takeaway and Dine-in options
- **Customer Information**: Collect name and CPF for order tracking
- **Order Status**: Track orders through PENDING → IN_PREPARATION → FINISHED states
- **Real-time Updates**: Automatic page revalidation after order creation

## 🛠️ Tech Stack

### Frontend

- **Next.js 15** - React framework with App Router
- **React 19** - Latest React version with modern features
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives
- **Lucide React** - Beautiful icon library

### Backend & Database

- **Prisma** - Type-safe database ORM
- **PostgreSQL** - Relational database
- **Next.js Server Actions** - Server-side operations

### State Management & Forms

- **React Context** - Cart state management
- **React Hook Form** - Form handling and validation
- **Zod** - Schema validation
- **React Number Format** - Input formatting

### UI Components

- **Class Variance Authority** - Component variant management
- **Tailwind Merge** - Utility class merging
- **Vaul** - Drawer component library
- **Sonner** - Toast notifications

### Development Tools

- **ESLint** - Code linting
- **Prettier** - Code formatting
- **PostCSS** - CSS processing

## 🗄️ Database Schema

The application uses a relational database with the following main entities:

- **Restaurant**: Basic restaurant information (name, slug, description, images)
- **MenuCategory**: Food categories for organizing products
- **Product**: Individual menu items with pricing and ingredients
- **Order**: Customer orders with status tracking
- **OrderProduct**: Junction table for order-product relationships

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL database
- Git

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd fsw-delivery
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Environment Setup**
   Create a `.env` file with your database connection:

   ```env
   DATABASE_URL="postgresql://username:password@localhost:5432/fsw_delivery"
   ```

4. **Database Setup**

   ```bash
   # Generate Prisma client
   npx prisma generate

   # Run migrations
   npx prisma migrate dev

   # Seed database (optional)
   npx prisma db seed
   ```

5. **Start Development Server**

   ```bash
   npm run dev
   # or
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📱 Application Structure

```
src/
├── app/                    # Next.js App Router
│   ├── [slug]/            # Dynamic restaurant routes
│   │   ├── menu/          # Restaurant menu pages
│   │   ├── orders/        # Order management
│   │   └── components/    # Restaurant-specific components
│   ├── components/        # Shared UI components
│   ├── data/             # Data fetching functions
│   ├── helpers/          # Utility functions (CPF validation, etc.)
│   └── lib/              # Database and utility configurations
```

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run postinstall` - Generate Prisma client
- `pnpm dev` - Start development server
- `pnpm build` - Build for production
- `pnpm start` - Start production server
- `pnpm lint` - Run ESLint
- `pnpm postinstall` - Generate Prisma client

## 🌟 Key Features Implementation

### Shopping Cart

- Context-based state management
- Add/remove products
- Quantity adjustment
- Real-time total calculation

### Order Management

- Server actions for order creation
- CPF validation and formatting
- Order status tracking
- Consumption method selection

### Database Operations

- Prisma ORM for type-safe queries
- Cascade deletion for data integrity
- Efficient relationship queries

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

**Giovanni Cruz** - [CRZ Web](https://crzweb.vercel.app/)

---

Made with ❤️ by [CRZ](https://crzweb.vercel.app/)
