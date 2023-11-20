from urllib.request import urlopen
readweb=urlopen('https://www.codingninjas.com/courses')
readweb
readweb_01=readweb.read()
print(readweb_01)
#parsing from here
from bs4 import BeautifulSoup as soup
soup01=soup(readweb_01,'html.parser')
print(soup01)
soup01.findAll('div')
title =soup01.findAll('div',{'class':'ninja-splash-screen-logo'})
print(title)
