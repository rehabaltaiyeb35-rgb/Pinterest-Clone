

markdown
# Pinterest-Clone

A scalable backend service and RESTful API inspired by Pinterest for visual content discovery, pin curation, and board management.

---

## 🚀 Features

* **Dynamic Home Feed:** Responsive masonry grid layout for seamless browsing.
* **Search & Discover:** Search photos by keywords and view high-resolution details.
* **Pins & Boards:** Save favorite images ("Pins") to personal custom collections ("Boards").
* **User Profile:** Manage saved pins, created boards, and user account settings.

---

## 🛠️ Prerequisites

Make sure you have the following installed on your machine before running the application:

* **Node.js** (`v18.0.0` or higher)
* **npm** or **yarn**
* **Expo CLI** or **React Native CLI**

---

## ⚙️ Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone [https://github.com/rehabaltaiyeb35-rgb/pinterest-clone.git](https://github.com/rehabaltaiyeb35-rgb/pinterest-clone.git)
   cd pinterest-clone

```

2. **Install Dependencies**
```bash
npm install
# or using yarn
yarn install

```


3. **Set Up Environment Variables**
Create a `.env` file in the root directory:
```env
API_BASE_URL=http://localhost:5000/api
EXPO_PUBLIC_CLOUDINARY_URL=your_cloudinary_url_here

```


4. **Start the Development Server**
```bash
npx expo start

```


5. **Run on Device or Emulator**
* **iOS Simulator:** Press `i` in the terminal.
* **Android Emulator:** Press `a` in the terminal.
* **Physical Device:** Scan the printed QR code using the **Expo Go** app.



---

## 📂 Project Structure

```text
pinterest-clone/
├── assets/            # Fonts, static images, and icons
├── src/
│   ├── components/    # Reusable UI elements (MasonryCard, BoardItem)
│   ├── navigation/    # React Navigation stacks & tabs
│   ├── screens/       # Main views (Home, Profile, Search, PinDetails)
│   ├── services/      # API clients & authentication logic
│   └── utils/         # Helper functions & grid calculations
├── App.js             # Entry point
└── package.json

```

---

## 💡 Usage Example

Here is a simple React Native component demonstrating how to fetch and display pins in a dual-column layout:

```jsx
import React, { useEffect, useState } from 'react';
import { View, Image, FlatList, Text, StyleSheet } from 'react-native';

export default function SimplePinFeed() {
  const [pins, setPins] = useState([]);

  useEffect(() => {
    fetch('[https://api.example.com/pins](https://api.example.com/pins)')
      .then((res) => res.json())
      .then((data) => setPins(data))
      .catch((err) => console.error(err));
  }, []);

  return (
    <View style="{styles.container}">
      <FlatList data="{pins}" keyExtractor="{(item)"> item.id.toString()}
        numColumns={2}
        renderItem={({ item }) => (
          <View style="{styles.card}">
            <Image item.imageUrl source="{{" style="{styles.image}" uri: }}/>
            <Text style="{styles.title}">{item.title}</Text>
          </View>
        )}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  container: { 
    flex: 1, 
    padding: 8, 
    backgroundColor: '#ffffff' 
  },
  card: { 
    flex: 1, 
    margin: 4, 
    borderRadius: 12, 
    overflow: 'hidden' 
  },
  image: { 
    width: '100%', 
    height: 200, 
    borderRadius: 12 
  },
  title: { 
    fontSize: 14, 
    fontWeight: 'bold', 
    marginTop: 4 
  },
});

```

---

## 👥 Contributor Credits

| Name | Role | GitHub Profile |
| --- | --- | --- |
| **Rehab Altaiyeb** | Main Writer & Developer | [@rehabaltaiyeb35-rgb](https://www.google.com/search?q=https://github.com/rehabaltaiyeb35-rgb) |

---

## 📜 License

This project is licensed under the MIT License.

```

```
