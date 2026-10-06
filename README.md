# Parallel Resistance Calculation
# Formula: 1/R_total = 1/R1 + 1/R2 + ... + 1/Rn

n = int(input("Enter the number of resistors: "))

reciprocal_sum = 0

for i in range(1, n + 1):
    resistance = float(input(f"Enter resistance R{i} (Ohms): "))

    if resistance <= 0:
        print("Resistance must be greater than zero.")
        exit()

    reciprocal_sum += 1 / resistance

total_resistance = 1 / reciprocal_sum

print("Total Parallel Resistance =", round(total_resistance, 2), "Ohms")