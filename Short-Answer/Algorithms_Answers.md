Add your answers to the Algorithms exercises here.

Exercise I

a) Runtime: O(n) - linear time. As the the input n increases, the number of looping operations done in the while loop increases in linear proportion. For example, n=2 will do 1 loop, n=3 will do 2 loops, n=4 will do 3 loops, etc.

b) Runtime: O(n^4) - quadratic time. As the input n increases, the runtime increases n^4. This is because of the 3 nested loops, each of which is running a linear operation.
The first for loop causes it to run in n time. The first nested for loop results in n^2 time. The second nested loops results in n^3 time. The third nested loop results in n^4 time

c) Runtime: O(n^2) - quadratic time. The recursive call will result in a quadratic run time.



Exercise II


This would essentially be a searching algorithm in which you are searching through a list. The list could be booleans representing floors in which the egg would not break (False) and the egg would break (True). This list would already be sorted, since the lowest stories of the building would not cause the egg to break, and every floor after the first True floor would also cause the egg to break. So the list may look look like floors = [False, True, True, True, True, True, True...].

Since the list of floors is already sorted, we could use a Binary Search algorithm, searching for a True that appears in the smallest index value of the list. In my example of list floors above, the target would be the True value in index 2.

def egg_drop(n):
  low = 0
  high = # of stories the building has

  while low is less than or equal to high:
    middle = the middle of the list of floors

    if middle is False (egg doesn't break):
      The target floor is to the right of the list, so ignore everything to the left of the list by setting low = middle + 1

    if middle is True (egg breaks):
      The target floor is either the current middle value or is to the left of the list, so ignore everything to the right of the list by setting high = middle (don't subtract 1 here because we don't know if this is the first instance of True in the list, so don't discard it)

  return middle


Runtime: O(log(n)) - logarithmic time.