# xG based Unexpected Wins (with_InStat data)

![](https://komarev.com/ghpvc/?username=ambrusza&style=for-the-badge)

#### How common is it for a team with a lower xG value to win a match in Hungarian NB1?



<!-- ABOUT THE PROJECT -->
## About The Project


### Goal, or what are we interested in?

how common is it for a team with a lower xG value to win a match in Hungarian NB1?

Process:

prerequisit:
what is xG? -> link: https://twitter.com/ambrusz_a/status/1602384735333933057

Note: we annotated the steps performed ([in the file](main_notebook_xG_analysis.ipynb/))

1. **Data:**
   We need data (we obtain them from InStat)

2. **Scrape:**

   - here for scraping we have to write an access password code (here you should get by with your own e-mail and password)
     ``` sh
     def site_login():
       driver.get ('https://football.instatscout.com/login')
       time.sleep(3)
       try:
           user_name = driver.find_element_by_name("email")
           user_name.send_keys("?????????@???.com")
       except NoSuchElementException:
           print("exception handled")
       password = driver.find_element_by_name("pass")
       submit = driver.find_element_by_name("commit")

       password.send_keys("?????")
       submit.click()
       
       driver = webdriver.Safari()
       
       site_login()
      ```

   - we have to collect the data we need, then organize and clean it
   - we are also interested in the number of xGPoints that can be obtained based on xG - that's why we write a function for this as well

3. **Data sorting:**
   
   here, for further analysis, we distinguish between home and away teams, as well as collect detailed data of the matches (shots/xG) etc.
   
   
4. **Analysis and plot:**

   we make a plot and analyze the data



This is where we want to go:

![Képernyőfotó 2023-01-21 - 19 24 54](https://user-images.githubusercontent.com/66861232/213881591-673d1390-591f-46f9-a606-0932a0c695b0.png)


**result** 

The team with the least xG won 22 of 94 games (~23% unexpected win)
and of these 22 matches, 16 were (~72%) matches where the winning team with less xG scored the first goal


<!-- CONTACT -->
## Contact

Ambrusz Árpád (Hungary)

email: ambruszarpad@gmail.com

<div id="badges">
  <a href="https://twitter.com/ambrusz_a">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
</div>


