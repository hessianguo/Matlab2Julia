# Matlab2Julia
List the equivalent Matlab commands  in Julia if there are different.


## Most common commands
| Matlab Command | Julia Comand | Description | 
| --- | --- | --- |
| `eye(n)`| `Matrix{Float64}(I, n,n)` | Identity matrix  |
| `max(A, 1)` | `maximum(A, dims=1)` | Find the maximum element of an array|
|`[m, idx] = max(a)` | `m,idx = find(a)` | Find the maximum element and idea of an vector a|

