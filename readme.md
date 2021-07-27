#   Locators Exercises

 __The purpose of this exercise is to learn and practice about locators, different strategies and how to name them properly. For this practice, we will use this [website](https://www.demoqa.com/) from which we will obtain the elements that need to be defined. Each exercise will relate to a specific element in the page and the format in which the
element must be defined.__


## Exercises

### 1. In the landing page, define the card “Elements” using xpath

        pagina= https://www.demoqa.com/
        //div[@class='category-cards']/div[1]

### 2. In this [page](https://www.demoqa.com/text-box), define the following elements:

  a. Full name: using css selector by Id
    
    - input#userName || input[id="userName"]
      
  b. Email: css selector by placeholder
    
    - input[placeholder="name@example.com"]
  
  c. Current Address: xpath by Id
    
    - //textarea[@id="currentAddress"]
  
  d. Permanent address: xpath by class
    
    - //div[4]/div[2]/textarea[@class="form-control"] || (//textarea[@class="form-control"])[2]
      
  e. Submit (button): xpath AND css by Id
    
    - //button[@id="submit"]  (Xpath by id)
    - button#submit           (cs selector by id)
      

### 3. In this page, define the following elements:

a. Home: xpath and css selector by Id
  
    - //a[@id="simpleLink"]   (Xpath by id)
    - a[id="simpleLink"]      (cs selector by id)
   
b. No Content: xpath by href

    - //a[@href="javascript:void(0)"][contains(text(),"No Content")]
    
c. List of links: xpath and css selector by tag (all the links)

    - #linkWrapper > p:nth-of-type(X) > a   (X es elnumero de posicion de cada link)
    
### 4. In this page, define the following elements:

a. What is Lorem Ipsum?: xpath and css selector by class

    - //div[@class="card-header"][contains(text(), "What is Lorem Ipsum")] -- xpath by class
      (//*[@class="card-header"])[1]
    - div:nth-child(1) > div[class="card-header"]
      div[class="card-header"][id="section1Heading"]
    
b. Why do we use it?: (To expand or collapse the text click on the link)
    
    i. Text inside closed by xpath using the class attribute.
        //div[3]/div[@class="collapse"]/div/p/text()
    
    ii. Text inside expanded by css selector using the class attribute.
        div:nth-child(3) > div[class="collapse show"] > div > p 
        
### 5. In this page, define the following elements:

a. Select date: xpath by value
    
    - //input[@value='07/26/2021'] 
    
b. Date and time: css selector by value.

    - input[value= 'July 26, 2021 5:01 PM']

## Extra Credits

__This page will be useful for the following exercises. However, feel free to search on the internet anything that is not explained there.__

### 6. In this page, obtain the text of the element called “Interactions” using xpath

      - //*[contains(text(), "Interactions")]
      
### 7. In this page, obtain the text from the following elements:

a. Text Box

    - //span[contains(text(), "Text Box")]

b. Buttons

    - //span[contains(text(), "Buttons")]
c. Broken Links - Images

    - //span[contains(text(), "Broken Links - Images")]
    
### 8. Create an xpath to match a span (located in the footer) that CONTAINS the text “QA"

    - //footer/span[contains(text(), 'QA')]

### 9. How would you change the xpath defined in the previous exercise to match ALL
ELEMENTS that CONTAIN the text QA.

    - //*[contains(text(), 'QA')]
