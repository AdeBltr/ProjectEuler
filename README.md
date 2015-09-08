# ProjectEuler
1.
resultat = 0
for i in range(1, 1000):
    if i%3 == 0 or i%5 == 0:
        resultat += i
print(resultat)

2.
fibonacci = [2]

i = 0

number_1 = 1
number_2 = 2
number_3 = 0

while (number_3 <= 4000000):
    number_3 = number_1 + number_2
    fibonacci.append(number_3)

    if i % 2 != 0:
        number_1 = number_3
        i += 1
    elif i % 2 == 0:
        number_2 = number_3
        i += 1

total = 0

for numbers in fibonacci:
    if numbers % 2 == 0:
        total += numbers

print total

3. 
const long numm = 600851475143;
long largestFact = 0;
 
for (long i = 2; i < numm; i++) {
    if (numm % i == 0) { // It is a divisor
        bool isPrime = true;
        for (long j = 2; j < i; j++) {
            if (i % j == 0) {
                isPrime = false;
                break;
            }
        }
        if (isPrime) {
            largestFact = i;
        }
    }
}
