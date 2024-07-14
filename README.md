![python](https://logos-world.net/wp-content/uploads/2021/10/Python-Logo.png)

# Length of Last Word

## Description

Given a string `s` consisting of words and spaces, return the length of the last word in the string.

A word is a maximal substring consisting of non-space characters only.

## Constraints

- `1 <= s.length <= 10^4`
- `s` consists of only English letters and spaces ' '.
- There will be at least one word in `s`.

## Approach

To solve this problem, we can use the following approach:

- Split the string `s` by spaces to get a list of words.
- Filter out any empty strings from the list.
- Return the length of the last word in the filtered list.

## Complexity

### Time Complexity

- `s.split()`: This operation splits the string `s` into a list of words, which is O(n) where n is the length of the string `s`.
- `filter(lambda x: x != '', words)`: Filtering out empty strings takes O(m) time, where m is the number of words in `s`.
- Accessing the last element and calculating its length takes O(1) time.

Therefore, the overall time complexity is O(n), where n is the length of the string `s`.

### Space Complexity

- `words = s.split()`: Requires O(n) space to store the list of words.
- `filtered_words`: Additional space depends on the number of non-empty words in `s`.

Thus, the space complexity is O(n) due to storing the list of words `words`.

## Code

```python
class Solution:
    def lengthOfLastWord(self, s: str) -> int:
        words = s.split()
        filtered_words = list(filter(lambda x: x != "", words))
        return len(filtered_words[-1])
```

## Installation

To run the code, ensure you have Python installed on your system. Save the code in a `.py` file and execute it using a Python interpreter.

## Usage

To use the function, create an instance of the `Solution` class and call the `maxProfit` method with your list of prices.

## Example

```python
s = "Hello World"
solution = Solution()
print(solution.lengthOfLastWord(s))  # Output: 5
```
## Contributing
If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

## Acknowledgements
Thanks to the open-source community for providing helpful resources and inspiration. Special thanks to [LeetCode](https://leetcode.com) for the platform and resources.

# LeetCode Submission
You can view my LeetCode submission for this problem [here](https://leetcode.com/problems/length-of-last-word/solutions/5476074/python-length-of-the-last-word-in-list)
.
