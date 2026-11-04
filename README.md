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
