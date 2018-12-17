def results(graph, costs, parents, processed):
    node = find_lowest_cost_node(costs, processed)
     while node is not None:
         cost = costs[node]
         neighbors = graph[node]
         for n in neighbors.keys():
             new_cost = cost + neighbors[n]
             if costs[n] > new_cost:
                costs[n] = new_cost
                 parents[n] = node
         processed.append(node)
         node = find_lowest_cost_node(costs, processed)
 # 存储邻居到散列表
 def create_data_1():
    graph = {}
     graph["乐谱"] = {}
     graph["乐谱"]["海报"] = 5
     graph["乐谱"]["黑胶唱片"] = 0
     graph["海报"] = {}
     graph["海报"]["吉他"] = 30
     graph["海报"]["架子鼓"] = 35
     graph["黑胶唱片"] = {}
     graph["黑胶唱片"]["吉他"] = 15
     graph["黑胶唱片"]["架子鼓"] = 20
     graph["吉他"] = {}
     graph["吉他"]["钢琴"] = 20
     graph["架子鼓"] = {}
     graph["架子鼓"]["钢琴"] = 10
     graph["钢琴"] = {}
     return graph
 # 开销表
 def create_data2():
    costs = {}
     costs["海报"] = 5
     costs["黑胶唱片"] = 0
     costs["吉他"] = 10000
     costs["架子鼓"] = 10000
     costs["钢琴"] = 10000
    return costs
 # 存储父节点的散列表
 def create_data3():
    parents = {}
     parents["海报"] = "乐谱"
     parents["黑胶唱片"] = "乐谱"
     parents["吉他"] = None
     parents["架子鼓"] = None
     parents["钢琴"] = None
     return parents
 # 找出最低开销的节点
 def find_lowest_cost_node(costs, processed):
    lowest_cost = 10000
     lowest_cost_node = None
     for node in costs:
         cost = costs[node]
         if cost < lowest_cost and node not in processed:
            lowest_cost = cost
             lowest_cost_node = node
     return lowest_cost_node
