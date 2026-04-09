# Office-Sales-PowerBI-Dashboard
It is an analysis of Office Supplies, Furniture, and Tech sales.


🏢 Making Sense of Office Sales: A Power BI Journey
Welcome! This repository houses a project where I took a deep dive into the messy world of retail data. Using a dataset focused on Office Supplies, Furniture, and Technology, I built an interactive dashboard to answer one big question: How can we sell smarter, not just more?

📸 The "Big Picture"
I wanted the UI to feel like a modern "Command Center." Here is the final result:

Why a Dark Theme?
I chose a high-contrast dark theme to make the key metrics (the "glowing" cards) pop. In a real-world setting, this helps managers quickly spot anomalies without getting lost in a sea of white cells.

🧠 The Problems I Wanted to Solve
When I started, I didn't just want to count sales. I wanted to solve specific business headaches:

The "Heavy Lifting" Problem: Furniture is bulky. By analyzing Shipment Modes, I wanted to see how much we rely on Standard vs. First Class shipping for these items.

The Payment Gap: Seeing that 43% of customers choose COD (Cash on Delivery) was a "lightbulb" moment. It shows a huge need for secure payment options or localized collection strategies.

The Seasonal Rollercoaster: Using the Sum of Sales by Month chart, you can clearly see the holiday rush. It’s the difference between being prepared and being overwhelmed.

🛠️ The "Under the Hood" (DAX)
To make the data dynamic, I used DAX. One of my favorite measures in this project was calculating Year-Over-Year Sales Variance. It's easy to see total sales, but it's much more useful to know if we are growing or shrinking compared to last year.

Code snippet
YoY Sales Growth = 
VAR CurrentSales = SUM(Sales[Amount])
VAR PriorYearSales = CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR('Date'[Date]))

RETURN
IF(
    ISBLANK(PriorYearSales), 
    "New Data", 
    DIVIDE(CurrentSales - PriorYearSales, PriorYearSales)
)
📈 What I Learned
Through this project, I realized that Technology drives the revenue, but Office Supplies drive the frequency. Balancing these two is the key to a healthy retail business.

I also practiced a lot of Power Query magic to ensure the dates and regions were perfectly aligned for the map visual you see in the top right!

👋 Let's Connect!
If you're a fellow data enthusiast or just curious about how I built this:

LinkedIn: [Your Profile Link Here]

Thoughts? Drop a star ⭐ on this repo if you find it helpful!
