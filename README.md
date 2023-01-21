# xG-based-unexpected-wins___(with_InStatdata)
How common is it for a team with a lower xG value to win a match in Hungarian NB1?

<!-- PROJECT LOGO -->
<br />
<div align="center">
 

<h3 align="center">Unexpected Wins</h3>

 
</div>

<!-- ABOUT THE PROJECT -->
## About The Project


### Goal, or what are we interested in?

how common is it for a team with a lower xG value to win a match in NB1?

Process:

1. We need data (we obtain them from InStat)


2. scrape:

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

3. **data sorting
   
   here, for further analysis, we distinguish between home and away teams, and also collect match data (shots/xG)
   
   
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```


This is where we want to go:

![Képernyőfotó 2023-01-21 - 19 24 54](https://user-images.githubusercontent.com/66861232/213881591-673d1390-591f-46f9-a606-0932a0c695b0.png)


Here's a blank template to get started: To avoid retyping too much info. Do a search and replace with your text editor for the following: `github_username`, `repo_name`, `twitter_handle`, `linkedin_username`, `email_client`, `email`, `project_title`, `project_description`

<p align="right">(<a href="#readme-top">back to top</a>)</p>
