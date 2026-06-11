DFS(g)
	for each vertex v $\in$ GV
		v.color = white
		v.$\pi$ = null
	time = 0
	for each vertex v $\in$ GV
		if v.color == white
			dfs_visit(g, v)

DFS_VISIT(g, v)
	time = time + 1
	v.d = time
	v.color=grey
	for each v.g.adj[v]
		if v.color == white
			v.$\pi$
			dfs_visit(g, v)
		v.color = black
		time = time+1
		v.f = time