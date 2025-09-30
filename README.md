# CountryListApp
This is an Android app that displays a list of countries from the Countries API .  The app follows MVVM architecture with offline caching, Hilt for DI, and modern Jetpack libraries.

✨ Features

Fetches countries from remote API using Retrofit.

Caches countries locally using Room Database for offline access.

Loads country flags with Glide (circular images).

Displays countries in a RecyclerView inside a Fragment.

Supports loading, success, and error states with a Resource wrapper.

Filter countries by region (Asia, Europe, Africa, etc.) via ActionBar menu.

Sorted results (ascending by name).

Hilt used for dependency injection.

StateFlow used for reactive UI updates.

🏗️ Architecture

The project follows MVVM (Model–View–ViewModel) with repository pattern:

com.example.countries
│
├── data
│   ├── local        # Room Database, DAO, entities
│   ├── remote       # Retrofit API service, DTOs
│   └── repository   # CountryRepository (decides API vs DB)
│
├── di               # Hilt modules
│
├── domain
│   └── model        # Domain models (Country)
│
├── ui
│   ├── main         # MainActivity
│   ├── countries    # CountriesFragment, Adapter, ViewModel
│
└── util             # Utils (NetworkUtils, Resource, Constants)

🔧 Tech Stack

Kotlin – main language

Coroutines + Flow – async & reactive streams

Retrofit – network calls

Room – local database (offline cache)

Hilt – dependency injection

StateFlow + ViewModel – UI state management

Glide – image loading (with circular ImageView)

RecyclerView – list rendering

MenuHost API – ActionBar filter menu
