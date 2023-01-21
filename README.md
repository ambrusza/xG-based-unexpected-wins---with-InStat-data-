# xG based Unexpected Wins (with_InStatdata)
### How common is it for a team with a lower xG value to win a match in Hungarian NB1?



<!-- ABOUT THE PROJECT -->
## About The Project


### Goal, or what are we interested in?

how common is it for a team with a lower xG value to win a match in NB1?

Process:

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
   
   here, for further analysis, we distinguish between home and away teams, as well as collect detailed data of the matches (shots/xG)
   
   
4. **Analysis and plot:**

   we make a plot and analyze the data



This is where we want to go:

![Képernyőfotó 2023-01-21 - 19 24 54](https://user-images.githubusercontent.com/66861232/213881591-673d1390-591f-46f9-a606-0932a0c695b0.png)



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/ambrusz_a) - email@email_client.com



<p align="right">(<a href="#readme-top">back to top</a>)</p>


