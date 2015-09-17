# Higher order functions

Firstly, read chapter 1.6 of [Composing Programs](http://composingprograms.com/pages/16-higher-order-functions.html).

Recall that functions serve the purpose of abstracting away larger, more complex operations.  For example,

    def sum_squares_of_even_elements(array):
        """
        Returns the sum of elements in array with an even index, squared.
        """
        return sum([array[i]**2 for i in range(len(array)) if i % 2 == 0])

is a more clear and concise than writing out the function innards that generates such output every time.  This is convenient because our code can minimize writing blocks of the exact same code over and over again.

However, what about if our program requires us to have blocks of *similar* code, but not *exactly the same*?  Consider the following example of printing all elements in an array:

    def print_all_array_elements(array):
        for element, index in enumerate(array):
            print('Element ' + element + ' is at index ' + str(index))

But, what if we want to do something else besides printing out the elements?  Notice that in the for loop above, inside the for loop, we're performing an action to the element: printing it.  We can break this down as follows:

    def print_all_array_elements(array):
        for element, index in enumerate(array):
            describe(element, index)

    def describe(element, index):
        print('Element ' + element + ' is at index ' + str(index))

Notice that the `print_all_array_elements` function is more or less a for loop wrapping around `describe`, now.  Let's modularize this even more.

    def for_each(array, fn):
        for element, index in enumerate(array):
            fn(element, index)

    def print_all_array_elements(array):
        for_each(array, describe)

Notice that we've treated `describe` as an object, and passed it into our `for_each` function.  `for_each` can then make calls to this argument.  This is what a *higher-order function* is: a function which operates on other functions, either by taking them as arguments, or by returning them.

Some common higher-order functions in all programming languages are `map`, `reduce`, and `filter`.  Some information about these can be found [here](http://www.bogotobogo.com/python/python_fncs_map_filter_reduce.php).

To conclude, higher-order functions are powerful tools because they can abstract *actions* away, not just values.  This is very useful for making modular code that is reusable and easy to maintain.
