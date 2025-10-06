# FormworkCalc - AI-Integrated Formwork Calculator

## Overview

FormworkCalc is a single-page web application designed for construction professionals to automatically analyze foundation plans using AI, calculate required formwork quantities, and provide visual layout schemes. The application integrates with OpenRouter API for intelligent blueprint analysis and operates as a mobile-first, responsive tool.

## Features

### 🤖 AI-Powered Analysis
- Automated extraction of wall dimensions from construction blueprints
- Support for multiple AI vision models (Claude, Gemini, GPT-4 Vision)
- Intelligent dimension parsing and validation

### 📊 Smart Formwork Calculation
- Optimized panel layout using greedy algorithm
- Real-time inventory management
- Waste minimization calculations
- Support for different foundation types

### 🎨 Visual Schema Generation
- Interactive canvas-based layout visualization
- Pan and zoom functionality
- Color-coded panel identification
- Detailed measurements and annotations

### 📱 Mobile-First Design
- Responsive design optimized for tablets and smartphones
- Touch-friendly interface
- Progressive web app capabilities
- Single HTML file deployment

## Quick Start

### 1. API Configuration
1. Get an OpenRouter API key from [openrouter.ai](https://openrouter.ai)
2. Enter your API key in the "API Configuration" section
3. The key is stored securely in your browser's local storage

### 2. Foundation Setup
1. Select your foundation type (Strip or Slab)
2. Set the foundation depth in millimeters
3. These settings affect the visual schema generation

### 3. Blueprint Analysis
**Option A: AI Analysis**
1. Upload a blueprint image (PNG/JPEG, max 10MB)
2. Click "Analyze Blueprint with AI"
3. Wait for AI to extract wall dimensions

**Option B: Manual Input**
1. Click "Enter Dimensions Manually"
2. Add wall lengths in millimeters
3. Click "Calculate Formwork Layout"

### 4. Inventory Management
**Sample Data:** Application loads sample formwork panel data automatically

**Custom Data:** 
1. Create a Google Sheets with columns: Width, Height, Quantity
2. Publish as CSV (File → Share → Publish to web → CSV)
3. Enter the CSV URL in the inventory section
4. Click "Load Inventory Data"

### 5. View Results
- **Summary Cards:** Total walls, panels used, and waste
- **Detailed Table:** Wall-by-wall breakdown
- **Visual Schema:** Interactive canvas with pan/zoom
- **Legend:** Color-coded panel identification

## Technical Specifications

### Supported File Formats
- **Blueprint Images:** PNG, JPEG, JPG (max 10MB)
- **Inventory Data:** CSV format via Google Sheets

### AI Model Support
- Anthropic Claude 3 Haiku (Primary)
- Google Gemini Pro Vision (Fallback)
- OpenAI GPT-4 Vision Preview (Secondary)

### Browser Compatibility
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Usage Examples

### Sample Inventory Data Format
```csv
Width,Height,Quantity
600,2400,20
900,2400,15
1200,2400,10
300,2400,25
450,2400,18
750,2400,12
```

### Manual Wall Input
- Enter each wall length in millimeters
- Example: 12000, 8500, 6000 for walls of 12m, 8.5m, and 6m
- Use the "+" button to add more walls
- Remove walls using the "×" button

### Google Sheets Integration
1. Create a spreadsheet with the required columns
2. Go to File → Share → Publish to web
3. Select "Entire Document" and "Comma-separated values (.csv)"
4. Copy the generated URL
5. Paste into the inventory URL field

## Troubleshooting

### Common Issues

**AI Analysis Not Working:**
- Verify API key is correctly entered
- Check blueprint image quality and file size
- Ensure dimensions are clearly visible in the image
- Try manual input as alternative

**Inventory Loading Failed:**
- Verify Google Sheets CSV URL format
- Check column names match requirements (Width, Height, Quantity)
- Ensure sheet is publicly accessible
- Try sample data first

**Canvas Not Displaying:**
- Check browser compatibility
- Ensure JavaScript is enabled
- Try refreshing the page
- Check browser console for errors

**Mobile Display Issues:**
- Use landscape orientation for better canvas viewing
- Pinch to zoom on the canvas area
- Use dedicated zoom controls for precise adjustments

### Performance Tips
- Use optimized blueprint images (compress large files)
- Limit wall count for complex calculations
- Use appropriate zoom levels for canvas viewing
- Clear browser cache if experiencing issues

## Development

### Architecture
- **Frontend:** Vanilla JavaScript, HTML5, CSS3
- **Styling:** Tailwind CSS (CDN)
- **Canvas:** HTML5 Canvas API
- **Storage:** Browser LocalStorage
- **AI Integration:** OpenRouter API

### File Structure
```
index.html          # Complete single-file application
├── HTML Structure  # Responsive layout components
├── CSS Styles     # Tailwind + custom styles
└── JavaScript     # Application logic
    ├── State Management
    ├── API Integration
    ├── Calculation Engine
    ├── Canvas Renderer
    └── UI Components
```

### Key Components
- `APIKeyManager`: Secure API key storage and validation
- `BlueprintUploader`: File handling and AI integration
- `InventoryManager`: CSV data parsing and management
- `FormworkCalculator`: Greedy algorithm implementation
- `CanvasRenderer`: Interactive visualization engine

## License

This project is provided as-is for educational and professional use in construction projects.

## Support

For issues, suggestions, or contributions, please refer to the application's error handling system which provides detailed feedback for troubleshooting.

---

**FormworkCalc** - Streamlining construction formwork planning with AI-powered analysis.