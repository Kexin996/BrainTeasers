# July 15

## PROBLEM

> There are two cities, A and B, 1,000 miles apart. You have 3,000 apples at City A, and you want to deliver as many as possible of them to City B. The only delivery method available is a truck. There are, however, two problems. The truck can hold at most only 1,000 apples, and if there are any apples at all in the truck, the hungry dishonest driver will steal and eat one apple for every mile he drives. What is the maximum number of apples you can deliver from City A to City B? Note that you are welcome to stop part way, dump off some apples, and then come back and pick them up later.



## SOLUTION&#x20;

* this problem is quite interesting
* we know that there are two conditions for the distance with apples the driver drives:
  * the truck can hold at most 1000 apples during driving
  * the driver will eat an apple each time
* for the maximum apples we will deliver, we need to **minimize the distances** **of delivering apples as much as possible and maximize the apples we load each time (1000 apples)**
* there will be some drop point that we can dump the apples and pick them up later.
* The **current** drop point acts like that:
* ...drop point——**drop point**——drop point...
* There will be distance before the drop point and after the drop point.
* after the current drop point: we **must carry apples**, since we gonna "pick them up". Thus, for this distance, the truck can hold at most 1,000 apples and the driver will eat an apple each time.
* before the current drop point: **we can either carry apples or not carry apples**. There is no requirement, and since we want to minimize the distances of delivering apples, we choose not to carry any apple at all.
* Do we know the number of drop points?&#x20;
* no. We only know that after the current drop point we must carry 1,000 apples, which means that the piles of apples at the drop point must be multiple of 1,000.
* Since the distance of carrying apples is the interval between drop points, the difference between the number of apples at two nearby drop points will be the apples eaten by driver.
* We don't want driver to eat a lot of apples, so we want the difference be 1000.
* With those in mind, we know that we will have two drop points:
* 3000(start) ---> **2000** ---> **1000** ---> left(end)
* The distance we drive to to each drop point is the same.
* (3000 - x)\*3 = 2000, and x = 1000 / 3 = 333.3333... (our first point)
* (2000- y)\*2 = 1000, y = 500 (second point).
* The number left = 333.3333+500 = 833.
