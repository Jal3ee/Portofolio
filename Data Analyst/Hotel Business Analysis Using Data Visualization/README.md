<h1>Investigate Hotel Business using Data Visualization</h1>
<h3>Background</h3>
Business performance analysis is crucial for companies to achieve success. In the hotel industry, understanding customer behavior is essential. Analyzing customer behavior helps identify factors influencing hotel bookings and enables businesses to adapt strategies to enhance customer experience and achieve long-term business goals.
<p> </p>
<h3>Problem Identification</h3>
1. What types of hotels are most frequently visited by customers?
2. Does the duration of stay affect hotel booking cancellation rates?
3. Does the lead time between hotel booking and guest arrival affect hotel booking cancellation rates?
<p> </p>
<h3>Business Objectives</h3>
Create data-based visualizations to gain insights for the hotel business.
<p> </p>
<h3>Tools</h3>
<ul>
<li>Jupyter Notebook</li>
<li>Python</li>
<li>Libraries: Pandas, NumPy</li>
<li>Visualization: Matplotlib, Seaborn</li>
</ul>
<p> </p>
<h3>Analytic Approach</h3>
<ol>
<li>Explore Hotel Booking Trends Based on Hotel Type:</li>
<ul>
<li>Assess monthly booking patterns for both City and Resort hotels.</li>
<li>Identify peak booking months and analyze customer preferences.</li>
</ul>

<li>Understand the Impact of Stay Duration on Cancellation Rates:</li>
<ul>
<li>Analyze the relationship between the duration of stay and hotel booking cancellation rates.</li>
<li>Investigate trends and potential factors influencing cancellation rates.</li>
</ul>

<li>Evaluate the Influence of Lead Time on Cancellation Rates:</li>
<ul>
<li>Examine the correlation between lead time (booking time to arrival) and hotel booking cancellation rates.</li>
<li>Provide insights into how lead time affects cancellation rates.</li>
</ul>
</ol>
<p> </p>
<h3>Preprocessing, Analyzing and Visualization</h3>
<ol>
  <li>Data Preprocessing</li>
  ### Data Overview
The dataset consists of 29 columns and 119,390 rows covering the period from 2017 to 2019.

### Data Assessment
Data assessment was conducted to ensure that the data used for further analysis is ready and meets the requirements of the analysis. The following steps were taken:
- Checking for null or missing values in the data
- Checking for data duplicates
- Verifying data types and value consistency
- Examining outliers or unusual data

Tabel 1 - Hasil Data Assessmen
 **Data Assessment** | **Finding**  | **Handling** 
--------------------|--------------|--------------
Missing values     | 	Null values found in `company`, `city`, `children`, and `agent` | - `company` : - `company` : **filled with 0**, indicating guests without a company affiliation <br> - `agent` : **filled with 0**, indicating guests who made self-reservations or did not go through an agent <br> - `children` : **filled with 0**, indicating guests without accompanying children <br> - `city` : **filled with 'Undefined'**, as the city is not precisely known
Inconsistent or inappropriate values | Meaning of 'Undefined' in the `meal` column | Values in the `meal` column can be categorized into **'With Meal'** (Breakfast, Full Board, Dinner) and **'No Meal'** (**No Meal, Undefined**)
Anomalous or unnecessary data | - Negative and significantly distant outlier values in the `adr` column <br> - 180 booking entries without guests | **Removing or dropping these data entries**           

<br>
<br>
<li>Data Analyzing and Visualization</li>
### 1. Monthly Hotel Booking Analysis Based on Hotel Type
This analysis aims to discern booking trends for each hotel type. It can assist the company **in better understanding the market and customer needs, enabling them to enhance operational efficiency and optimize revenue.**

<p align="center">
    <kbd><img width="600" alt="tipe hotel rasio" src="https://user-images.githubusercontent.com/115857221/230533333-0f148859-0edf-4baf-bfb6-18fcbe71d699.png"></kbd><br>
    Figure 1 — Percentage Ratio Graph of City Hotels and Resort Hotels
</p>
<br>

From the above plot, it's evident that **City Hotels are more favored by customers**, with a booking percentage of **66.41%**. These hotels are usually situated in city centers or urban areas, close to tourist and business locations, indicating that customers booking these hotels might have main activities around their stay. On the other hand, **Resort Hotels are booked by only 33.59% of customers**. These hotels are typically located in scenic areas like beaches, mountains, or quiet rural regions with comprehensive facilities. Customers booking these hotels likely have the intention of vacationing and relaxing in those locations.
<br>
<br>

<p align="center">
    <kbd> <img width="1000" alt="tipe hotel perbulan" src="https://user-images.githubusercontent.com/115857221/229820633-3b06eb81-5d85-4bba-bab6-733d5a846394.png">
 </kbd> <br>
     Figure 2 — Monthly Booking Figures for City Hotels and Resort Hotels
</p>
<br>

Hotel bookings tend to experience an **increase during holiday seasons**, especially in the **May - August** period. Both types of hotels, City Hotels and Resort Hotels, have the highest booking values during this period, with a **significant increase in City Hotels**. This is likely due to the numerous national holidays in 2017-2019, such as public holidays and religious events (Ramadan), allowing people to go on vacations. Additionally, with the majority of Indonesia's population being Muslim and the cultural practices of "mudik" (returning to hometowns) and "silaturahmi" (visiting relatives) during Eid al-Fitr, people tend to travel far and require accommodation in the midst of their journeys, leading to hotel bookings.

During the holiday season in the **October - December** period, hotel bookings also increase but tend to be lower than in May - August. It's likely that many people prefer to celebrate major holidays like Christmas and New Year at home.

In the **January - March** period, hotel booking rates are **lowest**. This is likely due to the scarcity of national holidays during this period, and it coincides with the beginning of the new school year for students, not being a busy period for business travel activities early in the year. <br>
<br>


### 2. Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
This analysis focuses on the relationship between the duration of stay and the cancellation rates of hotel bookings. According to data, approximately **19%** of hotel bookings made online are canceled before the customers arrive  [[source](https://www.phocuswire.com/One-in-five-hotel-bookings-on-the-web-are-cancelled)]. These cancellations can reduce room availability and impact hotel revenue because every empty room can be a financial burden for that day. Additionally, if a hotel uses an Online Travel Agency (OTA), these cancellation rates can affect the hotel's ranking in search results [[source](https://www.hotelminder.com/everything-you-need-to-know-about-hotel-cancellations)].

<p align="center">
    <kbd> <img width="600" alt="pembatalan city" src="https://user-images.githubusercontent.com/115857221/229821918-ae476922-2470-40fd-8dda-0a0a7f584b23.png"></kbd> <br>
    Figure 3 — Percentage of City Hotel Cancellations
</p>
<br>

<p align="center">
    <kbd><img width="600" alt="hotel resort" src="https://user-images.githubusercontent.com/115857221/229821958-a2153c90-9069-4685-a5d7-b0020763dbb2.png"></kbd> <br>
    Figure 4 — Percentage of Resort Hotel Cancellations
</p>
<br>

City Hotels also have a higher cancellation rate compared to Resort Hotels. This indicates that **customers booking City Hotels tend to cancel their reservations more frequently**. City Hotels, being centrally located in cities or urban areas and close to tourist and business locations, might have more activities to coordinate. This, along with other factors, could contribute to a higher rate of customers canceling their reservations.<br>
<br>

<p align="center">
    <kbd><img width="1000" alt="tren pembatalan" src="https://user-images.githubusercontent.com/115857221/229822263-6a6b771a-245f-4447-8c64-e1d44ad75e02.png">
</kbd> <br>
    Figure 5 — Cancellation Trends Based on Stay Duration
</p>
<br>

Based on the duration of stay, it is observed that **the cancellation rate of hotel bookings tends to increase with longer durations of stay**, both in City Hotels and Resort Hotels. In City Hotels, the cancellation rate increases significantly, with the percentage falling below 50% for a one-week duration. For stays of more than four weeks, Resort Hotels have a lower cancellation rate. In essence, both types of hotels exhibit **a positive trend, where the longer the duration of stay, the higher the likelihood of the reservation being canceled.**

The reason behind the increasing cancellation rate with longer stays could be evaluated and analyzed further by the company. Possible factors might include customer dissatisfaction. Customers staying in hotels for an extended period may have higher expectations and demand better service. If customers are dissatisfied with the hotel's service, they may decide to cancel their reservation and look for a better alternative. Additionally, higher costs could be a factor. Costs may exceed what customers expected or budgeted, leading them to seek more affordable alternatives.<br>
<br>



### 3. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates

The analysis is conducted to understand the correlation between reservation cancellations and lead time. Lead time is the waiting period or the time gap between hotel booking and the arrival date.

<p align="center">
    <kbd><img width="1000" alt="tren lead" src="https://user-images.githubusercontent.com/115857221/230551207-aa417f83-5979-4bc6-a615-e2f10e835b26.png"></kbd> <br>
     Figure 6 — Cancellation Trends Based on Lead Time
</p>
<br>

Pembatalan pemesanan **terendah** pada kedua tipe hotel terjadi pada *lead time* **kurang dari satu bulan**. Pembatalan **tertinggi hingga 60% terjadi pada City Hotel dengan *lead time* 10 bulan hingga 1 tahunan**. Sedangkan tren **Resort Hotel** memiliki tingkat pembatalan yang cukup **stagnan** dengan nilai **rata-rata 40%**.

The **lowest** booking cancellations for both hotel types occur with a lead time of **less than one month**. The **highest cancellation rate, up to 60%, occurs in City Hotels with a lead time of 10 months to 1 year**. Meanwhile, the trend for **Resort Hotels** shows a somewhat **stable cancellation rate with

Resort Hotels are likely more commonly used for vacations or recreational purposes, so customers tend to be more committed to their schedules and make fewer changes. Additionally, Resort Hotels, which may target customers seeking a more exclusive experience, might be better able to maintain their booking levels even when better offers are available elsewhere.

<br>
<br>
</ol>
<h3>Action and Value</h3>
The insights derived from this analysis can guide strategic actions to enhance the hotel business:
<ol>
  <li>Optimizing Hotel Facilities and Services:
    <ul>
      <li>For Resort Hotels with lower booking rates, consider enhancing facilities such as spa, gym, or swimming pools to attract more customers.</li>
      <li>Personalized and friendly services can improve customer satisfaction.</li>
    </ul>
  </li>


  <li>Strategic Marketing for City Hotels:
    <ul>
      <li>Implement additional services tailored to business needs, such as meeting packages or conference rooms.</li>
      <li>Utilize promotions during holiday seasons to boost bookings and revenue.</li>
    </ul>
  </li>

  <li>Managing Cancellation Rates:
    <ul>
      <li>Establish solid cancellation policies to protect against revenue loss.</li>
      <li>Consider implementing a flexible pricing strategy, limiting flexible rates to a one-week stay and offering non-refundable rates for longer durations.</li>
      <li>Provide pre-stay services and communication to increase customer satisfaction and reduce cancellations.</li>
    </ul>
  </li>


  <li>Reducing Lead Time Impact:</li>
    <ul>
      <li>Limit booking lead time to ensure customers are more certain about their stay.</li>
      <li>Consider adjusting room prices to improve profit margins and decrease cancellation rates.</li>
      <li>Implement reminder emails to guests approaching their stay, improving customer engagement and potentially reducing cancellations.</li>
    </ul>
  </li>
</ol>

<h3>Results and Evaluation</h3>
1. Overall, City Hotels are the most frequently booked by customers. Significant increases in customer bookings occur during holiday seasons, namely May-July and October-December, for both hotel types. Business recommendations:

    - The company can optimize facilities and services at Resort Hotels since they have lower booking rates compared to City Hotels. Enhancing facilities like spas, gyms, or swimming pools and providing more personalized and friendly services can attract more customers to book rooms there.
    - Maximizing strategies for City Hotels, given their high popularity, can be profitable. Additional services for business purposes, such as meeting rooms or packages for events like seminars, can be offered.
    - Increasing promotions during holiday seasons, such as providing special discounts for guests booking a certain number of rooms or offering attractive vacation packages. The company may also consider implementing non-refundable policies to prevent booking cancellations.
    - During off-peak seasons, the company can combine flexible and non-refundable rates or offer special discounts with non-refundable conditions. <br>
    <br>

2. Cancellation rates tend to increase with the length of stay for both hotel types. The cancellation rate at City Hotels significantly rises, with the lowest percentage for durations less than one week. Resort Hotels also experience an increasing cancellation rate, but it tends to be more stable. Recommendations for business:

    - The company should ensure robust cancellation policies to protect against potential revenue loss. Clearly communicating terms and conditions before booking, both online and offline, including information on refunds, cancellation fees, etc., can help. Stricter cancellation policies can have a significant impact and reduce fraudulent bookings.
    - Implement pricing strategies and limit the number of nights. Restricting flexible rates to a one-week range and providing non-refundable rates for longer stays can increase revenue and mitigate the risk of unwanted cancellations.
    - To prevent cancellations, the company can enhance services or offer excellent pre-stay services to improve customer satisfaction and reduce the likelihood of cancellations.<br>
    <br>

3. The lowest booking cancellations for both hotel types occur with a lead time of less than one month. City Hotels have the highest cancellation rate with a lead time of one year.

    - Both types of hotels may consider reducing lead times. By limiting the booking window, hotels can ensure that customers only book when they are genuinely certain about staying, reducing the likelihood of cancellations.
    - City Hotels can consider raising room rates to improve profit margins and decrease cancellation rates. Higher prices may make customers more inclined to reconsider before canceling their reservations.
    - Sending email reminders about bookings to stay connected and showcase the company's level of service. Informing customers that the deadline is approaching with details about the cancellation policy can help.
    - Instead of canceling reservations, the company can offer rescheduling and sell rooms with longer lead times. <br>
    <br>
    <br>
