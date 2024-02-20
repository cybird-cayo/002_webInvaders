import requests
from bs4 import BeautifulSoup

url = input("Please provide a website: ")
if ("https" or "http") in url:
    data = requests.get(url)
else:
    data = requests.get("https://" + url)
data.encoding = data.apparent_encoding
soup = BeautifulSoup(data.text, "html.parser")
contents = []

for content in soup.find_all(True):
    contents.append(content)

with open("DirectoryMap.txt", 'w', encoding='utf-8') as saved:
    print(contents, file=saved)
