---
author: Ron Henson
created: 2022-10-10
---

# Travel_Log Brainstorm Database

## tables

- user
  - id (automatically assigned)
  - nickname (If exists, will be shown on the page, otherwise first_name)
  - first_name
  - last_name
  - username(email address)
  - password
  - role

- role
  - user.id
  - id
  - name

- user_emails
    - user.id (primary_key)
    - id    (primary_key)
    - email

- user_phone_number
  - user.id (primary_key)
  - id (primary_key)
  - user_phone_type_id
  - phone_number

- user_phone_type
  - mobile
  - home
  - work
  - other

- categories
  - some fixed categories cannot delete
  - customizable categories
    - should you be able to delete a category if it is being used?  Probably not.  Possibly have items without categories unintentionally
  - id
  - category_name
  - category_type_id

- category_types
  - hidden
  - system (can be seen and applied but not customize)
  - address_book
  - journal
  - photos
  - travel_mode
    - car
    - rv
    - plane
    - train
    - hiking
    - bicycling
    -

- journal
  - id
  - Always have an owner (user)
  - creation_date_timestamp (store as gmt)
  - modification_date ( Is there a modification hitory and can you undo??)
  - date_arrival (store as gmt)
  - date_departure (store as gmt)
  - address_book.id

- address_book  ( possiblity django-address 0.2.8) `pip install django-address`
  - id
  - name
  - address_1
  - address_2
  - state / province (state_id)
  - postalcode
  - country (country_id)
  - location_coord (google_maps)

  [[travel-log-use-cases]]
