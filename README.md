# Pinterest-Clone
A scalable backend service and RESTful API inspired by Pinterest for visual content discovery, pin curation, and board management.

## Features

* **Dynamic Home Feed:** Responsive masonry grid layout for seamless browsing.
* **Search & Discover:** Search photos by keywords and view high-resolution details.
* **Pins & Boards:** Save favorite images ("Pins") to personal custom collections ("Boards").
* **User Profile:** Manage saved pins, created boards, and user account settings.

---

## Prerequisites

Make sure you have the following installed on your machine:

* **Node.js** (v18.0.0 or higher)
* **npm** or **yarn**
* **Expo CLI** or **React Native CLI**

* ## ⚙️ Installation & Setup

<sequence>

{/* Step-by-step setup procedure for a mobile React Native repo where execution sequence prevents runtime errors. */}

  <Step title="Clone the Repository">
    Pull down the project files to your local environment:

    ```bash
    git clone [https://github.com/your-username/pinterest-clone.git](https://github.com/your-username/pinterest-clone.git)
    cd pinterest-clone
    ```
  </Step>

  <Step title="Install Frontend Dependencies">
    Install all UI, navigation, and state-management packages:

    ```bash
    npm install
    # or using yarn
    yarn install
    ```
  </Step>

  <Step title="Set Up Environment Variables">
    Create a `.env` file in the root directory:

    ```env
    API_BASE_URL=http://localhost:5000/api
    EXPO_PUBLIC_CLOUDINARY_URL=your_cloudinary_url_here
    ```
  </Step>

  <Step title="Start the Development Server">
    Launch Metro Bundler via Expo:

    ```bash
    npx expo start
    ```
  </Step>

  <Step title="Run on Device or Emulator">
    * **iOS Simulator:** Press `i` in the terminal.
    * **Android Emulator:** Press `a` in the terminal.
    * **Physical Device:** Scan the printed QR code using the **Expo Go** app.
  </Step>

</Sequence>

---

## 📂 Project Structure

text
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

### Quick Start Example

Here is a simple component showing how to fetch and display pins on a home screen:

```jsx
import React, { useEffect, useState } from 'react';
import { View, Image, FlatList, Text, StyleSheet } from 'react-native';

export default function SimplePinFeed() {
  const [pins, setPins] = useState([]);

  useEffect(() => {
    // Fetch pins from your API
    fetch('[https://api.example.com/pins](https://api.example.com/pins)')
      .then((res) => res.json())
      .then((data) => setPins(data));
  }, []);

  return (
    <View style="{styles.container}">
      <FlatList data="{pins}" keyExtractor="{(item)"> item.id}
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
  container: { flex: 1, padding: 8, backgroundColor: '#fff' },
  card: { flex: 1, margin: 4, borderRadius: 12, overflow: 'hidden' },
  image: { width: '100%', height: 200, borderRadius: 12 },
  title: { fontSize: 14, fontWeight: 'bold', marginTop: 4 },
});

```
## 👥 Contributor Credits

|:rehab altaiyeb| :main writer| : https://github.com/rehabaltaiyeb35-rgb|

