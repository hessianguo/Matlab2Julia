# Matlab2Julia
List the equivalent Matlab commands  in Julia if there are different.


## Most common commands
| Matlab Command | Julia Comand | Description | 
| --- | --- | --- |
| `eye(n)`| `Matrix{Float64}(I, n,n)` | Identity matrix  |
| `max(A, 1)` | `maximum(A, dims=1)` | Find the maximum element of an array|
|`[m, idx] = max(a)` | `m,idx = findmax(a)` | Find the maximum element and index of an vector a|
| `[~, idx] = max(a)` | `idx = argmax(a)` | Find the index of maximum element |
| `min(A, 1)` | `minimum(A, dims=1)` | Find the minimum element of an array|
|`[m, idx] = min(a)` | `m,idx = findmin(a)` | Find the minimum element and index of an vector a|
| `[~, idx] = min(a)` | `idx = argmin(a)` | Find the index of minimum element |
| `squeeze(A)`|`dropdims(A, dims=3)` |Remove the dimensions specified by dims from array A |
|`diag(a, k)` |  `diagm(k => a)` | create a diagonal matrix from a with k|
|`diag(a)` |  `Diagonal(a)` | create a diagonal matrix from a; using LinearAlgebra|
|`flipup(A)`|`reverse(A, dims=1)`| Flip in the up-down direction |
|`fliplr(A)`|`reverse(A, dims=2)`| Flip in the left-right direction |
|`flip(A, k)`|`reverse(A, dims=k)`| Flip in the k-dimensional|
|`semilogx(x,y)`|`plot(x,y,xaxis=:log)`|Plot in log scale in x coordinate; using Plots|
|`semilogy(x,y)`|`plot(x,y,yaxis=:log)`|Plot in log scale in y coordinate; using Plots|
|`loglog(x,y)`|`plot(x,y,xaxis=:log, yaxis=:log)`|Plot in log scale in x and y coordinate; using Plots|
|`plot(x,y,'r')`|`plot(x,y,color=:red)`|Set red color in the plot; using Plots|
|`plot(x,y,':')`|`plot(x,y,linestyle=:dot)`|Use dot line in the plot; using Plots|
|`plot(x,y);hold on; plot(x,z)`|`plot(x,y);plot!(x,z)`| Plot in the same figur; using Plots|
|`subplot(121); plot(x,y); subplot(122);plot(x,z)`|`plot(plot(x,y),plot(x,z),layout=(1,2))`|Subplot, ; using Plots|
|`p=polyfit(x,y,k)`|`p=fit(x,y,k)`|Fit a polynomial of degree k; using Polynomials|
|`polyval(p,xx)`|`p.(xx)`|Evaluate the fitted polynomial at xx; using Polynomials|
|`a(end+1)=1`|`append!(a,1)`|Add 1 to the end of the vector a|
|`a+bi`|`a+bim`|Create a complex number|
|`1:2:5`|`collect(1:2:5)`|Create 1d array [1; 3; 5 ]|
|`x(x>3)`|`filter(z->z>3, x)`| Remove element less than 3|
|`randi(10,3,1)`|`rand(1:10, 3,1)`| Generate an array of random integer between 1 and 10|
|`a(1,3)`|`a[1,3]`|Access element of an array a|
