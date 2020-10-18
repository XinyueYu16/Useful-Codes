# Useful-Codes
常用代码块

## 爬虫（设置session）
def webcapture(url):
    headers = {
   # pretend I am a browser
   'User-Agent': 'Mozilla/5.0',
   }
    session = requests.Session() #setup session
    data = session.get(url, headers=headers) #scrape the data
    soup = BeautifulSoup(data.text, 'html.parser') #parse the data
    return soup #return the parsed data
    
    
# 解决plt中文乱码
import matplotlib.pyplot as plt
%matplotlib inline
plt.rcParams['font.sans-serif'] = ['SimHei'] #解决中文乱码
plt.rcParams['axes.unicode_minus'] = False #解决符号问题
