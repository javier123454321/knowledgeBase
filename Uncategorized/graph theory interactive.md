- https://d3gt.com/
    - Definitions
    - Order of a graph is the number of vertices, Size the number of edges
        - $$\frac{n(n-1)}{2}$$ 
            - Each vertex can connect to n-1 vertex, but because the connections of an [undirected graph](((MGxjRmXPv))) are bidirectional, they are divided by 2
        - {{[[drawing]]}}
        - 
    - Degree is a measure of edges attached to a vertex: $$deg$$
        - Minimum degree of a graph is small delta: $$\delta(G)$$ and maximum is big delta: $$\Delta(G)$$
        - $$deg$$ is a property of a **vertex**
        - $$\delta$$ and $$\Delta$$ are properties of **graphs**
    - The degree sequence of a graph is the list of the degrees in **descending order**
        - ex:
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FJavier-knowledge-graph%2F26Rzq7CnEG.png?alt=media&token=fe357c33-cbc7-4354-bf15-6c8b926b86c7)
                - $$\text{degree sequence}=(1,1)$$
                - $$\sum = 2$$
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FJavier-knowledge-graph%2FzUWovDjthO.png?alt=media&token=fb7c1144-d3b3-4aa7-8cc0-a3540e81745d)
                - $$\text{degree sequence}=(1,1,0)$$
                - $$\sum = 2$$
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FJavier-knowledge-graph%2FFn5rwqEOve.png?alt=media&token=1bd4c4df-cb38-4070-8a97-818020f11404)
                - $$\text{degree sequence}=(2,1,1)$$
                - $$\sum = 4$$
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FJavier-knowledge-graph%2FMbgnY9JddI.png?alt=media&token=c33e2fed-7b42-44ca-8ecb-dd4f3b139e80)
                - $$\text{degree sequence}=(5, 4,3, 2,2,2 )$$
                - $$\sum = 18$$
        - $$\sum deg(v_i)=2|E|$$ 
where $$|E| = \text{number of edges}$$ (size of graph) 
    - A graphic sequence is a sequence of numbers that can be used to draw a graph