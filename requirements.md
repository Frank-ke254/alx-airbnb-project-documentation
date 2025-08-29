# Technical and Functional Requirements:
  1. User authentication:
     Jwt will be used to ensure users are correctly aunthenticated based on their role in the system.
  2. Property management:
    Cloud solutions such as amazon s3 and cloudinary will be used to store images withe the implementation done in file storage.
  3. Notification system:
    Third party email services such as SendGrid and Mailgun will be used for managing and enabling email notifications.
  4. Search and filtering:
    With the help of the databse and cache the users will be able to filter and search for the property of their choice by location, price and amenities.

# API endpoints:
  ## Users endpoints:
    GET /users/ - List all users
    POST /users/ - Create a new user
    GET /users/{user_id}/ - Retrieve a specific user
    PUT /users/{user_id}/ - Update a specific user
    DELETE /users/{user_id}/ - Delete a specific user

  ## Properties endpoints:
    GET /properties/ - List all properties
    POST /properties/ - Create a new property
    GET /properties/{property_id}/ - Retrieve a specific property
    PUT /properties/{property_id}/ - Update a specific property
    DELETE /properties/{property_id}/ - Delete a specific property

  ## Bookings endpoints:
    GET /bookings/ - List all bookings
    POST /bookings/ - Create a new booking
    GET /bookings/{booking_id}/ - Retrieve a specific booking
    PUT /bookings/{booking_id}/ - Update a specific booking
    DELETE /bookings/{booking_id}/ - Delete a specific booking

  ## Payment endpoint:
    POST /payments/ - Process a payment

  ## Reviews endpoints:
    GET /reviews/ - List all reviews
    POST /reviews/ - Create a new review
    GET /reviews/{review_id}/ - Retrieve a specific review
    PUT /reviews/{review_id}/ - Update a specific review
    DELETE /reviews/{review_id}/ - Delete a specific review

# Performance criteria:
  Performance optimazation will be enabled by use of caching (redis) to improve response time.

# Input and output specifications:
  1. User registration:
      input: user_id, first_name, last_name, phone_number and email.
      process: validate inputs.
      output: user is authenticated and logged in to the system.
  2. Property management:
      input: property_id, host_id, name, description, location and pricepernight.
      process: validate inputs.
      output: property added to the properties section.
  3. Booking:
      input: booking_id, user_id, property_id, name and amount.
      process: validate inputs.
      output: booking confirmation.    
  4. Payment:
      input: customer_id, property_id, payment_method and amount.
      process: validate inputs.
      output: property booking payment confirmation.
  5. Reviews:
      input: sender_id, recipient_id, message_body and review_id.
      process: validate inputs.
      output: Reviews that are visible to others.
     
# Validation rules:
  Profile photos must be a passport picture of the user.
