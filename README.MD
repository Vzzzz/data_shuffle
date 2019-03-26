Data shuffle for cross-validation

We take two parameters: data that we need to shuffle and number of pieces that it need to be divided.
Accordind to Task requirements we should contain all the data in returned result without any duplication in "training" parts. Here is an algorithm:
1) We need to know what the lengths of our "training sets" are. It is always length of data divided by number of pieces or the same number plus one
2) According to previously mentioned "plus one" we need to know should we add to current set this "plus one" element
3) "Plus one" element(s) create the shift of indexes that we have to evaluate every step respectivly to p.2. That's why variable f exists. It checks "plus one(s)"
