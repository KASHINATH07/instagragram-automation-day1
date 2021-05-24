from selenium import webdriver
from time import sleep
class Bot():
    def __init__(self):
        self.driver=webdriver.Chrome()
        self.driver.get('https://www.instagram.com/')
        sleep(15)
        user_input=self.driver.find_element_by_xpath('//*[@id="loginForm"]/div/div[1]/div/label/input')
        user_input.send_keys("hii")
        passw=self.driver.find_element_by_xpath('//*[@id="loginForm"]/div/div[2]/div/label/input')
        passw.send_keys("hello")
        logibutton=self.driver.find_element_by_xpath('//*[@id="loginForm"]/div[1]/div[3]/button')
        logibutton.click()

def main():
    my_bot=Bot()


if __name__=='__main__':
    main()
