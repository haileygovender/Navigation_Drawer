# 📱 Navigation Drawer Android App (Kotlin)

This is a beginner-friendly Android application demonstrating how to implement a **Navigation Drawer** using Kotlin. The app includes a toolbar, a drawer layout, and fragment swapping based on menu selection from the drawer.

## 🎯 Features

- Navigation drawer with clickable menu items
- Toolbar integration with drawer toggle icon
- Fragment management for each drawer item
- Toast message on logout
- Smooth user experience with back navigation handling

## 🧱 Built With

- Kotlin  
- Android Studio  
- AndroidX DrawerLayout & NavigationView  
- Fragments  

## 🧪 How It Works

1. `DrawerLayout` wraps the main content and navigation menu.  
2. `NavigationView` hosts the menu items (e.g., Home, Settings, Share, About, Logout).  
3. `Toolbar` is linked to an `ActionBarDrawerToggle` to open/close the drawer.  
4. When a menu item is clicked, the corresponding fragment is displayed via `replaceFragment()`.  
5. On back press, if the drawer is open, it closes; otherwise, the app exits.  

## 📂 Project Structure

com.example.navigationdrawer/  
├── MainActivity.kt → Sets up drawer, handles navigation item clicks  
├── HomeFragment.kt  
├── SettingFragment.kt  
├── ShareFragment.kt  
├── AboutFragment.kt  
└── res/  
  └── layout/  
    ├── activity_main.xml → Contains DrawerLayout, Toolbar, NavigationView  
    ├── fragment_home.xml  
    ├── fragment_settings.xml  
    ├── fragment_share.xml  
    └── fragment_about.xml  

## 🧩 Example Navigation Logic

```kotlin
override fun onNavigationItemSelected(item: MenuItem): Boolean {
    when(item.itemId) {
        R.id.nav_home -> replaceFragment(HomeFragment())
        R.id.nav_settings -> replaceFragment(SettingFragment())
        R.id.nav_share -> replaceFragment(ShareFragment())
        R.id.nav_about -> replaceFragment(AboutFragment())
        R.id.nav_logout -> Toast.makeText(this, "Logout!", Toast.LENGTH_SHORT).show()
    }
    drawerLayout.closeDrawer(GravityCompat.START)
    return true
}

```
## 🚀 How to Run
Clone the repository:
git clone https://github.com/yourusername/navigation-drawer-kotlin-app.git

Open the project in Android Studio

Run the app on an emulator or connected device

Swipe from the left or tap the menu icon to open the drawer and navigate

## 📄 License
This project is licensed under the MIT License.


