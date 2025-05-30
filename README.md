# Murotal API

[![GitHub stars](https://img.shields.io/github/stars/cloudkuimages/cloudku-murotal-api?style=social)]()
[![GitHub forks](https://img.shields.io/github/forks/cloudkuimages/cloudku-murotal-api?style=social)](https://github.com/cloudkuimages/murotal-api/network/members)
[![GitHub issues](https://img.shields.io/github/issues/cloudkuimages/murotal-api)](https://github.com/cloudkuimages/cloudku-murotal-api/issues)
[![GitHub license](https://img.shields.io/github/license/cloudkuimages/cloudku-murotal-api)](https://github.com/cloudkuimages/cloudku-murotal-api/blob/main/LICENSE)
[![npm version](https://img.shields.io/npm/v/naruyaizumi)](https://www.npmjs.com/package/naruyaizumi)

Powerful and efficient API for accessing Quranic recitations (Murotal) with comprehensive features and easy integration.

## 🚀 Features

- **Complete Quran Recitations** - Access full Quran audio from various renowned reciters
- **Multiple Reciters** - Choose from different qaris with high-quality audio
- **Surah & Verse Access** - Get specific surahs or individual verses
- **Audio Formats** - Multiple audio format support (MP3, etc.)
- **Fast Response** - Optimized for speed and reliability
- **Easy Integration** - Simple REST API endpoints
- **Comprehensive Metadata** - Detailed information about surahs, verses, and reciters


## 🛠️ Installation & Usage

### NPM Package
```bash
npm install naruyaizumi
```

### Basic Usage
```javascript
const { MurotalAPI } = require('naruyaizumi');

const api = new MurotalAPI();
const recitation = await api.getMurotal('abdulbasit', 1);
```

### API Endpoints
```
GET /api/murotal/{reciter}/{surah}
GET /api/murotal/{reciter}/{surah}/{verse}
```

### NPM Implementation
```javascript
const { MurotalAPI } = require('naruyaizumi');

const api = new MurotalAPI({
  baseURL: 'https://api.cloudku.us.kg'
});

const data = await api.getRecitation({
  reciter: 'abdulbasit',
  surah: 1
});
```

### Response Format
```json
{
  "status": "success",
  "data": {
    "surah": 1,
    "name": "Al-Fatihah",
    "reciter": "Abdul Basit",
    "audio_url": "https://...",
    "duration": "02:30"
  }
}
```

## 🔗 Available Endpoints

- `/reciters` - List all available reciters
- `/surahs` - Get all surah information
- `/murotal/{reciter}` - Get all recitations by specific reciter
- `/murotal/{reciter}/{surah}` - Get specific surah recitation
- `/search?q={query}` - Search reciters or surahs

## 🤝 Contributing

1. Fork this repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## ⭐ Show Your Support

If this project helps you, please give it a ⭐ star!

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
