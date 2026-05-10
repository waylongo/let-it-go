# Why code comments rot

A letter, once sealed, can sit in a drawer for fifty years and still say exactly what it said on the day it was written. The words don't move. The paper yellows, the handwriting gets harder to read, but the sentences are sovereign — they do not depend on anything outside themselves to remain true.

A code comment is the opposite kind of thing. A code comment is a claim about its surroundings. It says: *this function returns null on failure*, or *cache is invalidated when the user logs out*, or *this loop runs at most three times.* And every one of those claims is hostage to code that someone will change next Thursday without thinking about the comment at the top of it.

The code gets fixed. The comment does not get fixed. It sits there, still making its old claim, while the thing it claims about has quietly become something else. Now it is worse than no comment. A missing comment leaves you uncertain; a wrong comment makes you confident about the wrong thing. Confidence is much more expensive than uncertainty.

Junior engineers are told to write more comments. Senior engineers are told to write fewer. The reason is the same in both cases: comments are liabilities that pretend to be assets. When you write one you are taking on a maintenance burden that the compiler will never remind you about and the tests will never fail on.

The only kind of comment that doesn't rot is the kind that refuses to make a claim about the code. *This is a workaround for a known kernel bug, ticket #4411.* *The formula comes from the 1964 paper, equation 3.2.* *Do not reorder these three lines.* These are fine, because the code can change around them and the statement stays true. They are letters, sealed and dated. They will still be themselves on the day someone finds them.

The others are just confident ghosts, making promises on behalf of a version of the code that died years ago.
