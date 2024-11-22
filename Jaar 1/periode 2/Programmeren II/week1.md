#  mult_of_five
```
    def mult_of_five(n):
        """Return a list containing the first n multiples of 5
        """
        return [i * 5 for i in range(1, n + 1)]
        
        
    assert mult_of_five(0) == []
    assert mult_of_five(1) == [5]
    assert mult_of_five(2) == [5, 10]
    assert mult_of_five(3) == [5, 10, 15] 
```


#  divisible_by
```
    def divisible_by(n, L):
        """Return a list with values in L divisible by n
        """
        return [i for i in L if i % n == 0]

    assert divisible_by(5, [15, 0, 23, 4]) == [15, 0]
    assert divisible_by(3, [2, 4, 8, 10]) == []
    assert divisible_by(2, []) == []
```

#  starts_with
```
    def starts_with(s, L):
        """Return all strings in L which start with s
        """
        return [i for i in L if s == i[:len(s)]]

    assert starts_with("a", []) == []
    assert starts_with("a", ["bbc", "brits", "omroep"]) == []
    assert starts_with("a", ["abc", "cde", "aha", "abba"]) == ["abc", "aha", "abba"]
    assert starts_with("ab", ["abc", "cde", "aha", "abba"]) == ["abc", "abba"]
    assert starts_with("abc", ["abc", "cde", "aha", "abba"]) == ["abc"]
    assert starts_with("abcd", ["abc", "cde", "aha", "abba"]) == []
```

#  double_letters
```
    def double_letters(L):
        """Double all letters in L
        """
        return [i * 2 for i in L]


    assert double_letters(["a"]) == ["aa"]
    assert double_letters(["a", "1", "23"]) == ["aa", "11", "2323"]
```


#  num_as
```
    def num_as(L):
    """Count the number of a's in L
    """
    return sum(1 for i in L if i == "a")

    assert num_as(["a", "b", "c", "a", "d"]) == 2
    assert num_as(["y", "b", "c", "x", "d"]) == 0
```


#  vwl
```
    def vwl(s):
        '''Return the number of vowels in a string'''
        return sum(1 for char in s if char in "aeiou")

    assert vwl("appel") == 2
    assert vwl("bbc") == 0
    assert vwl("oma") == 2
```


#  add_tax
```
    def add_tax(t, L):
        """Increment each item in L with t percent tax"""
        return [round(price * (1 + t / 100), 2) for price in L]

    assert add_tax(7, [10, 100, 30, 40]) == [10.7, 107.0, 32.1, 42.8]
    assert add_tax(7, [0, 16, 8]) == [0.0, 17.12, 8.56]
```

#  above_below_freeze
```
    def check_freeze(temp):
        """Return 'onder', 'boven' or 'gelijk' based on the temperature."""
        if temp < 0:
            return "onder"
        elif temp > 0:
            return "boven"
        else:
            return "gelijk"

    def above_below_freeze(L):
        """Return whether each item in L is below, above or equal to freezing temperature as a string representation."""
        return [check_freeze(temp) for temp in L]

    assert above_below_freeze([-1, 0, 10]) == ["onder", "gelijk", "boven"]
    assert above_below_freeze([21, -21, 0]) == ["boven", "onder", "gelijk"]
```

#  zipper
```
    def zipper(L1, L2):
        """Pairwise combine lists L1 and L2
        """
        return [[l1, l2] for l1, l2 in zip(L1, L2)]
        
    assert zipper([1, 3, 5], [2, 4, 6]) == [[1, 2], [3, 4], [5, 6]]
    assert zipper([10, 9, 12], ["jan", "feb", "mar"]) == [[10, "jan"], [9, "feb"], [12, "mar"]]
```

#  only_evens
```
    def is_even(x):
        """Return True if x is even, False otherwise
        """
        return x % 2 == 0

    def only_evens(L):
        """Returns a list containing the even numbers in L
        """
        return [x for x in L if is_even(x)]

    assert only_evens([1, 1, 1]) == []
    assert only_evens([2, 2, 2]) == [2, 2, 2]
    assert only_evens([0, 1, 2, 3]) == [0, 2]
```
