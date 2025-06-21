# ShipCart

A comprehensive courier and delivery service management system built with Streamlit, featuring real-time package tracking, SMS notifications, interactive maps, and business analytics dashboard.

## 🚀 Features

### Customer Portal
- **📦 Package Tracking**: Track shipments using phone number or courier ID
- **📱 SMS Verification**: Secure OTP-based authentication via Twilio
- **🗺️ Interactive Maps**: Visual route tracking with Folium maps
- **📋 Order History**: Complete shipment history for registered customers
- **📞 Contact Support**: Query submission system with FAQ section
- **📊 Real-time Status**: Live delivery status updates (Pending/Delivered)

### Admin Dashboard
- **👥 Customer Management**: Add, view, and manage customer records
- **📦 Courier Management**: Create and track courier shipments
- **🔄 Status Updates**: Update delivery status with automatic SMS notifications
- **📊 Analytics Dashboard**: Comprehensive Power BI reports including:
  - Count Analysis
  - Price Analysis
  - Source & Destination Analysis
  - Delivery Status Tracking
  - Weight Analysis
  - Revenue & Profit Analysis
  - Customer Analytics
  - Forecasting

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Database**: Deta Cloud Database
- **SMS Service**: Twilio API
- **Mapping**: Folium
- **Analytics**: Power BI Embedded
- **Data Processing**: Pandas
- **Authentication**: Custom OTP system

## 📋 Prerequisites

Before running this application, make sure you have:

- Python 3.7 or higher
- Twilio account with API credentials
- Deta account and project key
- Power BI account (for analytics dashboard)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/courier-management-system.git
   cd courier-management-system
   ```

2. **Install required packages**
   ```bash
   pip install streamlit deta pandas twilio folium pillow
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory and add:
   ```env
   DETA_KEY=your_deta_project_key
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_VERIFY_SID=your_twilio_verify_service_sid
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   ```

## ⚙️ Configuration

### Deta Database Setup
The system uses three Deta bases:
- `users_db`: Customer information
- `courier_db`: Shipment details
- `queries`: Customer queries and feedback

### Twilio Configuration
1. Create a Twilio account at [twilio.com](https://twilio.com)
2. Get your Account SID and Auth Token
3. Set up a Verify Service for OTP functionality
4. Purchase a phone number for SMS sending

### Power BI Setup
1. Create Power BI reports for analytics
2. Embed the reports and update the report IDs in `manager.py`

## 🚀 Usage

### Running the Customer Portal
```bash
streamlit run main.py
```

### Running the Admin Dashboard
```bash
streamlit run manager.py
```

### Default Admin Credentials
- **Username**: admin
- **Password**: password

## 📁 Project Structure

```
courier-management-system/
│
├── main.py                 # Customer portal application
├── manager.py              # Admin dashboard application
├── loginPage.py            # Simple login page template
├── home.py                 # Twilio SMS testing script
├── sms.py                  # OTP verification script
├── maptry.py               # Map functionality testing
├── map.html                # Generated map file
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

## 🔑 Key Functions

### Customer Management
- `insert_user(customerId, name, phoneNumber)`: Add new customer
- `fetch_all_users()`: Retrieve all customers
- `get_user(customerId)`: Get specific customer details

### Courier Management
- `insert_courier(...)`: Create new shipment
- `fetch_all_courier()`: Get all shipments
- `get_courier(courierId)`: Get specific shipment details

### Pricing Logic
Automatic pricing based on package weight:
- 0-30 kg: ₹30
- 31-50 kg: ₹50
- 51-70 kg: ₹70
- 70+ kg: ₹100

## 📱 SMS Integration

The system uses Twilio for:
- OTP verification during customer login
- Delivery confirmation notifications
- Status update alerts

## 🗺️ Map Integration

Interactive maps show:
- Source and destination markers
- Route visualization
- Real-time tracking display

## 📊 Analytics Dashboard

The admin dashboard includes comprehensive analytics:
- **Count Analysis**: Shipment volume trends
- **Price Analysis**: Revenue analytics
- **Geographic Analysis**: Source/destination patterns
- **Status Tracking**: Delivery performance metrics
- **Weight Distribution**: Package size analytics
- **Profit Analysis**: Financial performance
- **Customer Insights**: User behavior patterns
- **Forecasting**: Predictive analytics

## 🔒 Security Features

- OTP-based authentication
- Phone number verification
- Admin login protection
- Secure database connections

## 🙏 Acknowledgments

- Streamlit for the amazing web framework
- Deta for cloud database services
- Twilio for SMS integration
- Folium for interactive maps
- Power BI for analytics dashboard

---

**Made with ❤️ for efficient courier management**
```
