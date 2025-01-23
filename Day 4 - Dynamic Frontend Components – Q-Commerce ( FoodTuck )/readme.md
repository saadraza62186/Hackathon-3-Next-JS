Day 4 - Dynamic Frontend Components – Q-Commerce ( FoodTuck ) 

Functional Deliverables 

1. Screenshots/Screen Recordings 

Product Listing Page 

Displays dynamic data fetched from the API for all available restaurant items, such as food dishes or beverages. 

Includes dynamic category filters for menu sections (e.g., "Starters," "Main Course," "Desserts," etc.). 

Pagination enabled for a user-friendly browsing experience. 

Individual Product Detail Pages 

Each product (menu item) routes to its unique detail page with accurate rendering of data fetched from the API. 

Includes detailed descriptions, pricing, images, and availability status. 

Category Filters, Search Bar, and Pagination 

Functional category filters that allow users to narrow down menu items by type. 

A search bar for users to find specific dishes or beverages by name or ingredients. 

Pagination to navigate between pages when the menu exceeds a single page. 

Code Deliverables 

1. Key Components 

   {/* Chef Cards Section */}
      <div className="w-[1320px] h-[1386px] ml-[300px] mt-[200px]">
        <div className="flex flex-wrap justify-center items-center gap-5">
          {chefs.map((chef : any) => (
            <OurChef
              key={chef._id}
              imageSrc={urlFor(chef.image).url()} // Use `urlFor` to generate image URL
              name={chef.name}
              position = {chef.position}
            />
          ))}
        </div>
      </div>


2. API Integration and Dynamic Routing 

     <div className="w-[984px] h-[1810px] flex flex-wrap gap-3">
          {foods.map((food : any) => (
            <ShopItems
              key={food._id}
              imageSrc={urlFor(food.image).url()} // Use `urlFor` to generate image URL
              description={food.name}
              price={food.price}
              originalPrice={food.originalPrice}
            />
          ))}
          </div>

API Integration Logic 

 

Documentation 

Steps Taken to Build and Integrate Components 

Designed Reusable Components 

Created OurChef and ShopItems for modular and scalable development. 

Set Up API Integration 

Developed API calls using Sanity CMS to fetch products. 

Implemented Dynamic Routing 

Used Next.js dynamic routing for individual product detail pages. 

Enhanced User Experience 

Added features like related products and a user profile component for personalization. 

Challenges Faced and Solutions Implemented 

Challenge: Slow API response times causing delays in data loading. 

Solution: Implemented loading states and optimized API queries with proper filters and pagination. 

Challenge: Dynamic routing failing to fetch data for certain product IDs. 

Solution: Added error handling to display fallback content when data is unavailable. 

Best Practices Followed During Development 

Followed a mobile-first responsive design approach. 

Ensured code modularity and reusability with well-structured components. 

Used proper error handling for API integration. 

Followed accessibility guidelines, such as semantic HTML and alt attributes for images. 