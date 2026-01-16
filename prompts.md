### eCommerce Prompts

#7-Prompts

```
// Instructions
Can you craft a system instructions for a ecommerce website that accepts unstructured text input from a user requesting products that may contain metadata-based details that can filter product selection. The agent also exposes a search Bing website tool that can be invoked for web searches if needed.
```

```
"Looking for a great egg sandwich that doesn't cost over $6.00"
"Looking for a great egg sandwich that cost less than $4.00"
```

```
"I love peanut butter cups and cookies. What can I buy that has both?"
"Can you deliver to my home"
"my address is 4410 Kelly Drive, Richardson, TX"
"What is the address of nearest 7-11 store for me?"
"Can you check inventory at the nearest store"
** I can’t see store addresses in the files you shared—only product inventory for a nearby 7‑Eleven (store ID 12202), and those files don’t include a street addres
```

```
""
///Direct Lookup
Prompt: “Do you have Doritos?”
Expected Response: “Yes. Doritos Nacho Cheese 9.75oz is available.”

// Category Browsing
Prompt: “What snacks do you have?”
Expected Response: “We have chips, pretzels, popcorn, and nuts. For example: Doritos, Lay’s, and Smartfood Popcorn.”

// Vague/Natural Requests
Prompt: “I need something for a headache.”
Expected Response: “We carry pain relief products like Advil and Tylenol.”

// Comparisons
Prompt: “What’s your cheapest pizza?”
Expected Response: “Our lowest-priced pizza is Cheese Pizza 10” for $4.99.”

// Clarification Needed
Prompt: “I want a Coke.”
Expected Response: “We have Coca-Cola in 12oz cans, 20oz bottles, and 2L bottles. Which size do you prefer?”

//Out of Stock / Not Carried
Prompt: “Do you have gluten-free beer?”
Expected Response: “Sorry, we don’t carry gluten-free beer.”
```

```
"How are you managing the context between chat turns?"
"Looking for a great egg sandwich that cost less than $4.00"
```


