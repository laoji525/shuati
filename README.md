# shuati


937	Reorder Log Files	56.0%	Easy	
重写comparator，对array排序
973	K Closest Points to Origin	61.5%	Medium	
写一个method计算距离的平方，排序，输出
1	Two Sum	44.4%	Easy	
Hashmap记录补数和index，遍历出现补数就输出两个index
5	Longest Palindromic Substring	27.8%	Medium	
写一个method返回从中心开始的最大回文的长度，主method维护一个最大长度和起点start，当helper长度大于maxlen了，记录回文的start index，return起点加maxlen的substring
146	LRU Cache	26.8%	Medium	
用linkedhashmap实现congstructor（capacity，0.75f，true），override Boolean removeEldestEntry（map.Entry <Integer， Integer> eldest）return super.size() > capacity
200	Number of Islands	42.5%	Medium	
遍历二维数组，当出现1，ans++然后进dfs，dfs把当前点四周的1都变成0，dfs结束条件是到边界或者到0
819	Most Common Word	42.4%	Easy	
遍历string，判断char是不是letter，如果是加进stringbuilder，否则就是一个完整的word，把word放进hashmap，记录频率，维护一个最大频率，当当前word大于等于maxfreq，ans=当前word，遍历完，返回ans
763	Partition Labels	71.8%	Medium	
遍历一遍string记录每个字母的最后一次出现的index，再做一个遍历，维护一个start和当前substring的最大lastIndex，当lastIndex==i的时候，start到i的string放进ans，start=i+1;最后返回ans
103	Binary Tree Zigzag Level Order Traversal	42.8%	Medium	
Bfs遍历bt，用一个for循环维护同一层的节点，同一层的节点放进一个list，维护一个boolean是否要反转，进行collections。Reverse，同一层的放进ans，最后返回ans
957	Prison Cells After N Days	37.5%	Medium	
直接模拟，会出现循环，N从大到小减
42	Trapping Rain Water	44.2%	Hard	
双指针，左右一起遍历，左右当前高度低的先做，ans+=高度差，左右指针碰到就结束，返回ans
23	Merge k Sorted Lists	35.6%	Hard	
用一个pq存listNode，override comparator，把每个listNode放进pq，pq的第一个肯定是val最小的，把头拿出来，放进新的dummy listNode, 再把下一个节点放进pq一直到pq为空为止，返回dummy
2	Add Two Numbers	31.6%	Medium	
新建一个dummy listNode，声明一个carry和sum，当l1或l2不为空或carry不为零，进while循环，sum是两个node点val相加，carry是sum的十位数，新建node curr用sum的个位，两个listnode都到下一个节点，返回dummy。Next
909	Snakes and Ladders	35.0%	Medium	
写一个help method，左上从0开始是坐标，左下从1开始是游戏的序号，用bfs从左下开始遍历遍历,中间for循环是1-6的步数，当前点不是-1就到目标点，当用一个hashmap记录节点的最小步数，当走到终点，返回终点的步数
472	
Concatenated Words	36.2%	Hard	
165	Compare Version Numbers	24.3%	Medium	
先放进string array里， Length是两个的最大长度，for循环到length，两个当前string都转Integer，没有就给0，两个integer比较大小，出现不一样就返回compare的值
127	Word Ladder	25.1%	Medium	
写两个help method， 一个replace string里index上的char，另一个生成给的string能到的下一个word的所以的arraylist每个char都从a到z进行替换，如果在set里就放进arraylist，主method一个set存word，一个set存路径，一个queue做bfs，声明一个步数，用size的for循环，进行同一个word的遍历，用for循序在nextwords里遍历，如果能找到目标word就直接返回步数，如果路径里有word，就跳过，否则queue放进word，路径也放进word，最后返回零
139	Word Break	36.2%	Medium	
用dp，dp[0]是true，用一个set存words，双指针遍历，当前一个dp[j]是true同时往后的word在dict里，dp[i]就为true然后break小循环，最后返回最后一个dp
138	Copy List with Random Pointer	28.3%	Medium	
Deep copy一个linkedlist，用hashmap，存旧的node和新建一个node，再做一次遍历对新的node进行链接，最后返回hashmap里的value
269	Alien Dictionary 31.8%	Hard	

126	Word Ladder II	18.5%	Hard	

297	Serialize and Deserialize Binary Tree	42.1%	Hard	
两个都用dfs，都用preorder遍历，都写一个help method帮助递归，serialize用stringbuilder，每次递归都往后append当前节点的val，deserialize用一个list存每个string作为node，如果list的0是零就返回null节点，否则新建新节点val是list 0，再对当前节点的左右进行preorder遍历
772	Basic Calculator III 42.1%	Hard	

207	Course Schedule	38.8%	Medium	
拓扑排序+BFS；用arrayList的数组构建图，int的数组做indegree，index就是课号，声明一个queue做bfs，一个count记录满足条件的课的数量；第一个for循环先new graph的每个arrayList；第二个for循环构建indegree和graph；第三个for循环遍历indegree，没有上家的课放进queue里count加一；while循环开始做bfs，queue拿出第一个course，for循环遍历在同一门课的下家，在indegree里减一，如果indegree这门课是0，就是满足条件的课，放进bfs，count加一；while结束最后返回count是否等于numCourses
295	
Find Median from Data Stream	38.0%	Hard	
642	
Design Search Autocomplete System
39.0%	Hard	
545	Boundary of Binary Tree35.8%	Medium	
三次dfs遍历，左边界和叶子用preoreder，右边界用postorder
1000	
Minimum Cost to Merge Stones	34.3%	Hard	
505	The Maze II44.9%	Medium	
Bfs遍历，一个二维boolean array记录是否到过，
348	Design Tic-Tac-Toe 50.5%	Medium	
1玩家是+1，2玩家是-1，row的array，col的array，两个对角线出现数字加起来abs==size时候出现胜者
273	Integer to English Words	24.7%	Hard	
小于20一个array，整十一个array，billion以上，million以上，thousand以上，thousand以下，分别加到string里
863	All Nodes Distance K in Binary Tree	49.3%	Medium	
先用dfs遍历整个bt，建一个 map，key是节点，value是一个list包含左右节点和父节点，从target节点开始bfs遍历左右和父节点，用一个for循环遍历同一层，当层数到达K了，把所有节点放进list里返回list
253	Meeting Rooms II 43.3%	Medium	
把start和end分别放进两个array，排序，遍历start，维护一个end的index，如果start大于等于当前index的end，不加新房间，index++，否则加新房间
341	Flatten Nested List Iterator	48.9%	Medium
用arrayDeque实现stack，override next和hasnext，在声明一个tmp stack，先把nestedIterator放进tmp里，再把tmp放进stack里	
675	
Cut Off Trees for Golf Event	31.4%	Hard	
124	
Binary Tree Maximum Path Sum	30.7%	Hard	
588	
Design In-Memory File System
41.0%	Hard	
4	
Median of Two Sorted Arrays	27.0%	Hard	
733	Flood Fill	51.5%	Easy	
Dfs从起始点向四个方向遍历，原来的颜色换新颜色，到边界或者颜色不符就停
121	Best Time to Buy and Sell Stock	48.0%	Easy	
维护int最小价格和最大利润，遍历数组，计算当前的利润，输出最大利润
45	Jump Game II	28.6%	Hard	
1．Dp记录每个点能到的最小步数，用两个for循环，返回最后dp最后一个////超时
2. 贪心。类似763，从头开始遍历，当index达到最远点，就选这个点，
3，贪心另一种写法，bfs思想，走到最远点
15	3Sum	24.6%	Medium	
先排序，for循环遍历，当前数字为第一个数，在当前数往右找，和167一样，题目要求没有重复，因为是排序过的，和下一个一样就是重复，跳过，最后返回res
21	Merge Two Sorted Lists	48.5%	Easy	
While循环，l1和l2不为空，比节点大小，tmp的next连小的，最后把剩下的l1或者l2连上tmp，最后返回dummy的next
692	Top K Frequent Words	46.7%	Medium	
用hashmap存每个word出现频率，把key放进arraylist用collections sort排序arraylist，重写comparator，先比频率，一样的话再比字母，最后返回sublist从0到k
380	
Insert Delete GetRandom O(1)	43.5%	Medium	
49	Group Anagrams	48.6%	Medium	
用一个hashmap存，key是排序后的string，value是list，里面是每个anagram的string，最后声明一个arraylist用hashmap的value，返回这个list
212	
Word Search II	29.6%	Hard	
340	
Longest Substring with At Most K Distinct Characters
40.6%	Hard	
3	Longest Substring Without Repeating Characters	28.7%	Medium	
Sliding window, hashmap存char最后出现的位置，声明start位置和longest长度，遍历string，如果当前char出现过并且比start大，start=当前+1，每次计算longest长度，把当前c放进map里，最后返回longest
314	Binary Tree Vertical Order Traversal 41.6%	Medium	
用map存列数和list，list存每个节点的值，一个queue存node用来bfs遍历，一个queue存col#，和queue和map同步操作，左减右加，map存col#和list，最后返回map的values
239	
Sliding Window Maximum	39.0%	Hard	
155	Min Stack	38.3%	Easy	
写双向链表实现stack，维护min的node，写一个method找到min的node
994	Rotting Oranges	46.4%	Easy	
把二维坐标转成一个code代码，queue存code用来bfs，map存code和腐烂的天数，维护一个最大天数，最后再遍历一次grid，如果有fresh的就返回-1，最后返回天数
540	Single Element in a Sorted Array	57.4%	Medium	
数学问题，array基数个，定位到中间，取中位数和后一个数比较，可以排除掉一半的数，start 大于等于end，结束while循环
206	Reverse Linked List	56.2%	Easy	
三个node操作，curr存当前，head推进，prev存前一个，curr的next指向prev，prev推进到curr，一直到head到最后null
140	
Word Break II	27.9%	Hard	
387	First Unique Character in a String	50.5%	Easy	
String转成char []， 一个int[]存26个字母的频率，遍历char[]，频率为1返回index，最后返回-1
460	
LFU Cache	29.6%	Hard	
56	Merge Intervals	36.3%	Medium	
把interval进行array排序，重写comparator，维护newInter，for循环遍历intervals，当当前开始时间小于等于newInter的结束时间，就出现overlap，改写newinter，否则没有overlap，res加进这个array，newInter改为当前interval，最后返回array的结果
79	Word Search	32.1%	Medium	
两个for循环遍历二维array，进dfs遍历，维护index，进下一个字母index加一，到过的字母改成#标记为到过，遍历完在还愿字母，boolean用or连接
76	
Minimum Window Substring	31.6%	Hard	
997	Find the Town Judge	49.5%	Easy	
找法官，法官不信任何人，法官被除了自己的人都相信，遍历找到就行
20	Valid Parentheses	37.1%	Easy	
用stack存char，遍历char数组，前括号就放进后括号，后括号就和pop出来的比较，如果是一样就没事，否则返回false，最后返回stack isempty
33	Search in Rotated Sorted Array 33.1%	Medium	

还是二分搜索，先判断最左边值和中间值，如果小的就是正常的二分搜索，否则拐点在这个区间，反转二分搜索就行
12	Integer to Roman	51.8%	Medium	
弱智题，string array写0-9，10-90，100-900，结果加mod和除
53	Maximum Subarray	44.3%	Easy	
DP题，从index 1开始遍历，如果前一个是正的就加到当前，最后在array里找最大值，返回
992	
Subarrays with K Different Integers	44.9%	Hard	
560	Subarray Sum Equals K	42.7%	Medium	
1BF
2. 用map记录sum，用sum，k, sum – k, 思想是 i到j等于0到i减0到j，map value存频率，遍历array，计算sum，key出现sum-k就是要的值， res+value更新sum的频率，最后返回res
347	Top K Frequent Elements	56.1%	Medium	
用hashmap记录数字出现的频率，建一个pq，重写comparator，根据频率从大到小排序，把hashmap的key存进heap，循环做k次，poll到res里，返回res
993	Cousins in Binary Tree	52.2%	Easy	
两个判断条件，depth一样，parent不一样，method外面声明x和y的depth和parent node，dfs遍历，输入当前node和parentnode，找到x和y node，把depth和parent node赋值，最后比较x和y的depth parent
773	
Sliding Puzzle	53.6%	Hard	
238	Product of Array Except Self	56.1%	Medium	
不能用除法，先左到右遍历，算出从最左到i前一个的所有的乘积，再从右到左遍历，乘以右到左的所有的乘积，返回res
490	The Maze 48.3%	Medium	
只用返回能不能到，bfs，queue存int[] 为当前点的坐标，boolean二维数组存这个坐标有没有到过，点到了终点就返回true，while里套for循环4个方向，再套一个while循环让next点走到最远，放进boolean数组和queue，最后返回false
17	Letter Combinations of a Phone Number	42.6%	Medium	
Backtrack，写一个map，每个数字对应的字母，回溯输入当前的字母组合和剩下的数字，当后面没有数字了就把字母放进res，else拿出下一个数字找到对应的几个字母for循环进每个字母，进递归
199	Binary Tree Right Side View	49.0%	Medium	
1BFS， treeNode放进queue，while里用for维护同一层的node，当走到同层最右的时候放进res，注意放进queue的左右顺序
2DFS，dfs输入层数，当层数正好大于res的size 1的时候就是进新的一层，把当前的node放进res，返回res
289	Game of Life	47.1%	Medium	
两个for循环进行二维数组遍历，再对8个方向进行遍历，记录周围八个状态，判断变成死还是变成活，变活+10，变死+0，当前状态大于等于10就是活否则死，之前状态mod 10,0是死，1是活，遍历完之后，再做一次二维遍历，把当前状态改成1或0
503	Next Greater Element II	51.8%	Medium	
1BF两次遍历向右边，找到第一个比当前大的就加进res，返回res
2用单调栈stack优化，从右往左做两次遍历，stack存index，stack不为空and stack顶上的数小于等于当前数，pop掉，如果stack最后为空就给res -1，否则给他这个值，再把当前的index push进stack，最后返回res
516	Longest Palindromic Subsequence	47.9%	Medium	
DP，先话图吧，n x n的表格，对角线都是一，两个for循环，第一个循环控制字符串长度用d，第二个循环控制r的值，r表示左边的char，c表示右边的char c = r + d，当左右一样，dp[r][c] 结果是他的左下角格子加2，否则就是他的左边或者下边的max，结束循环返回右上角的值
716	Max Stack 40.6%	Easy	
写双向链表，维护max的node，写一个method找到最大node，别的和stack一样
943	
Find the Shortest Superstring	38.6%	Hard	
983	Minimum Cost For Tickets	57.6%	Medium	
DP题，先找一下最后一天是哪一天，建DP[]，长度是最后一天加一，dp[0]是0，建一个boolean array记录有没有买票日，for循环从第一天开始遍历到最后一天，如果这天不买票，这天就是前一天的钱，否则转移方程，dp前一天的钱加cost[0],dp前7天加cost[1],dp前30天加cost[2]，这三个里去最小的那个，天数如果减完是负数就取0，最后返回DP最后一天
1091	Shortest Path in Binary Matrix	36.5%	Medium	
BFS，用for循环遍历同一级坐标，二维数组visisted记录是否走过，for循环8次8个方向，如果走到终点返回level+1，while结束返回-1
323	
Number of Connected Components in an Undirected Graph
52.7%	Medium	
362	
Design Hit Counter
59.7%	Medium	
428	
Serialize and Deserialize N-ary Tree
55.1%	Hard	
11	Container With Most Water	46.1%	Medium	
左右双指针，计算每次的面积，高度取小的那个，while 左小于右，哪边高度小先缩哪边，每次都比较最大面积，最后返回最大面积
167	Two Sum II - Input array is sorted	51.1%	Easy	
双指针左右index，while里面，左右加起来比target小，左++，否则右-1，最后返回左右的index
538	Convert BST to Greater Tree	52.0%	Easy	
中序dfs遍历，有节点不用加，中加右，左加中，外面声明sum=0，先走右节点，然后改当前节点val为sum += 当前节点val，再走左节点
22	Generate Parentheses 56.5%	Medium	
回溯，递归输入当前string，还剩左括号数量，和右括号数量，当左右括号用完就把string放进res，else如果左小于等于右加一，string加一个左括号，数量-1，如果左小于等于右减一，string加一个右括号，右数量-1，最后返回res
57	
Insert Interval	31.6%	Hard	
394	Decode String	45.9%	Medium	
 用两个stack，一个存数字一个存string，遍历string，总共4种情况，1）数字，把数字记录下来；2）前括号，把当前数字存进stack，把当前string存进stack，把数字和string都初始化；3）后括号，说明一个tmp字符串，把数字和string从stack拿出来，用for循环把字符串重复，4）字母，就把当前字母放进当前的string；最后返回当前的string
333	
Largest BST Subtree
33.6%	Medium	
102	Binary Tree Level Order Traversal	49.7%	Medium	
BFS遍历，queue存treenode，while里用for循环维护同一层的treenode，把同一层的treenode放进一个level的list里，for做完把level放进res里，最后返回res
759	
Employee Free Time
62.2%	Hard	
64	
Minimum Path Sum	48.1%	Medium	
572	Subtree of Another Tree	42.0%	Easy	
100题sameTree的变种，大树进左树递归or右树递归or进sameTree
116	Populating Next Right Pointers in Each Node	38.9%	Medium	
同117，BFS遍历，for循环同层操作
215	Kth Largest Element in an Array	49.2%	Medium	
用pq存int，输出第k个大的int，就这样
895	
Maximum Frequency Stack	57.1%	Hard	
695	Max Area of Island	58.3%	Medium	
二维for循环遍历grid，有1进 Dfs遍历grid，把1改成0，dfs返回area，维护maxA，循环结束返回maxA
528	
Random Pick with Weight	43.0%	Medium	
543	Diameter of Binary Tree	47.3%	Easy	
找最长路径，外面声明一个max，一个点的最长路径就是他的左树的最长路径加右树的最长路径加一，dfs遍历整个树，计算每个点的最长路径，每个都和max比较，最后返回max
430	
Flatten a Multilevel Doubly Linked List	43.4%	Medium	
117	Populating Next Right Pointers in Each Node II	35.2%	Medium	
BFS遍历，用for循环对同层操作
710	
Random Pick with Blacklist	32.0%	Hard	
93	
Restore IP Addresses	32.2%	Medium	
843	
Guess the Word	44.4%	Hard	
653	Two Sum IV - Input is a BST	53.1%	Easy	
用hashset存补数，出现就返回true，左右两边都要进
1046	Last Stone Weight	61.9%	Easy	
Priorityqueue存integer，重写comparator按大到小排列，做length-1次的循环因为要留最后一个石头，拿出两个，第一个减第二个，再放回heap，最后return pq的poll
708	
Insert into a Cyclic Sorted List
29.8%	Medium	
388	
Longest Absolute File Path	39.5%	Medium	
498	
Diagonal Traverse	45.7%	Medium	
703	Kth Largest Element in a Stream	46.9%	Easy	
Pq, capacity为k，第k个大的就是第一个
346	Moving Average from Data Stream 67.1%	Easy	
Design一个class，用queue实现，class有capacity和sum，next method当size等于capacity了，poll掉最早的，然后sum除以queue的size
300	Longest Increasing Subsequence	41.2%	Medium	
Dp题，最好画个图，一维数组，index一致，dp{0} = 1，声明一个res=1存最大长度，从1开始遍历，再套一个for循环从0到j遍历，声明一个子序长度为0，当i的值大于j的值，sub取dp j的和sub的最大值，j结束，dp i就是sub的长度加1，res取最大值，最后返回res
694	Number of Distinct Islands	52.1%	Medium	
DFS回溯，用set记录path，path用string表示上下左右，因为二维数组遍历肯定都是从左上角开始的，dfs的顺序也是固定的，所以path一样的他们的string也是一样的，但是要在每次回溯做完加string后面加一个标记，最后返回set的size
353	
Design Snake Game
31.2%	Medium	
149	
Max Points on a Line	16.0%	Hard	
135	
Candy	29.0%	Hard	
91	Decode Ways 22.7%	Medium	
Dp题，注意dp的index比string的index多一位，从idx2开始遍历，分别去前一位的integer oneD和前两位的integer twoD，如果oneD是1到9，dp[i] 加等前一位dp，如果twoD是10到26，dp[i] 再加等前两位的dp，最后返回dp数组的最后一位
236	Lowest Common Ancestor of a Binary Tree	38.9%	Medium	
分治递归，用DFS遍历BT，到null就返回null，如果p或q找到就返回当前node，判断有3种情况，1.如果返回的左和右都是非null，说明当前node就是要的LCA；2.如果左是null说明pq不在左边返回右node；3.如果右是null说pq不在右边，返回左node
489	
Robot Room Cleaner
65.7%	Hard	
98	Validate Binary Search Tree	26.1%	Medium	
中序遍历一个bst，val一定是从小到大的；所以中序遍历这个bst，放进list里，在遍历list看是否是有序的
55	Jump Game	32.4%	Medium	
1. DP题，dp 0 为true，两个for循环遍历，i从1到最后，j从0到i，如果dp[j]为true并且dp[j]+j的结果大于等于i，说明能走到i，dp[i]就为true，最后返回dp最后一位
2.贪心思想，从后向前遍历，声明一个lastPos存能走到的最左边位置初始是最后一位，for循环如果当前位置能覆盖到lastPos，lastPos改成当前i，最后返回lastPos是否为0
188	
Best Time to Buy and Sell Stock IV	26.7%	Hard	
787	
Cheapest Flights Within K Stops	35.8%	Medium	
706	Design HashMap	56.8%	Easy	
就用int array存，key的hashcode做index，写一个method计算这个index，constructor里用array fill用-1填满，put get remove都先算index，然后对array操作就行
384	
Shuffle an Array	50.7%	Medium	
900	
RLE Iterator	50.8%	Medium	
432	
All O`one Data Structure	30.2%	Hard	
1022	Sum of Root To Leaf Binary Numbers	58.9%	Easy	
二进制转十进制加分，sum乘二加当前数，外面声明一个total，dfs递归，输入treenode和sum，当走到叶子，total加sum，dfs走左和右，同时进行二进制转十进制加法
252	Meeting Rooms 52.6%	Easy	
Array排序重写comparator按开始时间，然后遍历数组，如果当前的结束时间大于了下一个的开始时间，就返回false，结束后返回true
210	
Course Schedule II	35.9%	Medium	
227	
Basic Calculator II	34.2%	Medium	
662	
Maximum Width of Binary Tree	39.5%	Medium	
508	
Most Frequent Subtree Sum	55.2%	Medium	
361	
Bomb Enemy
44.0%	Medium	
767	
Reorganize String	43.5%	Medium	
268	Missing Number	49.0%	Easy	
1Xor 操作，a^b^b = a, 所以遍历一遍nums，xor^i^nums[i],最后xor^length的就是missnumber
2 sum = num。length，遍历整个数组，sum加idx，减nums[i]，最后sum剩下的就是missnumber
535	Encode and Decode TinyURL	77.4%	Medium	
就用hashcode，map存，code做key integer，longurl做value string，encode put进map，decode get map
40	
Combination Sum II	43.0%	Medium	
225	Implement Stack using Queues	40.4%	Easy	
同232，stack有top，不同的是top会一直变，选择改push用n时间实现，别的和queue一样
32	
Longest Valid Parentheses	26.1%	Hard	
25	
Reverse Nodes in k-Group	37.5%	Hard	
847	
Shortest Path Visiting All Nodes	47.8%	Hard	
13	Roman to Integer	53.0%	Easy	
写一个method字母转int，用switch case，从0遍历到最后第二个，记录curr和next，next比curr小与等于就加当前，否则减当前
449	
Serialize and Deserialize BST	48.3%	Medium	
134	
Gas Station	34.7%	Medium	
1026	
Maximum Difference Between Node and Ancestor	61.0%	Medium	
62	
Unique Paths	48.7%	Medium	
88	Merge Sorted Array	36.5%	Easy	
给了nums1和nums2的长度，减一就是各自的index，总index是长度加起来减一，while循环比大小从后面放进nums1，nums1没到0不用管，nums2没到0的话再用一个while循环把剩下的nums2放进nums1
208	Implement Trie (Prefix Tree)	39.9%	Medium	
先建一个TrieNode的class，node里存一个node的array，links连接26个字母，一个boolean值是否是最后一个字母，有method Boolean containsKey（char ch），TrieNode get（char ch）, void put (char ch, TrieNode node), void setEnd(), boolean isEnd(); Trie class 里constructor trie，有一个root，method insert（string word），遍历每个char，把每个char放进trieNode，node = 下一个node，写一个searchPrefix method，返回一个前缀是word的trieNode，search method用searchprefix method，判断返回的node是否为空，node是否能做结尾，startwith同样用searchprefix method，不要判断能否做结尾了
636	
Exclusive Time of Functions	49.2%	Medium	
78	Subsets	54.4%	Medium	
回溯题，DFS递归，DFS里先把tmp list加进res，然后for循环从start 开始到最后一位，把start位的数字加进tmp，然后进递归，递归结束把这个数字remove掉，最后返回res。
529	
Minesweeper	54.0%	Medium	
6	ZigZag Conversion	32.9%	Medium	
用stringbuilder操作，每行一个sb，一个boolean goDown判断是不是向下，currRow记录当前行数，初始是0，遍历string，加进这行的sb里，当行数是0或者最后一行，goDown翻一下，行数根据goDown加或减，最后输出toString
445	
Add Two Numbers II	50.9%	Medium	
640	
Solve the Equation	40.6%	Medium	
7	Reverse Integer	25.5%	Easy	
Mod和乘10，加进res，每次判断一下下一步会不会超过integer范围，是就返回0，最后返回res
101	Symmetric Tree	44.1%	Easy	
Dfs遍历，放进两个root，判读node的val，两个分别进左进右，用and连接boolean，
1044	
Longest Duplicate Substring	22.5%	Hard	
556	Next Greater Element III	30.3%	Medium	
和31题一模一样
133	
Clone Graph	27.8%	Medium	
240	Search a 2D Matrix II	41.2%	Medium	
从右上角开始二维数组遍历，如果当前是target返回true，如果当前小于target，row++，如果当前大于target，col--；最后返回false；
854	K-Similar Strings	34.7%	Hard	
其实本质上是排序，B是目标string，BFS遍历，用set记录visit是string，双指针，for循环同层遍历，做完for循环res+1，i是换的index，j是被换的index，i每次走到第一个unsorted的位置，j从i开始找到满足条件能交换的位置，把i和j交换然后进行判断，下一步遍历还是返回
150	
Evaluate Reverse Polish Notation	33.0%	Medium	
322	Coin Change 31.4%	Medium	
DP bottom up; dp[0] = 0, 初始值设amount+1， 两个for循环从1开始，里面的for遍历coins，转移公式是dp[i] , dp[i – coin] + 1 取最小值 ,最后返回dp最后一位，如果是amount+1的话就返回-1
298	
Binary Tree Longest Consecutive Sequence
44.6%	Medium	
36	Valid Sudoku	44.3%	Medium
Row col subbox 3 x 9 个array，subbox 的index = row / 3 * 3 + col / 3 每个array存hashmap， key是数字， value是出现的次数，做一遍遍历，出现2就返回false
	
211	
Add and Search Word - Data structure design	31.4%	Medium	
68	
Text Justification	24.0%	Hard	
442	
Find All Duplicates in an Array	61.9%	Medium	
312	
Burst Balloons	48.2%	Hard	
525	
Contiguous Array	43.2%	Medium	
185	
Department Top Three Salaries	27.5%	Hard	
8	
String to Integer (atoi)	14.8%	Medium	
987	
Vertical Order Traversal of a Binary Tree	32.1%	Medium	
336	
Palindrome Pairs	31.6%	Hard	
164	
Maximum Gap	33.1%	Hard	
228	
Summary Ranges	36.6%	Medium	
105	Construct Binary Tree from Preorder and Inorder Traversal	42.6%	Medium	
 要画图看，preorder的第一个肯定是root，然后在inorder里找到他，他的左边一定是他的左树，右边是右树，所以主要是三个位置，preoder的起始点就是当前节点的val，inorder的起始点和终点就是他下一个结点所需要的所有val；用递归建树；递归结束的判断是preoder或者inorder用完；先new当前node，然后for循环遍历在inorder里找到对应的val的index，然后递归左树和右树，比较难想的是右节点的preStart，当前preStart加左树的长度加一，画图能看出来
//优化：先把inorder的值和位置放进hashmap里，就不用每次都遍历一遍inorder，时间复杂度从O(n^2)降到O(n)
980	
Unique Paths III	71.2%	Hard	
70	Climbing Stairs	44.8%	Easy	
Dp题，转移方程是前两个相加，空间复杂度是n，可以只用两个int记录，space就只用1
224	
Basic Calculator	33.6%	Hard	
785	
Is Graph Bipartite?	44.3%	Medium	
99	
Recover Binary Search Tree	35.4%	Hard	
59	
Spiral Matrix II	47.8%	Medium	
14	Longest Common Prefix	34.0%	Easy	
就用第一个string做参照，声明一个pre，第一个for循环遍历string，取char，套一个for循环遍历strs数组，如果当前string大于pre长度，或者当前char和string1的char不符，就返回pre，如果每个string都符合，把这个char加进pre，结束返回pre
48	Rotate Image	50.0%	Medium	
把数组对角线交换，再水平交换，就是90度旋转
780	
Reaching Points	27.8%	Hard	
352	
Data Stream as Disjoint Intervals	44.1%	Hard	
443	String Compression	38.2%	Easy	
双指针，一个记录遍历的index，一个记录结果的index，while循环遍历array，count=0记录次数，用小的while循环记count，先写下当前char,因为结果要求integer也要拆分每一位，把count转成charArray，用for循环遍历，放进chars，因为最后操作是ans++，所以直接返回ans
635	
Design Log Storage System
55.6%	Medium	
438	Find All Anagrams in a String	38.0%	Medium	
双指针滑动窗口问题，用一个int array存26个字母的频率作为hashtable；start是窗口的左边end是右边，用diff表示还需要多少个字母能满足条件；先把end移动到target的长度的位置，同时看有没有满足条件放进res；然后是while循环滑动窗口，先看左边是不是符合的字母，是的话diff加一，hashtable加一左边右移一位，然后看右边，hashtable先减一，然后看频率是否大于0，是的话说明符合条件是anagram的一部分，diff减一，如果diff是0，当前窗口是anagram，左边放进res，然后右边右移一位；最后返回res
778	
Swim in Rising Water	48.6%	Hard	
1019	
Next Greater Node In Linked List	57.0%	Medium	
287	Find the Duplicate Number	50.6%	Medium	
二分搜索，mid是中位数，给的数组是从1到n，所以多出来的那个数会让mid左或右的density变大，用一个for循环遍历数组记多少个数不大于mid，然后把mid给low或者high，最后返回low
929	Unique Email Addresses	69.4%	Easy	
String操作，用set存unique邮箱，split分割@，后面的是domian，split分隔+，只取0，再拼成email放进set，最后返回set。Size（）；
96	Unique Binary Search Trees	47.3%	Medium	
数学DP题，画图，从1到n；0做root是1个，1root是1个；2做root，左树一个，右0个然后+=1做节点的结果；3做root，左树两个，右0个，加等2做root，左树一个右树一个，加等1做root，左树0右树2个；当i=3，3组树是2-3-0， 1-2-1， 0-1-2；当i=4，4组树是3-4-0，2-3-1，1-2-2，0-1-3；所以代码是两个for循环i2到n，j1到i，转移方程dp i += dp j - 1 * dp i - j；最后返回dp最后一位；
402	
Remove K Digits	26.9%	Medium	
742	
Closest Leaf in a Binary Tree
40.1%	Medium	
1086	High Five74.8%	Easy	
结果先按学生id排，然后算每个学生的top5分数的平均数，用一个treeMap存，key是学生id，value是一个pq，pq里存学生的分数，并且当pq大于5了就pop掉一个，然后遍历map的keyset，这里注意score不一定是5个，要取pq的size来算平均数，然后把id和平均数放进res里，最后返回res
16	
3Sum Closest	45.8%	Medium	
153	
Find Minimum in Rotated Sorted Array	43.4%	Medium	
726	
Number of Atoms	45.5%	Hard	
39	Combination Sum	50.1%	Medium	
回溯，思想和17题一样，dfs递归，把target减到0了，就把当前的list放进res，每次for循环从当前index向右遍历，如果target大于等于0，当前数字加进list，进dfs，把target减当前数字，做完dfs要把最后list最后的数remove掉
426	
Convert Binary Search Tree to Sorted Doubly Linked List
53.6%	Medium	
564	
Find the Closest Palindrome	19.0%	Hard	
924	
Minimize Malware Spread	40.5%	Hard	
797	
All Paths From Source to Target	71.1%	Medium	
344	Reverse String	63.8%	Easy	
这要不会写 回家种田吧
1032	
Stream of Characters	42.4%	Hard	
30	
Substring with Concatenation of All Words	24.0%	Hard	
34	Find First and Last Position of Element in Sorted Array	34.0%	Medium	
做两次二分搜索第一次找左边界，第二次找右边界，把大于等于小于的三种情况都写出来，第一次while的最后low就是左边界，第二次while，low不动，high还原成n-1，计算mid的时候+1，最后high就是右边界，做完第一个while先判断是否找到target，否则直接返回{-1，-1}
267	
Palindrome Permutation II
34.2%	Medium	
637	Average of Levels in Binary Tree	59.5%	Easy	
BFS遍历，用for循环维护同一层，sum/size加进res，最后返回res
986	
Interval List Intersections	63.8%	Medium	
250	
Count Univalue Subtrees
49.8%	Medium	
83	Remove Duplicates from Sorted List	43.2%	Easy	
While 循环，当前node的val等于next 的val，就把当前的next只想next。Next
1099	Two Sum Less Than K 61.7%	Easy	
和sorted two sum一样，先排序，一个max记录max的sum，最后返回max
417	
Pacific Atlantic Water Flow	38.1%	Medium	
261	
Graph Valid Tree
40.3%	Medium	
1120	
Maximum Average Subtree
60.6%	Medium	
507	Perfect Number	34.8%	Easy	
从1遍历到n的开方，找因数，用n/因数能直接得到一对因数，加进sum，最后==判断
162	
Find Peak Element	41.7%	Medium	
496	Next Greater Element I	60.3%	Easy	
单调栈，遍历nums2，用单调栈找到每个数的下一个数，放进hashmap里，遍历nums1，把结果放进res，最后返回res
136	Single Number	61.1%	Easy	
A^b^b = a; bit操作，res ^当前n，最后剩的res就是single number
1010	Pairs of Songs With Total Durations Divisible by 60	45.7%	Easy	
Two sum 变种，把数字%60，就是two sum，k是60，用hashmap做
75	Sort Colors	42.9%	Medium	
题目要求是计数排序，就是记录多少个0，1，2，然后在原数组里填上数字；followup要求onepass，就一次for循环遍历，用双指针；遍历时候三种情况，0swap，i进一位，left右移；1，i进一位；2swap，i不动，right左移
176	Second Highest Salary	28.0%	Easy	
用 limit 和offset
234	Palindrome Linked List	36.8%	Easy	
双指针，一个slow一个fast，fast走到头，slow就到中间，这里判断一下奇偶，fast为空节点，说明是是偶数个，让slow再多走一步，然后slow整个反转，fast指向head，然后两个同步走，val不同就返回false，最后返回true
316	
Remove Duplicate Letters	33.2%	Hard	
1083	
Sales Analysis II
51.4%	Easy	
171	Excel Sheet Column Number	52.1%	Easy	
遍历每个字母，距离最右多少位就是26的指数，再乘字母代表的数字，这里A是1，所以-‘A‘以后要再加1，加进res里，最后返回res
137	
Single Number II	46.8%	Medium	
904	
Fruit Into Baskets	41.8%	Medium	
281	
Zigzag Iterator
56.4%	Medium	
412	Fizz Buzz	60.0%	Easy	
1遍历到n，可以用两个int代表3和5，每次走到3 5 同步加，可以用来代替%
358	
Rearrange String k Distance Apart
33.3%	Hard	
283	Move Zeroes	54.9%	Easy	
只记录最左的zero的index，遍历array，当不是0，把当前和zero换
205	Isomorphic Strings	37.9%	Easy	
声明两个int array[] 做s 和t每个字母的map，遍历s和t，如果map1和map2指向不同的值就返回false，否则记录map的值到当前i+1，（为了避免0），最后返回true
19	
Remove Nth Node From End of List	34.5%	Medium	
169	Majority Element	53.7%	Easy	
1因为一定存在majority，排序array，majority就是中间数
2 用hashmap存数字频率，majority的频率大于nums。Length / 2，遍历keySet（），找到这个key返回
286	
Walls and Gates
50.2%	Medium	
355	
Design Twitter	27.9%	Medium	
1023	
Camelcase Matching	56.2%	Medium	
541	Reverse String II	45.9%	Easy	
写两个help method，一个反转char[]， 一个swap method，主method，先把s转成char[]，for循环遍历array，i每次加2k，把start和end传进help method，如果end超过长度-1就传长度-1，最后返回string
177	
Nth Highest Salary	27.3%	Medium	
332	
Reconstruct Itinerary	32.3%	Medium	
152	
Maximum Product Subarray	29.8%	Medium	
28	
Implement strStr()	32.7%	Easy	
277	Find the Celebrity 37.8%	Medium	
假设0是c，从1开始遍历到n-1，只要i认识c，c = i；找到这个c；第二遍for循环确认，从0到n-1遍历，如果不符就返回-1，结束返回c
301	
Remove Invalid Parentheses	40.0%	Hard	
349	Intersection of Two Arrays	56.1%	Easy	
1 如果是sort，双指针，数字一样放进array，重复数字就跳过，哪边数字小哪边先++，最后返回array
2如果不是sort，用两个set
31	Next Permutation	30.9%	Medium	
降序排列的数没有下一个，所以从右往左找到第一个不是降序排列的数，再找到右边比他大的最小的一个数，交换，右边一直是降序排列，右边reverse一下就行了
218	
The Skyline Problem	32.2%	Hard	
978	
Longest Turbulent Subarray	45.7%	Medium	
407	
Trapping Rain Water II	39.7%	Hard	
143	
Reorder List	31.9%	Medium	
9	Palindrome Number	44.5%	Easy	
负数或者非0的0结尾的都返回false，把x翻过来，返回两个数==
1051	
Height Checker	69.0%	Easy	
272	
Closest Binary Search Tree Value II
46.1%	Hard	
230	
Kth Smallest Element in a BST	52.8%	Medium	
729	
My Calendar I	48.2%	Medium	
204	Count Primes	29.6%	Easy	
Boolean array做hashmap记录是不是prime，从2遍历到n，填hashmap，记录res，非质数是质数的相乘，所以再用一个for循环，从2开始遍历到n，I * j的输都是非质数，最后返回res
123	
Best Time to Buy and Sell Stock III	34.5%	Hard	
97	
Interleaving String	28.6%	Hard	
688	Knight Probability in Chessboard	45.3%	Medium	
DP题，DP存每个点能走到的次数，先都用1填满，总共走K次，for循环K次，每次新建一个新的二维DP数组，然后二维遍历坐标，for循环8次8个方向，得到下一个位置的坐标，用if判断是否在棋盘上，是就到转移方程，tmp dp在当前点 += 前一个点的坐标上的次数。最后返回dp[r][c] / math.pow(8, k),因为dp[r][c]存的是从rc出发能到达棋盘内的次数。
221	Maximal Square	33.8%	Medium	
二维DP；思想是当1的时候把他当作正方形的最右下这个点，然后看它的左上三个位置能组成的最大正方形；dp数组比原数组大一个，两个for二位遍历，当当前char是1的时候用转移方程，看他的左，上和左斜上三个dp的最小值再加一，维护一个dp里面的最大值，最后返回这个最大值的平方。
907	
Sum of Subarray Minimums	28.8%	Medium	
1122	Relative Sort Array	66.6%	Easy	
Hashmap存arr1数字的频率，声明一个res list，遍历arr2，把arr2包括频率放进res，并且map remove 掉，把剩下的key放进一个list，排序，再放进res，最后返回一个array
450	
Delete Node in a BST	40.5%	Medium	
480	
Sliding Window Median	33.4%	Hard	
779	
K-th Symbol in Grammar	37.6%	Medium	
148	Sort List	36.7%	Medium	
并排，先用fast，slow找中点，用prev.next = null切断连接，用递归把所有节点都打散，前后两个节点进mergeSort，一个dummy用来return，一个tmp节点记录新list，while循环两个节点都不为空，小的放进新list，循环结束把没到结尾的list接上新list，最后返回dummy
409	Longest Palindrome	48.5%	Easy	
1用set，遍历s，set里有就remove，ans++，没有就放进set，res * 2，最后set如果不是空的res+1
2 用array写hashmap，记录每个字母的频率，遍历array里每个字母，ans = n / 2 * 2，ans有一次+1的机会，最后返回ans
731	
My Calendar II	45.6%	Medium	
518	Coin Change 2		43.7%	Medium	
DP buttom up; dp[0] = 1,两个for循环，外面for遍历coins；里面for遍历从coin到amount，转移公式是dp[i] += dp[i – coin],最后返回dp最后一位
90	
Subsets II	43.3%	Medium	
542	
01 Matrix	36.5%	Medium	
257	Binary Tree Paths	46.9%	Easy	
回溯，DFS遍历，没什么好说的，到叶节点，放进res
10	
Regular Expression Matching	25.6%	Hard	
72	
Edit Distance	38.9%	Hard	
92	
Reverse Linked List II	35.8%	Medium	
1104	Path In Zigzag Labelled Binary Tree	70.4%	Medium	
数学问题，先画图，用linkedlist声明res，用linkedlist的addfirst method，每层的个数是2的指数，while循环parent节点没到1，先用log找到指数d，然后找到这层的补数，这个node的parent是2^d加补数除以2，把parent存进res，进下个循环，最后返回res
54	
Spiral Matrix	31.1%	Medium	
452	
Minimum Number of Arrows to Burst Balloons	47.1%	Medium	
65	
Valid Number	14.2%	Hard	
37	
Sudoku Solver	38.3%	Hard	
583	
Delete Operation for Two Strings	45.4%	Medium	
193	
Valid Phone Numbers	25.4%	Easy	
173	
Binary Search Tree Iterator	49.9%	Medium	
175	
Combine Two Tables	53.6%	Easy	
399	
Evaluate Division
48.3%	Medium	
317	
Shortest Distance from All Buildings
38.6%	Hard	
628	Maximum Product of Three Numbers	46.4%	Easy	
遍历数组找最大的3和和最小的两个，（两个负数），返回比较这两情况里的最大值
85	
Maximal Rectangle	34.2%	Hard	
325	
Maximum Size Subarray Sum Equals k
45.1%	Medium	
609	
Find Duplicate File in System	56.1%	Medium	
104	Maximum Depth of Binary Tree	61.7%	Easy	
1 DFS遍历，1 + max（左，右）
2 BFS遍历，用for循环遍历同一层，到下一层，level++
284	
Peeking Iterator	41.5%	Medium	
468	
Validate IP Address	21.6%	Medium	
403	
Frog Jump	36.8%	Hard	
195	
Tenth Line	33.9%	Easy	
581	Shortest Unsorted Continuous Subarray	30.4%	Easy	
画图，从左往右从右往左遍历，声明一个flag，当开始unsorting了flag变true，找最小值，同样操作找最大值，然后在做两次左右遍历，小于最小数和大于最大数的就是起点和终点，返回长度
309	Best Time to Buy and Sell Stock with Cooldown	44.6%	Medium	
DP题，用两个buy和sell数组记录如果当前动作是买或者卖的最大收益，sell数组的转移方程是max不卖就是前一天的sell或者卖就是前一天的买加当前的价格，buy数组的转移方程是max不买就是前一天的buy或者买就是前两天的卖减当天的价格因为有cooldown所以是要隔一天。最后返回两个数组的最后一位的max；不过可以直接返回sell，因为最后一天买肯定会亏钱。看了别人答案dp数组可以只用两个int替代，以后再说吧
1029	Two City Scheduling	54.3%	Easy	
正好一半，贪心思想，按a城减b城的cost的差值排序，然后遍历array，前一般人去a，后移半人去b
63	
Unique Paths II	33.6%	Medium	
71	
Simplify Path	29.4%	Medium	
485	Max Consecutive Ones	55.4%	Easy	
遍历，math。Max
108	Convert Sorted Array to Binary Search Tree	52.1%	Easy	
DFS遍历，先建中间数的节点，左节点进递归用左半部的数组，右节点同理
611	
Valid Triangle Number	45.9%	Medium	
95	
Unique Binary Search Trees II	36.6%	Medium	
203	Remove Linked List Elements	36.3%	Easy	
建一个val是0的dummy，next指向head，while（head。Next ！= null）下一个点为val，连接下下个点，否则head到下一个点，结果返回dummy。Next
24	
Swap Nodes in Pairs	45.9%	Medium	
1094	
Car Pooling	57.7%	Medium	
50	Pow(x, n)	28.4%	Medium	
思想是两个同样的pow相乘，指数乘二，递归做，指数是0返回1，是偶数，half*half，是奇数half*half*x，先判断一下指数是否为负，换成倒数
404	Sum of Left Leaves	49.5%	Easy	
DFS遍历，看左节点，如果是叶节点，加进sum否则进左节点递归，再看右节点递归
223	
Rectangle Area	36.2%	Medium	
41	
First Missing Positive	29.5%	Hard	
378	
Kth Smallest Element in a Sorted Matrix	50.4%	Medium	
682	Baseball Game	61.6%	Easy	
Stack存分数，遍历string array，用switch case做选择，最后把stack加进res返回
214	
Shortest Palindrome	28.0%	Hard	
94	Binary Tree Inorder Traversal	57.9%	Medium	
Dfs inorder 遍历
189	Rotate Array	31.1%	Easy	
把array reverse一次，把0到k-1 reverse一次，再把k到最后一位reverse一次
463	Island Perimeter	61.6%	Easy	
两个for循环二维遍历，0就continue跳过，每个方块先假设周长4，判断在不在边界，四周有方块就减一，然后加进总周长里
86	
Partition List	38.1%	Medium	
106	
Construct Binary Tree from Inorder and Postorder Traversal	40.5%	Medium	
547	
Friend Circles	54.6%	Medium	
244	
Shortest Word Distance II
48.5%	Medium	
1047	Remove All Adjacent Duplicates In String	63.8%	Easy	
Stack思想，用stringBuilder存char，遍历string，如果和最后一个一样就pop掉，不一样就push，最后返回toString
151	
Reverse Words in a String	17.5%	Medium	
395	
Longest Substring with At Least K Repeating Characters	39.2%	Medium	
366	
Find Leaves of Binary Tree
66.8%	Medium	
232	Implement Queue using Stacks	44.5%	Easy	
同225，queue有front，选只改push，用n时间实现，queue的front只在empty的情况要操作，剩下的和stack一样
115	
Distinct Subsequences
35.6%	Hard	
1004	
Max Consecutive Ones III	54.3%	Medium	
81	
Search in Rotated Sorted Array II	32.7%	Medium	
120	
Triangle	40.4%	Medium	
617	Merge Two Binary Trees	70.9%	Easy	
DFS遍历，t1为空返回t2，t2为空返回t1，t3.val是t1。Val+t2.val，再进左右递归，返回t3
 46	Permutations  56.8%	Medium
回溯，从0开始推进index，index到最后就把list加进res，index和当前i的数字互换，进回溯，回溯结束再换回来
161	
One Edit Distance
31.8%	Medium	
622	
Design Circular Queue	40.4%	Medium	
141	Linked List Cycle	37.8%	Easy	
1 set记录到过的节点，碰到一样的就返回true，while结束返回false
2 双指针，因为如果没有cycle肯定会走到null node，一个走快一个走慢，while 慢!= 快，如果快走到null就返回false，while结束返回true
231	Power of Two	42.2%	Easy	
While 是偶数，n除以2，最后判断是不是1
125	Valid Palindrome	32.0%	Easy	
双指针从左右向中间遍历，跳过所有非alphanumeric，如果左右不同返回false，最后返回true
122	Best Time to Buy and Sell Stock II	52.8%	Easy	
从1开始遍历，能赚钱就加进profit
270	Closest Binary Search Tree Value 44.4%	Easy	
遍历bst，维护一个closest val，它和target的绝对值更小，小进左树大进右树，最后返回closest
209	
Minimum Size Subarray Sum	35.4%	Medium	
110	Balanced Binary Tree	41.5%	Easy	
DFS遍历递归，当左右高度差大于1就返回-1，当出现-1就返回-1，最后判断返回的是不是-1
183	Customers Who Never Order	46.3%	Easy	
Left join 再用where order = null找人
1135	
Connecting Cities With Minimum Cost
51.0%	Medium	
241	
Different Ways to Add Parentheses	51.1%	Medium	
128	
Longest Consecutive Sequence	42.4%	Hard	
243	Shortest Word Distance 58.1%	Easy	
遍历array，如果word1word2出现，记录位置，位置有效就算距离，维护最小的距离，最后返回min
350	
Intersection of Two Arrays II	48.7%	Easy	
77	
Combinations	49.2%	Medium	
647	Palindromic Substrings	57.7%	Medium	
从中心展开的暴力解；遍历string，以当前char和+1为中心向左右展开判断左右是否相同；O(n^2)反正和DP的时间复杂度一样写个简单的
771	
Jewels and Stones	83.5%	Easy	
160	
Intersection of Two Linked Lists	35.1%	Easy	
707	
Design Linked List	21.1%	Easy	
285	
Inorder Successor in BST
35.7%	Medium	
938	
Range Sum of BST	78.1%	Easy	
841	Keys and Rooms	61.0%	Medium	
回溯,DFS遍历,进过的房间放进set,进DFS后先拿所有钥匙,在for循环遍历钥匙,如果当前钥匙没进过就进DFS,DFS结束最后返回visited是否等于rooms的大小
743	
Network Delay Time	43.3%	Medium	
112	
Path Sum	38.4%	Easy	
687	Longest Univalue Path	34.3%	Easy	
绝对不是easyl； globalvariable res=0, dfs遍历，输入node和parentnode的val，左右树遍历，返回长度，res取left+right最大值，当当前node。Val==parent返回左右的max再+1，否则返回0
279	
Perfect Squares
42.8%	Medium	
74	
Search a 2D Matrix	35.1%	Medium	
561	
Array Partition I	69.7%	Easy	
113	
Path Sum II	41.8%	Medium	
315	
Count of Smaller Numbers After Self	38.9%	Hard	
877	
Stone Game	62.0%	Medium	
406	Queue Reconstruction by Height	60.6%	Medium	
重写compare对people数组排序，身高从大到小，如果一样第二位从小到大；创建一个list存结果，遍历排序好的数组，用list的add(#,#)method，把当前的一维数组放进他的第二位做index的位置，因为如果是小的数并不会影响到他的第二位前面有几个大的数，最后把list转换成二维数组return
166	
Fraction to Recurring Decimal	19.8%	Medium	
69	
Sqrt(x)	31.9%	Easy	
114	Flatten Binary Tree to Linked List	43.6%	Medium	
先画图弄清楚操作步骤；从root出发，先看有没有左节点，如果有则把左节点练到原右节点，把原右节点连到原左节点的最后一个右节点后面；然后向右迭代
73	
Set Matrix Zeroes	40.6%	Medium	
242	
Valid Anagram	53.2%	Easy	
304	
Range Sum Query 2D - Immutable	33.5%	Medium	
264	
Ugly Number II	37.1%	Medium	
145	
Binary Tree Postorder Traversal	49.7%	Hard	
1038	
Binary Search Tree to Greater Sum Tree	78.5%	Medium	
329	
Longest Increasing Path in a Matrix	40.7%	Hard	
198	House Robber	41.2%	Easy	
DP，用dp存当前节点能拿的最大值，注意nums的index比dp的index要多一位，最后返回DP数组的最后一位
451	
Sort Characters By Frequency	56.9%	Medium	
807	
Max Increase to Keep City Skyline	81.9%	Medium	
334	
Increasing Triplet Subsequence	39.5%	Medium	
429	
N-ary Tree Level Order Traversal	60.3%	Easy	
179	
Largest Number	26.3%	Medium	
337	House Robber III	48.7%	Medium	
DP+DFS；DP数组0是不加当前节点，1是加当前节点；从root开始递归；递归结束就是走到null，返回两个0；递归进左右树；当前不加那就加左右里的加或不加里大的；当前加那就不加左右；最后返回也是比较root加或不加
60	
Permutation Sequence	33.8%	Medium	
811	
Subdomain Visit Count	66.3%	Easy	
912	
Sort an Array	63.1%	Medium	
229	
Majority Element II	32.8%	Medium	
66	
Plus One	41.6%	Easy	
654	
Maximum Binary Tree	76.8%	Medium	
67	
Add Binary	40.1%	Easy	
299	
Bulls and Cows	40.2%	Easy	
118	
Pascal's Triangle	47.4%	Easy	
131	
Palindrome Partitioning	42.2%	Medium	
109	Convert Sorted List to Binary Search Tree	42.0%	Medium	
递归，传入开始点和结束点，用while，fast，slow找中间node，中间node作为root，call递归方程，左节点传第一个点和中间node，右节点传中间下一个和最后节点
509	
Fibonacci Number	66.7%	Easy	
129	
Sum Root to Leaf Numbers	43.4%	Medium	
437	
Path Sum III	43.5%	Easy	
44	
Wildcard Matching	23.2%	Hard	
226	
Invert Binary Tree	59.2%	Easy	
621	
Task Scheduler	46.1%	Medium	
290	
Word Pattern	35.4%	Easy	
559	
Maximum Depth of N-ary Tree	66.0%	Easy	
977	
Squares of a Sorted Array	71.8%	Easy	
190	
Reverse Bits	32.5%	Easy	
181	
Employees Earning More Than Their Managers	49.9%	Easy	
100	Same Tree	50.5%	Easy	
递归，四种情况，都为null，一个为null，值不同，和值相同则进递归
84	
Largest Rectangle in Histogram	32.0%	Hard	
222	
Count Complete Tree Nodes	35.8%	Medium	
328	
Odd Even Linked List	50.1%	Medium	
1114	
Print in Order	58.5%	Easy	
61	
Rotate List	27.8%	Medium	
739	Daily Temperatures	60.4%	Medium	
用递减stack存index，for循环遍历T数组，用一个while循环做判断，把当前温度和stack的第一个的温度比较，看是不是更热，如果是的话把stack第一个pop出来，这个index就可以算出距离，放进res数组里，while判断结束把当前i放进stack，因为int数组默认是0，所以不用再赋值0了，最后返回res
217	
Contains Duplicate	52.9%	Easy	
35	
Search Insert Position	41.1%	Easy	
1155	
Number of Dice Rolls With Target Sum	49.8%	Medium	
18	
4Sum	31.3%	Medium	
142	Linked List Cycle II	33.1%	Medium	
141的followup这次是return环开始的节点；还是快慢双指针，相遇的时候break，然后在其中一个初始到head，这次两个都只走一步，相遇，return节点；因为快指针走的距离是head到环起点加起点到相遇的距离，两个同步走就相当于一起减掉起点到相遇的距离
47	
Permutations II	41.7%	Medium	
905	
Sort Array By Parity	72.7%	Easy	
235	
Lowest Common Ancestor of a Binary Search Tree	45.8%	Easy	
29	
Divide Two Integers	16.2%	Medium	
111	
Minimum Depth of Binary Tree	35.7%	Easy	
237	
Delete Node in a Linked List	55.0%	Easy	
26	
Remove Duplicates from Sorted Array	41.6%	Easy	

402. Remove K Digits
把数字存进stack， 当当前数字小于前一个数，把前一个pop掉，最后用stack建string，edge case找不到小的数，1所有数字一样，2所有数字升序排列，只用把stack pop掉K个就行， 如果string头上有0，就把0都去掉
397. Integer Replacement		Medium
本质上目的是多做/2的操作,4的倍数是最好情况，能连做两次/2，N % 4 的四种情况，0是最优；1就-1；2直接/2，下一步未知；3就+1变成4；最后到3是特殊情况，3-2-1
345. Reverse Vowels of a String
写个method判断vowel，一个method用来swap，双指针左右遍历，都是vowel就swap，最后返回string
1005. Maximize Sum Of Array After K Negations EASY
先排序，遍历数组，K大于0且当前数是负数就取反，计算sum,遍历结束如果K大于0且是奇数就sum减两倍最小数
958. Check Completeness of a Binary Tree	Medium
1.BFS遍历，声明一个boolean存是否走到最后一个节点，whilequeue循环遍历，如果curr节点是null就循环走完，flag变true，else当前节点不为空里面，flag为true直接返回false，queue加左右节点，最后返回true
2.BFS遍历，前面都一样，while里先看左节点，不为空如果flag是true直接返回false，否则放进左节点，然后看右节点一样的操作，while结束返回true
1133. Largest Unique Number
1.遍历array,放进hashtable,value存频率,再遍历keyset,只看频率为一的最后返回最大值
2.因为取值范围是0到1000,建一个大小是1001的hashtable就行,遍历array存频率,table从大到小遍历,如果table[i]为1直接return i
1167. Minimum Cost to Connect Sticks	Medium
pq，拿出前两个相加，放回去，while到size是1，返回sum
494. Target Sum		Medium
https://blog.csdn.net/mine_song/article/details/70216562
DP；等式推导，positive的和减negative的和等于target，推出positive的和等于target + nums的和除以二；问题就变成只要知道positive的和有几种可能就行；然后是动态规划，dp数组表示加起来的和是这个数有多少种可能，先遍历nums数组，然后从大到小for循环；具体步骤就像，当前是1，目标9，9就是加等8的个数，目标8，8就是加等7的个数，依此类推；最后返回dp目标的个数
416. Partition Equal Subset Sum		Medium
DP;能被分成两部分那么所有数的和的一半一定能被数组里的数组成；所以先算和，和一定要是偶数，dp的boolean数组表示这个数能不能被加到，dp0是true；遍历数组，然后从大到小for循环，转移方程是dp中这个数减当前遍历的数ordp这个数；最后返回dp目标数字
836. Rectangle Overlap		Easy
画图，从1D开始，记住负负得正所以不用管哪个在左，推导出两个关系式；然后把套在x和y上


Amazon BQ
Practice using the STAR Method on these common behavioral interviewing questions: 
• Describe a situation in which you were able to use persuasion to successfully convince someone to see things your way.
• Describe a time when you were faced with a stressful situation that demonstrated your coping skills. 
• Give me a specific example of a time when you used good judgment and logic in solving a problem. 
• Give me an example of a time when you set a goal and were able to meet or achieve it. 
• Tell me about a time when you had to use your presentation skills to influence someone's opinion. 
• Give me a specific example of a time when you had to conform to a policy with which you did not agree. 
• Please discuss an important written document you were required to complete.
• Tell me about a time when you had to go above and beyond the call of duty in order to get a job done. 
• Tell me about a time when you had too many things to do and you were required to prioritize your tasks. 
• Give me an example of a time when you had to make a split second decision. 
• What is your typical way of dealing with conflict? Give me an example. 
• Tell me about a time you were able to successfully deal with another person even when that individual may not have personally liked you (or vice versa). 
• Tell me about a difficult decision you've made in the last year. 
• Give me an example of a time when something you tried to accomplish and failed. 
• Give me an example of when you showed initiative and took the lead. 
• Tell me about a recent situation in which you had to deal with a very upset customer or coworker. 
• Give me an example of a time when you motivated others. 
• Tell me about a time when you delegated a project effectively. 
• Give me an example of a time when you used your fact-finding skills to solve a problem. 
• Tell me about a time when you missed an obvious solution to a problem. 
• Describe a time when you anticipated potential problems and developed preventive measures. 
• Tell me about a time when you were forced to make an unpopular decision. 
• Please tell me about a time you had to fire a friend. 
• Describe a time when you set your sights too high (or too low).
