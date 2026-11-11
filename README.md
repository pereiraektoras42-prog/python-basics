def cups_to_grams(cups, ingredients):
    conversion_rates = {
        "flour": 120, # 1 cup = 120g for flour
        "sugar": 200, 
        "butter": 230,
        "milk": 240,
        }

    if ingredients in conversion_rates:
        grams = cups * conversion_rates[ingredients]
        return grams
    else:
        return "conversion rate for this ingredient is not available."

# Convert tablespoons to teaspoons
def tablespoons_to_teaspoons(tablespoons):
    return tablespoons * 3

# Convert grams to cups
def grams_to_cups(grams, ingredients):
    conversion_rates = {
        "flour": 120, # 1 cup = 120g for flour
        "sugar": 200,
        "butter": 230,
        "milk": 240,
        }

    if ingredients in conversion_rates:
        cups = grams / conversion_rates[ingredients]
        return cups
    else:
        return "conversion rate for this ingredient is not available."

# Main Program
def recipe_converter():

    while True:
        print("\nRecipe Converter App\n")
        print("1. Convert cups to grams")
        print("2. Convert tablespoons to teaspoons")
        print("3. Convert grams to cups")
        print("4. Exit")

        choice = input("Choose an option(1-4):")

        if choice =="1":
            cups = float(input("Enter the number of cups"))
            ingredient = input("Enter the ingredient (flour, sugar, butter):").strip().lower()
            result = cups_to_grams(cups, ingredient)
            print(f"Result: {result} grams")

        elif choice == "2":
            tablespoons = float(input("Enter the number of tablespoons:"))
            result = tablespoons_to_teaspoons(tablespoons) 
            print("Result: {result} teaspoons")    
