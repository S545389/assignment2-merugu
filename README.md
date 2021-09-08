# assignment2-merugu
# Ruchitha Merugu
###### Venice

It is bulit on more than **100 small islands** in a lagoon in the Adriatic Sea. Venice is known for its **bridges**. There are 417 bridges in Venice, and 72 of those are private. Houses in Venice are numbered according to districts, not streets, making is difficult to find addresses, even for postmen. The rule of thumb is to look for a monument, shop, or landmark in close proximity. There are about 350 gondolas and 400 gondalieri in Venice. On average, gondolas are 11 meters long and weigh around 600 kils. In 1608, the Council of Ten approved wearing maks only during the carnival. Those who broke the law were heavily punished. Punishments ranged from two years in prison to public beating and binding to the pillar of shame. There are 177 canals in Venice. The S-shaped Grand Canal is the biggest and splits the city in two. It has **no roads**, just canals. With its **winding canals**, **striking architecture**, and **beautiful bridges**, Venice is a popular destination for travel.

***

# Directions to venice from Maryville( Ordered list)
1. Book a cab to Kansas Airport
    1. To book a cab we need to see available rides in lift
2. Get down in airport
3. Then get an airticket for Venice Treviso airport
    1. Because it is the nearst airport to venice
4. get down in the Venice Treviso airport
    1. The airport is 7.5km from venice 
    2. So book a cab for venice
5. enjoy the trip

* Buy some food
  * snacks
* Buy some swim wear
* Buy cooling glasses

[AboutMe](https://github.com/S545389/assignment2-merugu/blob/main/AboutMe.md)

***

# Food Recommendation

The below table has the food recommendations in maryville city. My personal choice would be croissant which is available in  walmart,chicken nuggets at MCD are delicious. For dinner chicken Biryani at Godavari is tasty with great aroma. Lastly, a shot of coke which is found in walmart would complete the day.

|  food/drink(item)         |   location   |   price   |
|        ----                      |       ---    | ---: |
| croissant                 |    walmart   |   $8.99   |
| chicken nuggets           |     McD      |   $9.00   |
| chicken biryani           |   godavari   |  $25.00   |
| coke                      |   walmart    |   $1.77   |

***

# Quotes

> "Either get busy living or get busy dying" - *STEPHEN KING*

> "Not all those who wander are lost" - *J.R.R TOLKIEN*

***

# Check whether a graph is bipartite
> When modelling relations between two different classes of objects, bipartite graphs very often arise naturally. For instance, a graph of football players and clubs, with an edge between a player and a club if the player has played for that club, is a natural example of an affiliation network, a type of bipartite graph used in social network analysis.Another example where bipartite graphs appear naturally is in the (NP-complete) railway optimization problem, in which the input is a schedule of trains and their stops, and the goal is to find a set of train stations as small as possible such that every train visits at least one of the chosen stations. This problem can be modeled as a dominating set problem in a bipartite graph that has a vertex for each train and each station and an edge for each pair of a station and a train that stops at that station.A third example is in the academic field of numismatics. Ancient coins are made using two positive impressions of the design (the obverse and reverse). The charts numismatists produce to represent the production of coins are bipartite graphs.
Read More <https://en.wikipedia.org/wiki/Bipartite_graph>
```
int n;
vector<vector<int>> adj;

vector<int> side(n, -1);
bool is_bipartite = true;
queue<int> q;
for (int st = 0; st < n; ++st) {
    if (side[st] == -1) {
        q.push(st);
        side[st] = 0;
        while (!q.empty()) {
            int v = q.front();
            q.pop();
            for (int u : adj[v]) {
                if (side[u] == -1) {
                    side[u] = side[v] ^ 1;
                    q.push(u);
                } else {
                    is_bipartite &= side[u] != side[v];
                }
            }
        }
    }
}

cout << (is_bipartite ? "YES" : "NO") << endl;
```
Read More <https://cp-algorithms.com/graph/bipartite-check.html>


