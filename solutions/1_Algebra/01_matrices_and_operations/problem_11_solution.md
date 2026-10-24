Given:
A = [1 1; 0 1]
B = [a b; c d]

Computing AB and BA:
AB = [1 1; 0 1] * [a b; c d] = [a + c   b + d; c   d]
BA = [a b; c d] * [1 1; 0 1] = [a   a + b; c   c + d]

Finding Conditions for AB = BA:
Equating the corresponding entries of AB and BA:

Top-left: a + c = a => c = 0

Top-right: b + d = a + b => d = a

Bottom-left: c = c (satisfied)

Bottom-right: d = c + d => c = 0 (consistent)

Thus, the required conditions are c = 0 and d = a (while a and b can be any real numbers).

General Form of Matrix B:
Substituting these conditions into B, the general form of all matrices that commute with A is:
B = [a b; 0 a]
