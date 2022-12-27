# my-subscribtion
def find_combinations(budget, prices):
    # Initialize an empty list to store the combinations
    combinations = []

    # Generate all possible combinations of newspaper subscriptions
    for newspaper_1 in prices:
        for newspaper_2 in prices:
            # Calculate the total cost of the combination
            cost = prices[newspaper_1] + prices[newspaper_2]

            # If the cost is within the budget, add the combination to the list
            if cost <= budget:
                combinations.append({newspaper_1, newspaper_2})

    # Return the list of combinations
    return combinations

# Test the function with the example input
print(find_combinations(40, {“TOI”: 3, “Hindu”: 2.5, “ET”: 4, “BM”: 1.5, “HT”: 2}))
