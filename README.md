def bfs(graph, root):
    visited = set()
    queue = []
    visited.add(root)
    queue.append(root)

    while queue:
        vertex = queue.pop(0)
        print(str(vertex) + " ", end="")

        for neighbour in graph[vertex]:
            if neighbour not in visited:
                visited.add(neighbour)
                queue.append(neighbour)



graph = {'1': ['2', '3'], '2': ['4', '5'], '3': ['6', '7'], '4': ['8', '9'], '5': ['10', '11']}
print("Following is Breadth First Traversal: ")
bfs(graph, '1')
