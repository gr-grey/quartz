---
title: "food log"
date: "2023-07-25"
tags:
- "dev-logs"
---

My weight over time.

<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>

<div id="weight-chart"></div>

<script>
    // Function to read the TSV file
    async function fetchTSV(url) {
        const response = await fetch(url);
        const text = await response.text();
        return text;
    }

    // Function to parse the TSV data
    function parseTSV(data) {
        const rows = data.split('\n').slice(1); // Skip the header row
        const dates = [];
        const weights = [];

        rows.forEach(row => {
            const columns = row.split('\t');
            if (columns.length === 2) {
                const date = columns[0];
                const weight = parseFloat(columns[1]);
                if (!isNaN(weight)) {
                    dates.push(date);
                    weights.push(weight);
                }
            }
        });

        return { dates, weights };
    }

    // Fetch and parse the TSV data
    fetchTSV('/attachments/weightRecord.tsv')
        .then(data => {
            const { dates, weights } = parseTSV(data);

            // Create the Plotly chart
            const trace = {
                x: dates,
                y: weights,
                type: 'scatter',
                mode: 'lines+markers',
                name: 'Weight'
            };

            const layout = {
                title: 'Weight Over Time',
                xaxis: { title: 'Date' },
                yaxis: { title: 'Weight (kg)' }
            };

            Plotly.newPlot('weight-chart', [trace], layout);
        })
        .catch(error => {
            console.error('Error fetching or parsing data:', error);
        });
</script>


## 2023-09-16

breakfast sandwich, 2 slices of bread, 2 eggs, 1 slice of cheese, 1 slice of bacon
1 apple cinnamon oats, 3 nature valley crunch bars (chocolate, peanut butter, honey oats)
2 beivita crunchy biscuit (1 cinnamon, 1 chocolate)
1 row of great value oat cookie

Lunch, 
some black beans and chicken
3 dessert rolls in a plate
1 apple, 1 yogurt
tortilla chips with guac and chicken quesadilla

Afternoon snacks,
1 Klondike Reese's ice cream bar
2 nature valley crunchy granola bars (chocolate and peanut butter)
1 beivita biscuit

Night,
1 apple, some blueberries
2 chocolate cookies, 1 nature value honey oat bar
1 diet coke
1 beivita biscuit

## 2023-08-05

2 eggs + veggie  + 1 cup of beans

2 pack of three small cookies,
1 protein bar,
1 hot chocolate with milk,
1 apple,

2 tacos,
1 orange,
half a bag of sliced brioche,
1 bagel with cream cheese,
2.2 lbs of cherry,

fried chicken plate - half chicken + fries + coleslaw,  
3/4 of Aldi's triple chocolate cake

---

Note:

I seems to be getting better at this.
Originally really worried because I've been stressed out and emotionally all over the place after relocated to Dallas this week.

Then a bunch of  things went wrong and I felt like I couldn't catch a break.
I thought today was going to be rough.

But reunited with my old roommate and having fried chicken with her made my week 😋
It was another small yet solid piece of evidence that we as humans hold great power to heal each other with care and love.

And reminding myself to be less judgy also helped.

## 2023-07-29

I wonder if the body craving more food after being full comes is related with having food shortage in childhood.

My brain learned at a young age that food is scarcity, it's an important resource that we need to stock up, as much as I can.

One day my PFC might be able to rewire it, to convince the body that we are in safe zone now, that there's enough food, and we can stop eating now.

Breakfast: 2 eggs, 1 cup spinach, 1 cup black beans,
2 KIND peanut butter banana dark chocolate bar,
2 donuts, 1 bagel with cream cheese,
1 insomnia cookie, 1 pork bun,
a few (6 or 7?) bakery snacks,
strawberries

lunch,
half of tuna wrap,
1 chipotle chicken bowl,
1 slice of pizza, 1 pork bun, 1 cookie,
1 donut, 1 bagel with cream cheese,

dinner with friends,
1/4 of the followings:
dan dan noodles, dry chili chicken, chicken stirred fried rice noodle.
2 pan fried pork soup buns, 1 shrimp chive dumpling, 1 pumpkin cake.
1 cookie, 1 granola bar

## 2023-07-22

Cheat day note: carbohydrates are better when you put in some workouts - strength training, or moving.
It really helps replenishing energy.

Normal breakfast: 2 eggs, 1 cup spinach, 2/3 cup beans

1 pretzel knot, 
3 donuts, 
1 black sesame snack stuff, 
1 bagel, 
1 cookie

2 scallion pancakes  , 
1 diet coke, 
mixed veggie, 
spicy soup, 
beefless beef bogoggi , 
1 black sesame snack stuff

1 bagel, 
1 donut, 
1 pork bun, 

6 pieces of fried chicken, 
salad, pickles, 
fries, 
a bit beer

1 donut, 
half of a tuna roll

## 2023-07-15

Cheat day note: binge with friends is so much better than doing it alone.

Normal breakfast: 2 eggs, 80g of spinach, 150g of beans

1 pretzel stick, 
1 pretzel knot, 
2 black sesame snack stuff

2 cookies (1 insomnia big, one small), 
2 and a half donuts, 
half of a bagel

breakfast2: large croissant with eggs and cheese and ham, 
1.75 blueberry pancakes, 
popcorns and chips

1 plain donut, 
2 bagel knots, 
1 slice of pizza, 
brussels sprouts, 
half of a scallion pancake, 
pigs blanket, 
1 bagel

watermelon, 
2 slices of Hawaiian pizza, 
1 eggtart, 
2 segs of garlic bread, 
cinnamon rolls 
