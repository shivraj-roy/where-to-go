# Where to Go

This project helps you choose a place to visit using the `useEffect` hook in a React application.

## Getting Started

1. Clone the repository:

   ```sh
   git clone https://github.com/shivraj-roy/where-to-go.git
   cd where-to-go
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

3. Start the development server:
   ```sh
   npm run dev
   ```

## Usage

The main component uses the `useEffect` hook to fetch a list of places to visit and displays them.

### Example Code

```jsx
import React, { useState, useEffect } from "react";

const PlacesToVisit = () => {
   const [places, setPlaces] = useState([]);

   useEffect(() => {
      fetch("https://api.example.com/places")
         .then((response) => response.json())
         .then((data) => setPlaces(data))
         .catch((error) => console.error("Error fetching places:", error));
   }, []);

   return (
      <div>
         <h1>Places to Visit</h1>
         <ul>
            {places.map((place) => (
               <li key={place.id}>{place.name}</li>
            ))}
         </ul>
      </div>
   );
};

export default PlacesToVisit;
```

## Contributing

Feel free to submit issues and pull requests.

## License

This project is licensed under the MIT License.
