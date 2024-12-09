# ai prompt writing


below is my prompt my schema a recipes ingredients and an output I got from Quen2.5-coder-0.5b-instruct-4bit

## prompt:
	This recipe is not formatted correctly for my data base can you take the recipe below and parse it into this format prefer imperial measurements over metric
## schema
```
Ingredients": [
            {
                "quantity": " amount",
                "unit": "oz., cup teaspoon etc",
                "ingredient": "the name of the ingredient",
                "preparation_method":"words like minced diced shredded trimmed",
		        "optional_notes": "the recipe authors extra information or (optional)"
		        "alternative": "if there is an extra ingredient in the ingerdient you will add it here  "
            },
        ]
```
### Example:

**Recipe ingredient string**

```
1/2 cup /60g well-chopped walnuts or pecans
```

**Parsed output**

```json
“Ingredients": [
            {
                "quantity": “1/2",
                "unit": "cup",
                "ingredient": "walnuts",
                "preparation_method":"well-chopped",
		        "optional_notes": ""
		        "alternative": "pecans "
            },
        ]
```

## recipe ingredients

```json

"ingredients": [
"1 cup / 225g unsalted butter, room temperature",
"1 cup / 200g granulated sugar",
"1 cup / 170g brown sugar, firmly packed",
"1 egg, room temperature",
"1 cup / 185g avocado oil or sunflower seed oil",
"1 cup / 90g rolled oats, not instant",
"1 cup / 50g crushed cornflakes",
"1/2 cup /40g unsweetened shredded coconut",
"1/2 cup/ 60g well-chopped walnuts or pecans",
"1 teaspoon vanilla extract",
"3 1/2 cups / 435g unbleached all-purpose flour",
"1 teaspoon baking soda",
"1 1/2 teaspoon fine grain sea salt",
"Large-grain sugar (optional)",
"Freeze-dried raspberries, crushed (optional)"
],
```
##output from ai 

Here's the JSON representation of the recipe ingredients:

```json
{
  "ingredients": [
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "unsalted butter",
      "preparation_method": "minced diced shredded trimmed",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "granulated sugar",
      "preparation_method": "firmly packed",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "brown sugar, firmly packed",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 egg",
      "unit": "room temperature",
      "ingredient": "room temperature"
    },
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "avocado oil or sunflower seed oil",
      "preparation_method": "not instant",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "rolled oats, not instant",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 cup",
      "unit": "oz.",
      "ingredient": "crushed cornflakes",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1/2 cup /40g",
      "unit": "unsweetened shredded coconut",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1/2 cup /40g",
      "unit": "unsweetened shredded coconut",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1/2 cup /40g",
      "unit": "unsweetened shredded coconut",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 teaspoon vanilla extract",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "3 1/2 cups / 435g",
      "unit": "unbleached all-purpose flour",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 teaspoon baking soda",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "1 1/2 teaspoon",
      "unit": "fine grain sea salt",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "Large-grain sugar (optional)",
      "optional_notes": "the recipe authors extra information or (optional)"
    },
    {
      "quantity": "Freeze-dried raspberries, crushed",
      "optional_notes": "the recipe authors extra information or (optional)"
    }
  ]
}

```

This JSON representation adheres to the specified schema with the same structure and components as the input recipe. Adjust the quantities and units as needed for your specific recipe.
