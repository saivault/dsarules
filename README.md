<h1>Rules for DSA</h1>
<ul>
<li>Only think the solution is done when the base cases are handled. </li>
<li>The size of a data structure can be of any amount, try to reduce the number of traversals. </li>
<li>Though traversal means visiting each element, it doesn't always imply moving from start to end in case of linear data strcutures. It may also be from end to the start to solve the task efficiently and more logically.</li>

<li>At times, think from the perspective of STL</li>
<li>While performing a remainder operator <code>n % d</code>, make sure that n is not negative, otherwise do <code>(n + CONSTANT*d) % d</code> </li>
</ul>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>


<h1>Special Cases</h1>
<h2>1. Use of long long is underrated.</h2>

```cpp
    int x = 1000000;
    int y = 1000000;
  
    // This causes overflow even if z is long long int
    long long int z = x*y;
    cout << z;
```
<blockquote>-727379968</blockquote>

<br><br><br>
You might get some other negative value as output. So what is the problem here? The ints are not promoted to long long before multiplication, they remain ints and their product as well. Then the product is cast to long long, but we are late now as overflow has already occurred. Having one of x or y as long long should would work, as the other would be promoted. We can also use 1LL (or 1ll). LL is the suffix for long long, which is 64-bit on most C/C++ implementations. So 1LL, is a 1 of type long long.
<br><br><br>

```cpp
    int x = 1000000;
    int y = 1000000;
  
    long long int z = 1LL*x*y;
    cout << z;
```
<blockquote>1000000000000</blockquote>
