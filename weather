import requests
import matplotlib.pyplot as plt

api_key = "62ed9d2511ad4f2d9f422759252501"
city = input("Enter the city name: ")
url = "http://api.weatherapi.com/v1/current.json?key=" + api_key + "&q=" + city +"&aqi=yes"

response = requests.get(url)

if response.status_code == 200:
    data = response.json()
 
 
print(f"""
    Weather Data for {city}:
    Temperature: {data['current']['temp_c']}°C
    Humidity: {data['current']['humidity']}%
    Wind Speed: {data['current']['wind_kph']}km/h
    Condition: {data['current']['condition']['text']}
    UV Index: {data['current']['uv']}

""")

x = ['Temperature(°C)', 'Humidity(%)', 'Wind Speed(km/h)', 'UV index']
y = [data['current']['temp_c'], data['current']['humidity'], data['current']['wind_kph'], data['current']['uv']]

plt.bar(x, y, color='skyblue')
plt.title("Weather Parameters Visuallzation")  
plt.xlabel("")         
plt.ylabel("Values")     
plt.savefig("Weather Parameters Visuallization.png")  
