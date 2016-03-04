# trello-groceries

This light Python tool connects to your Trello board where you store your recipes and your weekly meals and it builds
for you a groceries list ready to go.

# In a nutshell

trello-groceries is in an early developement stage so the documentation is far from extensive
and the tool is not too flexible yet.

To create your grocery list, you first need to create a new Trello board with at least three lists:
  1. The 'Recipes' list contains one card per recipe.
  2. The 'Week meals' list contains one card per day.
  3. The 'Groceries' list is empty and you don't need to worry about it!

In a simple way, trello-groceries reads your weekly meals plan, retrieve the ingredients from the recipe for each meal,
and then aggregate the ingredients to build your new groceries list.

For more details about how to format your list, keep on reading! ;)

# The lists

For trello-groceries to work, your lists and cards need to be properly formatted. Here are the guidelines to build your lists.

## Recipes

Each card in the Recipes list must contain one recipe.

The title of a recipe/card identifies it uniquely. The recipe's description can be broken down in two parts: the mandatory ingredients
part, and the optional instructions part. Following is an example of a complete recipe:
  ```
  # Ingredients
  
  - chicken breasts [1 cup]
  - egg whites [4]
  - *salt
  - *pepper
  - *breadcrumbs
  - olive oil [1/4 cup]
  
  # Instructions
  
  - Blend the 4 chicken breast with the 4 egg whites
  - Make small balls of the mix
  - Roll the balls in breadcrumbs
  - Heat oil in a pan and cook the nuggets, turn after 4-5 minutes
  ```

### Ingredients

This part of the recipe is mandatory: trello-groceries won't be able to build your groceries list if you don't give your ingredients.
Each ingredient can have a given quantity indicated between brackets, this quantity can be a number or a fraction followed (or not) by
a unit (oz, cup, lb, but also slice, bunch, etc). A star at the beginning of the ingredient indicates that this ingredient should not
be added to your groceries list. This is useful for very recurrent ingredients like salt, or pepper.

### Instructions

The instructions part of the recipe is optional and can be freely formatted, trello-groceries is not using this part to build your
groceries list.

## Weekly meals

## Groceries list

# Requirements

# Future work

- Documentation.
- Script code to class code.
- Add 'Owned' list to take into account products already in the pantry/fridge.
- Add price estimation of the groceries list: need an API.
- Use POS and stemming to retrieve ingredients and quantity instead of hard coding the parsing. (e.g. write
'diced chicken breast [1 cup]' and get 1 cup of chicken breasts added to the groceries list)
- Add ingredients without matching recipe?
