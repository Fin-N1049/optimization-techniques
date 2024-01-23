from itertools import permutations

def calculate_total_distance(order, distances):
    total_distance = 0
    n = len(order)

    for i in range(n - 1):
        total_distance += distances[order[i]][order[i + 1]]

    total_distance += distances[order[-1]][order[0]]
    return total_distance

def tsp_bruteforce(distances):
    n = len(distances)
    cities = list(range(n))
    all_permutations = permutations(cities)
    min_distance = float('inf')
    best_path = None

    for perm in all_permutations:
        distance = calculate_total_distance(perm, distances)
        if distance < min_distance:
            min_distance = distance
            best_path = perm

    return min_distance, best_path

distances = [
    [0, 10, 15, 20],
    [10, 0, 35, 25],
    [15, 35, 0, 30],
    [20, 25, 30, 0]
]

min_distance, best_path = tsp_bruteforce(distances)

print("Minimum Distance:", min_distance)
print("Best Path:", best_path)
