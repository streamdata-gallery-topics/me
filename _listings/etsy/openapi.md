---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 1
info:
  title: Etsy
  description: bring-etsys-handmade-marketplace-and-community-into-your-apps-
  version: 1.0.0
host: openapi.etsy.com
basePath: /v2/private/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /homepages/pickers/:
    get:
      summary: Get Homepages Pickers
      description: Finds all FeaturedListingPicker in scope active.
      operationId: getHomepagesPickers
      x-api-path-slug: homepagespickers-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Pickers
  /homepages/pickers/{featured_listing_picker_id}:
    get:
      summary: Get Homepages Pickers Featured Listing Picker
      description: Retrieves a FeaturedListingPicker by id.
      operationId: getHomepagesPickersFeaturedListingPicker
      x-api-path-slug: homepagespickersfeatured-listing-picker-id-get
      parameters:
      - in: path
        name: featured_listing_picker_id
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Pickers
      - Featured
      - Listing
      - Picker
  /homepages/pickers/{featured_listing_picker_id}/featured:
    get:
      summary: Get Homepages Pickers Featured Listing Picker Featured
      description: Retrieves a set of FeaturedListing objects associated to a FeaturedListingPicker.
      operationId: getHomepagesPickersFeaturedListingPickerFeatured
      x-api-path-slug: homepagespickersfeatured-listing-picker-idfeatured-get
      parameters:
      - in: path
        name: featured_listing_picker_id
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Pickers
      - Featured
      - Listing
      - Picker
      - Featured
  /homepages/pickers/{featured_listing_picker_id}/listings:
    get:
      summary: Get Homepages Pickers Featured Listing Picker Listings
      description: Retrieves a set of Listing objects associated to a FeaturedListingPicker.
      operationId: getHomepagesPickersFeaturedListingPickerListings
      x-api-path-slug: homepagespickersfeatured-listing-picker-idlistings-get
      parameters:
      - in: path
        name: featured_listing_picker_id
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Pickers
      - Featured
      - Listing
      - Picker
      - Listings
  /homepages/pickers/{featured_listing_picker_id}/listings/active:
    get:
      summary: Get Homepages Pickers Featured Listing Picker Listings Active
      description: Retrieves a set of Listing objects associated to a FeaturedListingPicker
        in scope active.
      operationId: getHomepagesPickersFeaturedListingPickerListingsActive
      x-api-path-slug: homepagespickersfeatured-listing-picker-idlistingsactive-get
      parameters:
      - in: path
        name: featured_listing_picker_id
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Pickers
      - Featured
      - Listing
      - Picker
      - Listings
      - Active
  /homepages/listings/:
    get:
      summary: Get Homepages Listings
      description: Finds all FeaturedListings regardless of Listing state
      operationId: getHomepagesListings
      x-api-path-slug: homepageslistings-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Listings
  /homepages/listings/active:
    get:
      summary: Get Homepages Listings Active
      description: Finds all FeaturedListings that point to active Listings
      operationId: getHomepagesListingsActive
      x-api-path-slug: homepageslistingsactive-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Listings
      - Active
  /homepages/listings/{featured_listing_id}:
    get:
      summary: Get Homepages Listings Featured Listing
      description: Retrieves a FeaturedListing by id.
      operationId: getHomepagesListingsFeaturedListing
      x-api-path-slug: homepageslistingsfeatured-listing-id-get
      parameters:
      - in: path
        name: featured_listing_id
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Listings
      - Featured
      - Listing
  /homepages/listings/{featured_listing_id}/picker:
    get:
      summary: Get Homepages Listings Featured Listing Picker
      description: Retrieves a set of FeaturedListingPicker objects associated to
        a FeaturedListing.
      operationId: getHomepagesListingsFeaturedListingPicker
      x-api-path-slug: homepageslistingsfeatured-listing-idpicker-get
      parameters:
      - in: path
        name: featured_listing_id
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Listings
      - Featured
      - Listing
      - Picker
  /homepages/listings/{featured_listing_id}/listing:
    get:
      summary: Get Homepages Listings Featured Listing Listing
      description: Retrieves a set of Listing objects associated to a FeaturedListing.
      operationId: getHomepagesListingsFeaturedListingListing
      x-api-path-slug: homepageslistingsfeatured-listing-idlisting-get
      parameters:
      - in: path
        name: featured_listing_id
      responses:
        200:
          description: OK
      tags:
      - Home Pages
      - Listings
      - Featured
      - Listing
      - Listing
  /listings/{listing_id}/payments:
    get:
      summary: Get Listings Listing Payments
      description: Retrieves a set of ListingPayment objects associated to a Listing.
      operationId: getListingsListingPayments
      x-api-path-slug: listingslisting-idpayments-get
      parameters:
      - in: path
        name: listing_id
      responses:
        200:
          description: OK
      tags:
      - Listings
      - Payments
  /users/{user_id}/recommended_listings:
    get:
      summary: Get Users User Recommended Listings
      description: Get recommended listings for an authenticated member. The number
        of listings returned may not match the specified limit if there is no activity
        from recommended shops.
      operationId: getUsersUserRecommendedListings
      x-api-path-slug: usersuser-idrecommended-listings-get
      parameters:
      - in: query
        name: excluded_listing_ids
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Recommended
      - Listings
  /users/{user_id}/recommended_listings/rejects/{listing_ids}:
    post:
      summary: Post Users User Recommended Listings Rejects Listing S
      description: Registers rejections of recommended listings. Affects future recommended
        listings.
      operationId: postUsersUserRecommendedListingsRejectsListingS
      x-api-path-slug: usersuser-idrecommended-listingsrejectslisting-ids-post
      parameters:
      - in: path
        name: listing_ids
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Recommended
      - Listings
      - Rejects
      - Listings
  /users/{user_id}/recommended_listings/views/{listing_ids}:
    post:
      summary: Post Users User Recommended Listings Views Listing S
      description: Register viewings of recommended listings. Affects future recommended
        listings.
      operationId: postUsersUserRecommendedListingsViewsListingS
      x-api-path-slug: usersuser-idrecommended-listingsviewslisting-ids-post
      parameters:
      - in: path
        name: listing_ids
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Recommended
      - Listings
      - Views
      - Listings
  /users/{user_id}/payments:
    get:
      summary: Get Users User Payments
      description: Retrieves a set of BillPayment objects associated to a User.
      operationId: getUsersUserPayments
      x-api-path-slug: usersuser-idpayments-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: query
        name: offset
        description: Bring Etsys handmade marketplace and community into your apps
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Payments
  /users/{user_id}/payments/templates:
    get:
      summary: Get Users User Payments Templates
      description: Retrieves a set of PaymentTemplate objects associated to a User.
      operationId: getUsersUserPaymentsTemplates
      x-api-path-slug: usersuser-idpaymentstemplates-get
      parameters:
      - in: path
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Users
      - Payments
      - Templates
  /payments/templates/{payment_template_id}:
    get:
      summary: Get Payments Templates Payment Template
      description: Retrieves a PaymentTemplate by id.
      operationId: getPaymentsTemplatesPaymentTemplate
      x-api-path-slug: paymentstemplatespayment-template-id-get
      parameters:
      - in: path
        name: payment_template_id
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Templates
      - Payment
      - Template
    put:
      summary: Put Payments Templates Payment Template
      description: Updates a PaymentTemplate
      operationId: putPaymentsTemplatesPaymentTemplate
      x-api-path-slug: paymentstemplatespayment-template-id-put
      parameters:
      - in: query
        name: allow_check
      - in: query
        name: allow_mo
      - in: query
        name: allow_other
      - in: query
        name: allow_paypal
      - in: query
        name: city
      - in: query
        name: country_id
      - in: query
        name: first_line
      - in: query
        name: name
      - in: path
        name: payment_template_id
      - in: query
        name: paypal_email
      - in: query
        name: second_line
      - in: query
        name: state
      - in: query
        name: zip
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Templates
      - Payment
      - Template
  /payments/templates:
    post:
      summary: Post Payments Templates
      description: Creates a new PaymentTemplate
      operationId: postPaymentsTemplates
      x-api-path-slug: paymentstemplates-post
      parameters:
      - in: query
        name: allow_check
      - in: query
        name: allow_mo
      - in: query
        name: allow_other
      - in: query
        name: allow_paypal
      - in: query
        name: city
      - in: query
        name: country_id
      - in: query
        name: first_line
      - in: query
        name: name
      - in: query
        name: paypal_email
      - in: query
        name: second_line
      - in: query
        name: state
      - in: query
        name: zip
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Templates
  /payments/{listing_payment_id}:
    get:
      summary: Get Payments Listing Payment
      description: Retrieves a ListingPayment by id.
      operationId: getPaymentsListingPayment
      x-api-path-slug: paymentslisting-payment-id-get
      parameters:
      - in: path
        name: listing_payment_id
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Listing
      - Payment
---