# 🌱 GreenFork - Food Delivery Carbon Footprint Tracker

A comprehensive web application that helps users track, analyze, and reduce their carbon footprint from online food deliveries. GreenFork provides AI-powered recommendations to make more environmentally conscious food delivery choices.

## 🎯 Mission

Food deliveries contribute significantly to carbon emissions through transportation, packaging, and food production. GreenFork aims to raise awareness and empower users to make more sustainable choices by providing detailed carbon footprint analysis and personalized AI recommendations.

## ✨ Features

### 📊 Carbon Footprint Tracking
- **Multi-platform Support**: Import orders from Swiggy and Zomato
- **Comprehensive Analysis**: Track transport, packaging, and food-related emissions
- **Real-time Calculations**: Advanced emission factor algorithms for accurate carbon footprint estimation
- **Historical Data**: View trends and patterns in your delivery habits

### 🤖 AI-Powered Recommendations
- **Personalized Suggestions**: AI analyzes your order history to provide tailored recommendations
- **Item-level Analysis**: Get specific recommendations for each food item in your orders
- **Overall Strategy**: Receive comprehensive tips to reduce your carbon footprint
- **Smart Caching**: Optimized performance with intelligent caching of AI recommendations

### 📈 Advanced Analytics
- **Emission Breakdown**: Detailed analysis of transport, packaging, and food emissions
- **Platform Comparison**: Compare carbon footprints across different delivery platforms
- **Trend Analysis**: Track your progress over time with interactive charts
- **Environmental Impact**: See your footprint in relatable terms (trees, car days, etc.)

### 🎨 Beautiful Dashboard
- **Modern UI**: Clean, responsive design with Tailwind CSS
- **Interactive Charts**: Visualize your data with Chart.js
- **Mobile Responsive**: Optimized for all device sizes
- **Real-time Updates**: Live data refresh and notifications


## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB
- OpenAI API key (for AI recommendations)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/anshaneja5/GreenFork.git
   cd GreenFork
   ```

2. **Set up the backend**
   ```bash
   cd backend
   npm install
   ```

3. **Configure environment variables**
   Create a `.env` file in the backend directory:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   OPENAI_API_KEY=your_openai_api_key
   PORT=5000
   ```

4. **Set up the frontend**
   ```bash
   cd ../frontend
   npm install
   ```

5. **Start the development servers**
   ```bash
   # Backend (from backend directory)
   npm run dev
   
   # Frontend (from frontend directory)
   npm run dev
   ```

## 📱 How to Use

### 1. Account Setup
- Register with your email and password
- Complete your profile with delivery preferences

### 2. Import Your Orders
- **Swiggy**: Follow the step-by-step instructions to extract your order data
- **Zomato**: Follow the step-by-step instructions to extract your order data
- **Manual Entry**: Add orders manually with restaurant and item details

### 3. View Your Carbon Footprint
- **Dashboard**: Overview of your total emissions and recent orders
- **Insights**: Detailed charts and analysis of your carbon footprint
- **Trends**: Track your progress over time

### 4. Get AI Recommendations
- **Order-specific**: AI analyzes each order for improvement opportunities
- **Overall Strategy**: Personalized tips based on your ordering patterns
- **Actionable Tips**: Specific suggestions to reduce your carbon footprint


### AI Recommendation System
- **GPT-3.5-turbo**: Powered by OpenAI for intelligent analysis
- **Multi-level Caching**: Database and memory caching for optimal performance
- **Personalized Analysis**: Considers your specific ordering patterns
- **Fallback System**: Graceful degradation when AI is unavailable

### Data Security
- **JWT Authentication**: Secure user sessions
- **Password Hashing**: bcrypt for secure password storage
- **Rate Limiting**: Protection against abuse
- **Input Validation**: Comprehensive data validation

## 🌍 Environmental Impact

### Carbon Footprint Reduction Strategies
1. **Order from nearby restaurants** - Reduces transport emissions
2. **Choose vegetarian options** - Lower food production emissions
3. **Combine orders** - Reduces packaging and delivery trips
4. **Opt for eco-friendly packaging** - Minimize waste
5. **Support sustainable restaurants** - Encourage green practices

### Impact Metrics
- **Trees Equivalent**: Your emissions in terms of trees needed to absorb CO₂
- **Car Days**: Equivalent days of car emissions
- **Smartphone Charges**: Number of phone charges equivalent
- **Light Bulb Hours**: Hours of light bulb usage equivalent

## 🛠️ Development

### Database Schema

#### User Model
```javascript
{
  name: String,
  email: String,
  password: String,
  platformCredentials: Object,
  preferences: Object
}
```

#### Order Model
```javascript
{
  user: ObjectId,
  platform: String,
  orderId: String,
  restaurantName: String,
  items: Array,
  emissionData: Object
}
```

#### Emission Model
```javascript
{
  user: ObjectId,
  order: ObjectId,
  transportEmission: Number,
  packagingEmission: Number,
  foodEmission: Number,
  totalEmission: Number,
  factors: Object
}
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **OpenAI** for providing the AI recommendation system
- **Chart.js** for beautiful data visualization
- **Tailwind CSS** for the modern UI design
- **MongoDB** for reliable data storage

## 📞 Support

If you have any questions or need help, please:
- Open an issue on GitHub
- Check our [FAQ](FAQ.md)
- Contact us at anshanejaa@gmail.com

---

**Made with ❤️ for a greener planet**

*Track your food delivery carbon footprint and make a difference, one order at a time.* 
