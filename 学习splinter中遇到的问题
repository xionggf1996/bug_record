学习splinter
代码如下：
from splinter.browser import Browser
browser = Browser()
browser =Browser(driver_name="chrome")
browser.visit('https://www.baidu.com/')
browser.fill('wd','splinter - python acceptance testing for web applications')
button = browser.find_by_xpath('//*[@id="su"]')
button.click()
browser.find_by_xpath('//*[@id="1"]/h3/a').click()
if browser.is_text_present('splinter.readthedocs'):
    print("yes,found it!")
else:
    print('NO!,did not find it:')
出处中文文档上cpoy来的。

1.bug：
Traceback (most recent call last):
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\site-packages\selenium\webdriver\common\service.py", line 76, in start
    stdin=PIPE)
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\subprocess.py", line 756, in __init__
    restore_signals, start_new_session)
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\subprocess.py", line 1155, in _execute_child
    startupinfo)
FileNotFoundError: [WinError 2] 系统找不到指定的文件。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "spider.py", line 2, in <module>
    browser = Browser()
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\site-packages\splinter\browser.py", line 63, in Browser
    return driver(*args, **kwargs)
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\site-packages\splinter\driver\webdriver\firefox.py", line 65, in __init__
    timeout=timeout, **kwargs)
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\site-packages\selenium\webdriver\firefox\webdriver.py", line 160, in __init__
    self.service.start()
  File "C:\Users\Administrator\AppData\Local\Programs\Python\Python37-32\lib\site-packages\selenium\webdriver\common\service.py", line 83, in start
    os.path.basename(self.path), self.start_error_message)
selenium.common.exceptions.WebDriverException: Message: 'geckodriver' executable needs to be in PATH.

重点：我解决的方法是：去掉了 browser = Browser（） 之后程序运行成功.分析原因暂无！
