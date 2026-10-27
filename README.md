# python-activity-based-learing-2
Algorithm
1.Start.
2.Enter electricity units consumed for 3 months.
3.Calculate bill using slabs:
First 100 units: ₹2/unit
Next 100 units: ₹3/unit
Above 200 units: ₹5/unit
4.Add fixed charge ₹50.
5.Apply a ₹20 rebate if the bill is above ₹500? No — apply it if the bill is below ₹500.
6.Compare monthly bills and identify an increase above 50%.
7.Display bills and stop.
units = [80, 150, 250]
bills = []

for u in units:
    if u <= 100:
        bill = u * 2
    elif u <= 200:
        bill = 200 + (u - 100) * 3
    else:
        bill = 500 + (u - 200) * 5

    bill += 50

    if bill < 500:
        bill -= 20

    bills.append(bill)

for i in range(3):
    print("Month", i + 1, "Bill: Rs.", bills[i])

    if i > 0 and bills[i] > bills[i-1] * 1.5:
        print("Unusual increase!")
Month 1 Bill: Rs. 190
Month 2 Bill: Rs. 480
Unusual increase!
Month 3 Bill: Rs. 800
Unusual increase!

        
