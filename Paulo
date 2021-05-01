### Program make a simple calculator ###
##
# Imports
import reverse_geocoder as rg
import geocoder
import pyziptax
import socket
import ipinfo
from requests import get

##########  API Connections Start ##########

### Try Catch ###
# try:

# This function handles the Geo Code to grab longitude + latitude
gpslock = geocoder.ip('me')

# This function handles the reverseGeo Code to grab location from longitude + latitude
cordinates = (gpslock.latlng)
a = rg.search(cordinates)
translateArray = a[0]
userState = translateArray['admin1']
userCity = translateArray['name']

# This function grabs the user's IP address to determine their ZipCode
ip = get('https://api.ipify.org').text
access_token = 'f4fe41cfc27590'
handler = ipinfo.getHandler(access_token)
ip_address = format(ip)
details = handler.getDetails(ip_address)
userZipcode = details.postal

# This function uses the user ZipCode and location variables above to determine local TaxRate
pyziptax.api_key = 'Nq9iTwClWpHBQkFD'
rate = pyziptax.get_rate(userZipcode, userCity)
userTax = (rate / 100)

## Error Catch ###
# except:
#     print("Oops!", sys.exc_info()[0], "occurred.")

##########  API Connections End ##########

### Try Catch ###
# ry:

# This function adds two numbers
def add(x, y):
        return x + y

# This function subtracts two numbers
def subtract(x, y):
        return x - y

# This function multiplies two numbers
def multiply(x, y):
        return x * y

# This function divides two numbers
def divide(x, y):
        return x / y

### Error Catch ###
# except:
#   print("Oops!", sys.exc_info()[0], "occurred.")

# Prints Results
print("Select operation.")

print("1.Add")

print("2.Subtract")

print("3.Multiply")

print("4.Divide")

### Try Catch ###
# try:

while True:

        # Take input from the user !!!!!!!!!!!!!!Variable and UI NEEDED FOR THIS

        choice = input("Enter choice(1/2/3/4): ")

        # Check if choice is one of the four options
        if choice in ('1', '2', '3', '4'):

            num1 = float(input("Enter first number: "))

            num2 = float(input("Enter second number: "))

        if choice == '1':
            taxamt = add(num1, num2) * float(userTax)
            print('$', num1, "+", '$', num2, "=")
            print('Sub-Total', "=", '$', add(num1, num2))
            print('TAX Amount', "=", '$', float(taxamt))
            print('Total Amount', "=", '$', add(num1, num2) + taxamt)

        elif choice == '2':

            taxamt = subtract(num1, num2) * float(userTax)
            print('$', num1, "-", '$', num2, "=")
            print('Sub-Total', "=", '$', subtract(num1, num2))
            print('TAX Amount', "=", '$', float(taxamt))
            print('Total Amount', "=", '$', subtract(num1, num2) - taxamt)

        elif choice == '3':

            taxamt = multiply(num1, num2) * float(userTax)
            print('$', num1, "*", '$', num2, "=")
            print('Sub-Total', "=", '$', multiply(num1, num2))
            print('TAX Amount', "=", '$', float(taxamt))
            print('Total Amount', "=", '$', multiply(num1, num2) + taxamt)

        elif choice == '4':

            taxamt = divide(num1, num2) * float(userTax)
            print('$', num1, "/", '$', num2, "=")
            print('Sub-Total', "=", '$', divide(num1, num2))
            print('TAX Amount', "=", '$', float(taxamt))
            print('Total Amount', "=", '$', divide(num1, num2) + taxamt)
        break

else:

        print("Invalid Input")
# except:
#   print("Oops!", sys.exc_info()[0], "occurred.")
