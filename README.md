# yelp-business   

## Overview
The Yelp-Business MCP is designed to enhance interactions between businesses and customers through various communication tools. This platform includes five primary tools to facilitate business discovery, inquiries, and detailed information retrieval.

## Tools

### 1. **Yelp Chat**
   - **Description**: A conversational AI tool that handles business inquiries, supporting multi-turn dialogue and location awareness.
   - **Input Requirements**:
     - `query` (required): Natural language text for querying specific Yelp information (e.g., "Where is the nearest Thai restaurant?").
     - `chat_id` (optional): A unique identifier for the current session, can be omitted on the first request.
     - `latitude` (optional): User's latitude for more accurate results.
     - `longitude` (optional): User's longitude for more accurate results.
     - `user_id` (optional): Unique identifier for the user for personalized responses.

### 2. **Yelp Search**
   - **Description**: Allows users to search for businesses via the Yelp Fusion API, returning up to 50 businesses.
   - **Input Requirements**:
     - `location` (required): Geographic area to search (e.g., "San Francisco").
     - `latitude` (optional): Required if location is not provided.
     - `longitude` (optional): Required if location is not provided.
     - `term` (optional): Keywords for the search (e.g., "coffee").
     - `radius` (optional): Search radius (in meters), maximum value is 40,000.
     - `categories` (optional): Categories to filter businesses (e.g., "restaurants").
     - `sort_by` (optional): Sorting method (e.g., "best_match" or "rating").
     - `limit` (optional): Number of results to return, default is 20.

### 3. **Yelp Phone Search**
   - **Description**: Searches for businesses based on phone number, returning matching results.
   - **Input Requirements**:
     - `phone` (required): Business phone number (including country code).
     - `locale` (optional): Locale code for regional results (e.g., "en_US").
     - `country_code` (optional): Country code for the phone number.

### 4. **Yelp Business Match**
   - **Description**: Matches business data using precise information.
   - **Input Requirements**:
     - `name` (required): Name of the business.
     - `address1` (required): Business address (line 1).
     - `city` (required): City of the business.
     - `state` (required): State or province of the business.
     - `country` (required): Country of the business.
     - `postal_code` (optional): Business postal code.
     - `phone` (optional): Business phone number.
     - `limit` (optional): Limit on the number of results returned, default is 1.
     - `address2` (optional): Business address (line 2).
     - `address3` (optional): Business address (line 3).

### 5. **Yelp Business Details**
   - **Description**: Retrieves detailed information for a specific business using its Business ID or alias.
   - **Input Requirements**:
     - `business_id_or_alias` (required): Unique identifier or alias for the business.
     - `locale` (optional): Locale code for regional results (e.g., "en_US").
     - `device_platform` (optional): Device platform information (e.g., "web" or "mobile").
     - `attributes` (optional): Specific attributes to retrieve (e.g., "parking" or "outdoor_seating").
