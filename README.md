# Food_Donation

User:

user_id: Primary key to uniquely identify users.
username: The username of the user.
email: The email address of the user.
password: The password (hashed and secured) of the user.
phone_number: The contact phone number of the user.
Orphanage:

orphanage_id: Primary key to uniquely identify orphanages.
name: The name of the orphanage.
address: The address of the orphanage.
contact_number: The contact phone number of the orphanage.
FoodItem:

food_item_id: Primary key to uniquely identify food items.
name: The name of the food item.
description: A description of the food item.
quantity: The available quantity of the food item.
DeliveryOrder:

order_id: Primary key to uniquely identify delivery orders.
user_id: Foreign key referencing the user_id in the User table.
orphanage_id: Foreign key referencing the orphanage_id in the Orphanage table.
order_date: The date when the order was placed.
OrderItem:

order_id: Foreign key referencing the order_id in the DeliveryOrder table.
food_item_id: Foreign key referencing the food_item_id in the FoodItem table.
quantity: The quantity of the specific food item in the order.
