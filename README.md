# Agenda:

## 08.30 am: Intro, career paths in data and questions
   1. [This](https://docs.google.com/presentation/d/e/2PACX-1vRbfvQpTP4ARbARRWhOL6WZ6koCKSHvf5OxFyHcJjn8GHXG3OpuneEH6uMYlpxKX0H_sEfHB6KAKrkq/pub?start=true&loop=false&slide=id.g29007063b8d_0_118) is how my career is progressing so far
   2. [Here](https://docs.google.com/presentation/d/e/2PACX-1vQp61itveaNmpuS4UMXIfaQshjMYBqywRP2aMWZjMlZy5v-iNOUouDMn_-z33RBwi2TeauhgEzGoep-/pub?start=false&loop=false)'s some information about career paths in data
   3. What [problems](https://padlet.com/kohwyhow/what-problems-do-you-want-to-solve-gjcypqiq99ko1wke) do you want to solve?

## 09.00 am: Looker Studio
   1. [Create](https://mail.google.com/mail/) a Google account (you can use your personal one too, if you prefer)
   2. Head to [Looker Studio](https://datastudio.google.com/), using another tab
   3. Download as [CSV](https://docs.google.com/spreadsheets/d/1IaonaJj-c5Ud76Uc9WeRiMSlKLTNnbg-BCUxOoZrXn0/edit?usp=sharing) from here and upload to Looker Studio
   4. Build a few charts and filters
       - What are the total `sales` by `category` and `year`?
       - What are the total `profit` by `category` and `year`?
       - Which `cities` have generated the highest `sales`?
       - What are the `margins` by `segment`?
       - Make your dashboard look better using a [color palette generator](https://coolors.co/)
   5. Practice by creating another page named `Customer`, and using any chart/table:
       - What is the name of the Customer with the Highest Sales in New York City?
       - What Sub-Category did this Customer buy, and how much Sales and Profit did this Customer generate for the company?
       - Open question: Is the business doing better or worse off from 2014 to 2017?
    
   - Source: Superstore sample data from [Tableau](https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls)
___

## 10.30 am: Break
___

## 10.50 am: Google Colab and Seaborn
   1. Using either your new Google account or your personal account, open [Google Colab](https://colab.research.google.com/) in another tab
   2. Google Colab's interface and functions:
     - Tools >> Settings >> 
         - Editor >> Show line numbers (check if you prefer)
         - Miscellaneous >> Corgi mode, Kitty mode (turn on if you like)
      - Test with some basic code:
         - Click Connect at top right
         - Write simple definition	
         - Test simple math problem
      - Runtime settings
         - Run cells
         - Reset
      - Code and text cells
      - Save
   3. More about Colab’s Markdown here
   4. Refer to [colab_intro.ipynb](https://github.com/atlas-github/2023fstep25/blob/main/colab_intro.ipynb)
   5. Open a new notebook on [Google Colab](https://colab.research.google.com/)
   6. Try out a few plots on Seaborn:
      - [histplot](https://seaborn.pydata.org/generated/seaborn.histplot.html#seaborn.histplot)
      - [displot](https://seaborn.pydata.org/generated/seaborn.displot.html#seaborn.displot)
      - [boxplot](https://seaborn.pydata.org/generated/seaborn.boxplot.html#seaborn.boxplot)
      - [lmplot](https://seaborn.pydata.org/generated/seaborn.lmplot.html#seaborn.lmplot)
   7. Practice:
      - Load the [CSV](https://docs.google.com/spreadsheets/d/1IaonaJj-c5Ud76Uc9WeRiMSlKLTNnbg-BCUxOoZrXn0/edit?usp=sharing) into Colab
      - Create a [displot](https://seaborn.pydata.org/generated/seaborn.displot.html#seaborn.displot), where x-axis represents `Region`
      - Create a [catplot](https://seaborn.pydata.org/generated/seaborn.catplot.html#seaborn.catplot), where x-axis is `Profit` and y-axis is `Sub-Category`
      - Adjust the size of charts by `sns.set(rc={'figure.figsize':(25.7,8.27)})`
      - Create a [boxplot](https://seaborn.pydata.org/generated/seaborn.boxplot.html#seaborn.boxplot) where x-axis is `Sales`, and y-axis is `Region`
___   

## 12:30 pm: Break
___

## 1:30 pm: [data.gov.my](https://data.gov.my/dashboard)
   1. Using either your new Google account or your personal account, sign up for [Postman](https://www.postman.com/), then log in
       - Look for Workspaces (top left of the page) >> My Workspace (Click)
       - ![image](https://github.com/atlas-github/2023fstep25/assets/50855923/4144bc9c-1375-404e-9a39-747cd179724c)
         
       - Look for the + sign beside Overview
       - ![image](https://github.com/atlas-github/2023fstep25/assets/50855923/3582e9e2-61d3-4925-811d-959303ffca23)
         
   2. Open [data.gov.my](https://data.gov.my/dashboard) using another tab on your browser >> API Docs
   3. Scroll to Realtime APIs >> Weather API
   4. Try the Forecast API Endpoint `GET https://api.data.gov.my/weather/forecast` on Postman
        - Look for the icon circled in the snapshot below
        - ![image](https://github.com/atlas-github/2023fstep25/assets/50855923/f68b0004-a86f-467a-8c0c-d0a5c47c09a5)
     
        - Switch from cURL to Python - Requests
        - ![image](https://github.com/atlas-github/2023fstep25/assets/50855923/225b80ec-0323-42ad-8eb0-67c9d5ae0d85)
     
        - Copy the Python code from Postman and paste into a new [Colab notebook](https://colab.research.google.com/)

   5. Change `print(response.text)` to `response.json()` to see the data returned by the API endpoint
   6. Tasks:
      - Convert json output into a dataframe using `pd.json_normalize()`
      - Store dataframe into a variable `df`
      - Filter to include only `df[df['location.location_name'] == 'Langkawi']`
      - Output into a CSV file, then download and open in Excel
      - Now try the Transport API (GTFS-R) and output the locations of Prasarana buses on Google My Maps
      - What other questions can you answer?
      - Don't forget to try using the [Weather API](https://developer.data.gov.my/realtime-api/weather) 

___    

## 2:30 pm: Break
___
    
## 2.50 pm: Send emails of Air Pollution Index (API) data using Python
   1. Need to [create](https://mail.google.com/mail/) another Google account, if you haven't already. Remember to activate [2-Step Verification](https://support.google.com/accounts/answer/185839)
   2. Refer to Sending a [Plain-Text Email](https://realpython.com/python-send-email/). Look for the code section just above the **Sending a Fancy Email** header.
   3. Register for an account on [aciqn](https://aqicn.org/api/)
   4. Using Postman, try making an API call (documentation [here](https://aqicn.org/json-api/doc/#api-City_Feed-GetCityFeed))
      - `GET https://api.waqi.info/feed/kuala%20lumpur/?token=###INSERT TOKEN HERE###`
   5. From Postman, copy the Python code into a [Colab notebook](https://colab.research.google.com/)
   6. Tasks:
      -  Get the API readings of a few stations
      -  Send the email containing the API of a chosen station/a few selected locations
___

## 4.15 pm: Wrap up
   1.  Data visualization and coding skills help to automate routine tasks - worth picking up to save time
       - Looker Studio / Power BI
       - [Exam PL-300](https://learn.microsoft.com/en-us/certifications/exams/pl-300/): Microsoft Power BI Data Analyst 
       - [Python Crash Course](https://nostarch.com/pythoncrashcourse2e)
   2. Get certified for cloud computing
       - [Google Cloud](https://cloud.google.com/certification)
       - [Azure](https://docs.microsoft.com/en-us/learn/certifications/)
       - [Amazon Web Services](https://aws.amazon.com/certification/)

