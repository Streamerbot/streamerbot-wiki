---
title: Inline Math Function
description: 
published: true
date: 2022-02-26T19:58:35.678Z
tags: 
editor: markdown
dateCreated: 2021-11-17T21:12:11.893Z
---

# Math

Levaraging the [mXparser](https://github.com/mariuszgromada/MathParser.org-mXparser) library, you can now evaluate mathematical equations directly inline with variable replacements.

# Supported Tokens

For easier reference, these are all the supported tokens, this is current for the version of mXparser that is used, these can also be seen on the [mXparser](https://github.com/mariuszgromada/MathParser.org-mXparser) GitHub, version 4.4.2 is the version in use.

## Number format
|Keyword|Category|Description|Example|
|---|---|---|---|---|
|Number|Decimal Number|Decimal number|1, 1.5, -
|Number|Decimal Number|Decimal number - scientific notation|1.2e10, -2.4e-10, 2.3E+10|
|Number|Binary Number|Binary number - number literal| b.10101, B.10101, b2.10010|
|Number|Octal Number|Octal number - number literal| o.1027, O.1027, b8.1027|
|Number|Hexadecimal Number|Hexadecimal number - number literal| h.12fE, H.12fE, b16.12fE|
|Number|Unary Number|Unary number - number literal| b1.111 , B1.111|
|Number|Base 1-36|Base 1-36 number - number literal| bN.xxxx , BN.xxxx|
|Number|Fraction|Number literal as fraction| 1_2 , 2_3_4, 172_345, 345_172 |

## Operators
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| `+` | Operator | Addition | a + b |
| `-` | Operator | Subtraction | a - b |
| `*` | Operator | Multiplication | a * b |
| `/` | Operator | Division | a / b |
| `^` | Operator | Exponentiation | a^b |
| `!` | Operator | Factorial | n! |
| `#` | Operator | Modulo function | a # b |
| `%` | Operator | Percentage | n% |
| `^^` | Operator | Tetration | a^^b |

## Boolean Operators
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| & |Boolean Operator|Logical conjunction (AND)|p & q|
| && |Boolean Operator|Logical conjunction (AND)|p && q|
| /\\ |Boolean Operator|Logical conjunction (AND)|p /\\ q|
| ~& |Boolean Operator|NAND - Sheffer stroke|p ~& q|
| ~&& |Boolean Operator|NAND - Sheffer stroke|p ~&& q|
| ~/\\ |Boolean Operator|NAND - Sheffer stroke|p ~/\\ q|
| \| |Boolean Operator|Logical disjunction (OR)|p \| q|
| \|\| |Boolean Operator|Logical disjunction (OR)|p \|\| q|
| \\/ |Boolean Operator|Logical disjunction (OR)|p \\/ q|
| ~\| |Boolean Operator|Logical NOR|p ~\| q|
| ~\|\| |Boolean Operator|Logical NOR|p ~\|\| q|
| ~\\/ |Boolean Operator|Logical NOR|p ~\\/ q|
| (+) |Boolean Operator|Exclusive or (XOR)|p (+) q|
| --> |Boolean Operator|Implication (IMP)|p --> q|
| <-- |Boolean Operator|Converse implication (CIMP)|p <-- q|
| -/> |Boolean Operator|Material nonimplication (NIMP)|p -/> q|
| </- |Boolean Operator|Converse nonimplication (CNIMP)|p </- q|
| <-> |Boolean Operator|Logical biconditional (EQV)|p <-> q|
| ~ |Boolean Operator|Negation|~p|

## Bitwise Operators
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| @~ |Bitwise Operator|Bitwise unary complement|@~10|
| @& |Bitwise Operator|Bitwise AND|10 @& 2|
| @^ |Bitwise Operator|Bitwise exclusive OR|10 @^ 2|
| @\| |Bitwise Operator|Bitwise inclusive OR|10 @\| 2|
| @<< |Bitwise Operator|Signed left shift|10 @<< 2|
| @>> |Bitwise Operator|Signed right shift|10 @>> 2|

## Binary Relations
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| = |Binary Relation|Equality|a = b|
| == |Binary Relation|Equality|a == b|
| <> |Binary Relation|Inequation|a <> b|
| ~= |Binary Relation|Inequation|a ~= b|
| != |Binary Relation|Inequation|a != b|
| < |Binary Relation|Lower than|a < b|
| > |Binary Relation|Greater than|a > b|
| <= |Binary Relation|Lower or equal|a <= b|
| >= |Binary Relation|Greater or equal|a >= b|

## Unary Functions
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| sin | Unary Function | Trigonometric sine function | sin(x) |
| cos | Unary Function | Trigonometric cosine function | cos(x) |
| tg | Unary Function | Trigonometric tangent function | tg(x) |
| tan | Unary Function | Trigonometric tangent function | tan(x) |
| ctg | Unary Function | Trigonometric cotangent function | ctg(x) |
| cot | Unary Function | Trigonometric cotangent function | cot(x) |
| ctan | Unary Function | Trigonometric cotangent function | ctan(x) |
| sec | Unary Function | Trigonometric secant function | sec(x) |
| csc | Unary Function | Trigonometric cosecant function | csc(x) |
| cosec | Unary Function | Trigonometric cosecant function | cosec(x) |
| asin | Unary Function | Inverse trigonometric sine function | asin(x) |
| arsin | Unary Function | Inverse trigonometric sine function | arsin(x) |
| arcsin | Unary Function | Inverse trigonometric sine function | arcsin(x) |
| acos | Unary Function | Inverse trigonometric cosine function | acos(x) |
| arcos | Unary Function | Inverse trigonometric cosine function | arcos(x) |
| arccos | Unary Function | Inverse trigonometric cosine function | arccos(x) |
| atg | Unary Function | Inverse trigonometric tangent function | atg(x) |
| atan | Unary Function | Inverse trigonometric tangent function | atan(x) |
| arctg | Unary Function | Inverse trigonometric tangent function | arctg(x) |
| arctan | Unary Function | Inverse trigonometric tangent function | arctan(x) |
| actg | Unary Function | Inverse trigonometric cotangent function | actg(x) |
| acot | Unary Function | Inverse trigonometric cotangent function | acot(x) |
| actan | Unary Function | Inverse trigonometric cotangent function | actan(x) |
| arcctg | Unary Function | Inverse trigonometric cotangent function | arcctg(x) |
| arccot | Unary Function | Inverse trigonometric cotangent function | arccot(x) |
| arcctan | Unary Function | Inverse trigonometric cotangent function | arcctan(x) |
| ln | Unary Function | Natural logarithm function (base e) | ln(x) |
| log2 | Unary Function | Binary logarithm function (base 2) | log2(x) |
| log10 | Unary Function | Common logarithm function (base 10) | log10(x) |
| rad | Unary Function | Degrees to radians function | rad(x) |
| exp | Unary Function | Exponential function | exp(x) |
| sqrt | Unary Function | Squre root function | sqrt(x) |
| sinh | Unary Function | Hyperbolic sine function | sinh(x) |
| cosh | Unary Function | Hyperbolic cosine function | cosh(x) |
| tgh | Unary Function | Hyperbolic tangent function | tgh(x) |
| tanh | Unary Function | Hyperbolic tangent function | tanh(x) |
| coth | Unary Function | Hyperbolic cotangent function | coth(x) |
| ctgh | Unary Function | Hyperbolic cotangent function | ctgh(x) |
| ctanh | Unary Function | Hyperbolic cotangent function | ctanh(x) | 
| sech | Unary Function | Hyperbolic secant function | sech(x) |
| csch | Unary Function | Hyperbolic cosecant function | csch(x) |
| cosech | Unary Function | Hyperbolic cosecant function | cosech(x) |
| deg | Unary Function | Radians to degrees function | deg(x) |
| abs | Unary Function | Absolut value function | abs(x) |
| sgn | Unary Function | Signum function | sgn(x) |
| floor | Unary Function | Floor function | floor(x) |
| ceil | Unary Function | Ceiling function | ceil(x) |
| not | Unary Function | Negation function | not(x) |
| asinh | Unary Function | Inverse hyperbolic sine function | asinh(x) |
| arsinh | Unary Function | Inverse hyperbolic sine function | arsinh(x) |
| arcsinh | Unary Function | Inverse hyperbolic sine function | arcsinh(x) |
| acosh | Unary Function | Inverse hyperbolic cosine function | acosh(x) |
| arcosh | Unary Function | Inverse hyperbolic cosine function | arcosh(x) |
| arccosh | Unary Function | Inverse hyperbolic cosine function | arccosh(x) |
| atgh | Unary Function | Inverse hyperbolic tangent function | atgh(x) |
| atanh | Unary Function | Inverse hyperbolic tangent function | atanh(x) |
| arctgh | Unary Function | Inverse hyperbolic tangent function | arctgh(x) |
| arctanh | Unary Function | Inverse hyperbolic tangent function | arctanh(x) |
| acoth | Unary Function | Inverse hyperbolic cotangent function | acoth(x) |
| actgh | Unary Function | Inverse hyperbolic cotangent function | actgh(x) |
| actanh | Unary Function | Inverse hyperbolic cotangent function | actanh(x) |
| arcoth | Unary Function | Inverse hyperbolic cotangent function | arcoth(x) |
| arccoth | Unary Function | Inverse hyperbolic cotangent function | arccoth(x) |
| arcctgh | Unary Function | Inverse hyperbolic cotangent function | arcctgh(x) |
| arcctanh | Unary Function | Inverse hyperbolic cotangent function | arcctanh(x) |
| asech | Unary Function | Inverse hyperbolic secant function | asech(x) |
| arsech | Unary Function | Inverse hyperbolic secant function | arsech(x) |
| arcsech | Unary Function | Inverse hyperbolic secant function | arcsech(x) |
| acsch | Unary Function | Inverse hyperbolic cosecant function | acsch(x) |
| arcsch | Unary Function | Inverse hyperbolic cosecant function | arcsch(x) |
| arccsch | Unary Function | Inverse hyperbolic cosecant function | arccsch(x) |
| acosech | Unary Function | Inverse hyperbolic cosecant function | acosech(x) |
| arcosech | Unary Function | Inverse hyperbolic cosecant function | arcosech(x) |
| Sa | Unary Function | Sinc function (normalized) | Sa(x) |
| sinc | Unary Function | Sinc function (normalized) | sinc(x) |
| Sinc | Unary Function | Sinc function (unnormalized) | Sinc(x) |
| Bell | Unary Function | Bell number | Bell(n) |
| Luc | Unary Function | Lucas number | Luc(n) |
| Fib | Unary Function | Fibonacci number | Fib(n) |
| harm | Unary Function | Harmonic number | harm(n) |
| ispr | Unary Function | Prime number test (is number a prime?) | ispr(n) |
| Pi | Unary Function | Prime-counting function - Pi(x) | Pi(n) |
| Ei | Unary Function | Exponential integral function (non-elementary special function) - usage example: Ei(x) | Ei(x) |
| li | Unary Function | Logarithmic integral function (non-elementary special function) - usage example: li(x) | li(x) |
| Li | Unary Function | Offset logarithmic integral function (non-elementary special function) - usage example: Li(x) | Li(x) |
| erf | Unary Function | Gauss error function (non-elementary special function) - usage example: 2 + erf(x) | erf(x) |
| erfc | Unary Function | Gauss complementary error function (non-elementary special function) - usage example: 1 - erfc(x) | erfc(x) |
| erfInv | Unary Function | Inverse Gauss error function (non-elementary special function) - usage example: erfInv(x) | erfInv(x) |
| erfcInv | Unary Function | Inverse Gauss complementary error function (non-elementary special function) - usage example: erfcInv(x) | erfcInv(x) |
| ulp | Unary Function | Unit in The Last Place - ulp(0.1) | ulp(x) |
| isNaN | Unary Function | Returns true = 1 if value is a Not-a-Number (NaN), false = 0 otherwise - usage example: isNaN(x) | isNaN(x) |
| ndig10 | Unary Function | Number of digits in numeral system with base 10 | ndig10(x) |
| nfact | Unary Function | Prime decomposition - number of distinct prime factors | nfact(x) |
| arcsec | Unary Function | Inverse trigonometric secant | arcsec(x) |
| Gamma | Unary Function |  Gamma special function Γ(s) | Gamma(x) |
| LambW0(x) | Unary Function | Lambert-W special function, principal branch 0, also called the omega function or product logarithm | LambW0(x) |
| LambW1(x) | Unary Function | Lambert-W special function, branch -1, also called the omega function or product logarithm | LambW1(x) |
| sgnGamma | Unary Function | Signum of Gamma special function, Γ(x) | sgnGamma(x) |
| logGamma | Unary Function | Log Gamma special function, lnΓ(x) | logGamma(x) |
| diGamma | Unary Function | Digamma function as the logarithmic derivative of the Gamma special function, ψ(x) | diGamma(x) |

## Binary Functions
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| log | Binary Function | Logarithm function | log(a, b) |
| mod | Binary Function | Modulo function | mod(a, b) |
| C | Binary Function | Binomial coefficient function | C(n, k) |
| Bern | Binary Function | Bernoulli numbers | Bern(m, n) |
| Stirl1 | Binary Function | Stirling numbers of the first kind | Stirl1(n, k) |
| Stirl2 | Binary Function | Stirling numbers of the second kind | Stirl2(n, k) |
| Worp | Binary Function | Worpitzky number | Worp(n, k) |
| Euler | Binary Function | Euler number | Euler(n, k) |
| KDelta | Binary Function | Kronecker delta | KDelta(i, j) |
| EulerPol | Binary Function | EulerPol | EulerPol |
| Harm | Binary Function | Harmonic number | Harm(x, n) |
| rUni | Binary Function | Random variable - Uniform continuous distribution U(a,b), usage example: 2*rUni(2,10) | rUni(a, b) |
| rUnid | Binary Function | Random variable - Uniform discrete distribution U{a,b}, usage example: 2*rUnid(2,100) | rUnid(a, b) |
| round | Binary Function | Half-up rounding, usage examples: round(2.2, 0) = 2, round(2.6, 0) = 3, round(2.66,1) = 2.7 | round(x, n) |
| rNor | Binary Function | Random variable - Normal distribution N(m,s) m - mean, s - stddev, usage example: 3*rNor(0,1) | rNor(mean, stdv) |
| ndig | Binary Function | Number of digits representing the number in numeral system with given base | ndig(number, base) |
| dig10 | Binary Function | Digit at position 1 ... n (left -> right) or 0 ... -(n-1) (right -> left) - base 10 numeral system | dig10(num, pos) |
| factval | Binary Function | Prime decomposition - factor value at position between 1 ... nfact(n) - ascending order by factor value | factval(number, factorid) |
| factexp | Binary Function | Prime decomposition - factor exponent / multiplicity at position between 1 ... nfact(n) - ascending order by factor value | factexp(number, factorid) |
| root | Binary Function | N-th order root of a number | root(rootorder, number) |
| GammaL | Binary Function | Lower incomplete gamma special function, γ(s,x) | GammaL(s,x) |
| GammaU | Binary Function | Upper incomplete Gamma special function, Γ(s,x) | GammaU(s,x) |
| GammaP | Binary Function | Lower regularized P gamma special function, P(s,x) | GammaP(s,x) |
| GammaRegL | Binary Function | Lower regularized P gamma special function, P(s,x) | GammaRegL(s,x) |
| GammaQ | Binary Function | Upper regularized Q Gamma special function, Q(s,x) | GammaQ(s,x) |
| GammaRegU | Binary Function | Upper regularized Q Gamma special function, Q(s,x) | GammaRegU(s,x) |
| Beta | Binary Function | The Beta special function B(x,y), also called the Euler integral of the first kind | Beta(x,y) |
| logBeta | Binary Function | The Log Beta special function ln B(x,y), also called the Log Euler integral of the first kind, ln B(x,y) | logBeta(x,y) |

## 3-args Functions
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| if | 3-args Function | If function | if( cond, expr-if-true, expr-if-false ) |
| chi | 3-args Function | Characteristic function for x in (a,b) | chi(x, a, b) |
| CHi | 3-args Function | Characteristic function for x in [a,b] | CHi(x, a, b) |
| Chi | 3-args Function | Characteristic function for x in [a,b) | Chi(x, a, b) |
| cHi | 3-args Function | Characteristic function for x in (a,b] | cHi(x, a, b) |
| pUni | 3-args Function | Probability distribution function - Uniform continuous distribution U(a,b) | pUni(x, a, b) |
| cUni | 3-args Function | Cumulative distribution function - Uniform continuous distribution U(a,b) | cUni(x, a, b) |
| qUni | 3-args Function | Quantile function (inverse cumulative distribution function) - Uniform continuous distribution U(a,b) | qUni(q, a, b) |
| pNor | 3-args Function | Probability distribution function - Normal distribution N(m,s) | pNor(x, mean, stdv) |
| cNor | 3-args Function | Cumulative distribution function - Normal distribution N(m,s) | cNor(x, mean, stdv) |
| qNor | 3-args Function | Quantile function (inverse cumulative distribution function) | qNor(q, mean, stdv) |
| dig | 3-args Function | Digit at position 1 ... n (left -> right) or 0 ... -(n-1) (right -> left) - numeral system with given base | dig(num, pos, base) |
| BetaInc | 3-args Function | The incomplete beta special function B(x; a, b), also called the incomplete Euler integral of the first kind | BetaInc(x,a,b) |
| BetaI | 3-args Function | The regularized incomplete beta (or regularized beta) special function I(x; a, b), also called the regularized incomplete Euler integral of the first kind | BetaI(x,a,b) |
| BetaReg | 3-args Function | The regularized incomplete beta (or regularized beta) special function I(x; a, b), also called the regularized incomplete Euler integral of the first kind | BetaReg(x,a,b) |

## Variadic Functions
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| iff | Variadic Function | If function | iff( cond-1, expr-1; ... ; cond-n, expr-n ) |
| min | Variadic Function | Minimum function | min(a1, ..., an) |
| max | Variadic Function | Maximum function | max(a1, ..., an) |
| ConFrac | Variadic Function | Continued fraction | ConFrac(a1, ..., an) |
| ConPol | Variadic Function | Continued polynomial | ConPol(a1, ..., an) |
| gcd | Variadic Function | Greatest common divisor | gcd(a1, ..., an) |
| lcm | Variadic Function | Least common multiple | lcm(a1, ..., an) |
| add | Variadic Function | Summation operator | add(a1, ..., an) |
| multi | Variadic Function | Multiplication | multi(a1, ..., an) |
| mean | Variadic Function | Mean / average value | mean(a1, ..., an) |
| var | Variadic Function | Bias-corrected sample variance | var(a1, ..., an) |
| std | Variadic Function | Bias-corrected sample standard deviation | std(a1, ..., an) |
| rList | Variadic Function | Random number from given list of numbers | rList(a1, ..., an) |
| coalesce | Variadic Function | Returns the first non-NaN value | coalesce(a1, ..., an) |
| or | Variadic Function | Logical disjunction (OR) - variadic | or(a1, ..., an) |
| and | Variadic Function | Logical conjunction (AND) - variadic | and(a1, ..., an) |
| xor | Variadic Function | Exclusive or (XOR) - variadic | xor(a1, ..., an) |
| argmin | Variadic Function | Arguments / indices of the minima | argmin(a1, ..., an) |
| argmax | Variadic Function | Arguments / indices of the maxima | argmax(a1, ..., an) |
| med | Variadic Function | The sample median | med(a1, ..., an) |
| mode | Variadic Function | Mode - the value that appears most often | mode(a1, ..., an) |
| base | Variadic Function | Returns number in given numeral system base represented by list of digits | base(b, d1, ..., dn) |
| ndist | Variadic Function | Number of distinct values | ndist(v1, ..., vn) |

## Calculus Operators / Iterated Operators
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| sum | Calculus Operator | Summation operator - SIGMA | sum( i, from, to, expr , <by> ) |
| prod | Calculus Operator | Product operator - PI | prod( i, from, to, expr , <by> ) |
| int | Calculus Operator | Definite integral operator | int( expr, arg, from, to ) |
| der | Calculus Operator | Derivative operator | der( expr, arg, <point> ) |
| der- | Calculus Operator | Left derivative operator | der-( expr, arg, <point> ) |
| der+ | Calculus Operator | Right derivative operator | der+( expr, arg, <point> ) |
| dern | Calculus Operator | n-th derivative operator | dern( expr, n, arg ) |
| diff | Calculus Operator | Forward difference operator | diff( expr, arg, <delta> ) |
| difb | Calculus Operator | Backward difference operator | difb( expr, arg, <delta> ) |
| avg | Calculus Operator | Average operator | avg( i, from, to, expr , <by> ) |
| vari | Calculus Operator | Bias-corrected sample variance operator | vari( i, from, to, expr , <by> ) |
| stdi | Calculus Operator | Bias-corrected sample standard deviation operator | stdi( i, from, to, expr , <by> ) |
| mini | Calculus Operator | Minimum value | mini( i, from, to, expr , <by> ) |
| maxi | Calculus Operator | Maximum value | maxi( i, from, to, expr , <by> ) |
| solve | Calculus Operator | f(x) = 0 equation solving, function root finding | solve( expr, a, b ) |

## Random Variables
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [Uni] |Random Variable|Random variable - Uniform continuous distribution U(0,1), usage example: 2*[Uni]|2*[Uni]|
| [Int] |Random Variable|Random variable - random integer - usage example sin( 3*[Int] )|[Int]*3|
| [Int1] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^1, 10^1} - usage example sin( 3*[Int1] )|2*[Int1]|
| [Int2] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^2, 10^2} - usage example sin( 3*[Int2] )|[Int2]*3|
| [Int3] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^3, 10^3} - usage example sin( 3*[Int3] )|2*[Int3]|
| [Int4] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^4, 10^4} - usage example sin( 3*[Int4] )|[Int4]*3|
| [Int5] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^5, 10^5} - usage example sin( 3*[Int5] )|2*[Int5]|
| [Int6] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^6, 10^6} - usage example sin( 3*[Int6] )|[Int6]*3|
| [Int7] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^7, 10^7} - usage example sin( 3*[Int7] )|2*[Int7]|
| [Int8] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^8, 10^8} - usage example sin( 3*[Int8] )|[Int8]*3|
| [Int9] |Random Variable|Random variable - random integer - Uniform discrete distribution U{-10^9, 10^9} - usage example sin( 3*[Int9] )|2*[Int9]|
| [nat] |Random Variable|Random variable - random natural number including 0 - usage example sin( 3*[nat] )|[nat]*3|
| [nat1] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^1} - usage example sin( 3*[nat1] )|2*[nat1]|
| [nat2] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^2} - usage example sin( 3*[nat2] )|[nat2]*3|
| [nat3] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^3} - usage example sin( 3*[nat3] )|2*[nat3]|
| [nat4] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^4} - usage example sin( 3*[nat4] )|[nat4]*3|
| [nat5] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^5} - usage example sin( 3*[nat5] )|2*[nat5]|
| [nat6] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^6} - usage example sin( 3*[nat6] )|[nat6]*3|
| [nat7] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^7} - usage example sin( 3*[nat7] )|2*[nat7]|
| [nat8] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^8} - usage example sin( 3*[nat8] )|[nat8]*3|
| [nat9] |Random Variable|Random variable - random natural number including 0 - Uniform discrete distribution U{0, 10^9} - usage example sin( 3*[nat9] )|2*[nat9]|
| [Nat] |Random Variable|Random variable - random natural number - usage example sin( 3*[Nat] )|[Nat]*3|
| [Nat1] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^1} - usage example sin( 3*[Nat1] )|2*[Nat1]|
| [Nat2] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^2} - usage example sin( 3*[Nat2] )|[Nat2]*3|
| [Nat3] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^3} - usage example sin( 3*[Nat3] )|2*[Nat3]|
| [Nat4] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^4} - usage example sin( 3*[Nat4] )|[Nat4]*3|
| [Nat5] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^5} - usage example sin( 3*[Nat5] )|2*[Nat5]|
| [Nat6] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^6} - usage example sin( 3*[Nat6] )|[Nat6]*3|
| [Nat7] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^7} - usage example sin( 3*[Nat7] )|2*[Nat7]|
| [Nat8] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^8} - usage example sin( 3*[Nat8] )|[Nat8]*3|
| [Nat9] |Random Variable|Random variable - random natural number - Uniform discrete distribution U{1, 10^9} - usage example sin( 3*[Nat9] )|2*[Nat9]|
| [Nor] |Random Variable|Random variable - Normal distribution N(0,1) - usage example cos( 3*[Nor]+1 )|[Nor]*3|

## Mathematical Constants
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| pi |Constant Value|Pi, Archimedes' constant or Ludolph's number|2*pi|
| e |Constant Value|Napier's constant, or Euler's number, base of Natural logarithm|e*3|
| [gam] |Constant Value|Euler-Mascheroni constant|2*[gam]|
| [phi] |Constant Value|Golden ratio|[phi]*3|
| [PN] |Constant Value|Plastic constant|2*[PN]|
| [B*] |Constant Value|Embree-Trefethen constant|[B*]*3|
| [F'd] |Constant Value|Feigenbaum constant alfa|2*[F'd]|
| [F'a] |Constant Value|Feigenbaum constant delta|[F'a]*3|
| [C2] |Constant Value|Twin prime constant|2*[C2]|
| [M1] |Constant Value|Meissel-Mertens constant|[M1]*3|
| [B2] |Constant Value|Brun's constant for twin primes|2*[B2]|
| [B4] |Constant Value|Brun's constant for prime quadruplets|[B4]*3|
| [BN'L] |Constant Value|De Bruijn-Newman constant|2*[BN'L]|
| [Kat] |Constant Value|Catalan's constant|[Kat]*3|
| [K*] |Constant Value|Landau-Ramanujan constant|2*[K*]|
| [K.] |Constant Value|Viswanath's constant|[K.]*3|
| [B'L] |Constant Value|Legendre's constant|2*[B'L]|
| [RS'm] |Constant Value|Ramanujan-Soldner constant|[RS'm]*3|
| [EB'e] |Constant Value|Erdos-Borwein constant|2*[EB'e]|
| [Bern] |Constant Value|Bernstein's constant|[Bern]*3|
| [GKW'l] |Constant Value|Gauss-Kuzmin-Wirsing constant|2*[GKW'l]|
| [HSM's] |Constant Value|Hafner-Sarnak-McCurley constant|[HSM's]*3|
| [lm] |Constant Value|Golomb-Dickman constant|2*[lm]|
| [Cah] |Constant Value|Cahen's constant|[Cah]*3|
| [Ll] |Constant Value|Laplace limit|2*[Ll]|
| [AG] |Constant Value|Alladi-Grinstead constant|[AG]*3|
| [L*] |Constant Value|Lengyel's constant|2*[L*]|
| [L.] |Constant Value|Levy's constant|[L.]*3|
| [Dz3] |Constant Value|Apery's constant|2*[Dz3]|
| [A3n] |Constant Value|Mills' constant|[A3n]*3|
| [Bh] |Constant Value|Backhouse's constant|2*[Bh]|
| [Pt] |Constant Value|Porter's constant|[Pt]*3|
| [L2] |Constant Value|Lieb's square ice constant|2*[L2]|
| [Nv] |Constant Value|Niven's constant|[Nv]*3|
| [Ks] |Constant Value|Sierpinski's constant|2*[Ks]|
| [Kh] |Constant Value|Khinchin's constant|[Kh]*3|
| [FR] |Constant Value|Fransen-Robinson constant|2*[FR]|
| [La] |Constant Value|Landau's constant|[La]*3|
| [P2] |Constant Value|Parabolic constant|2*[P2]|
| [Om] |Constant Value|Omega constant|[Om]*3|
| [MRB] |Constant Value|MRB constant|2*[MRB]|
| [li2] |Constant Value|li(2) - logarithmic integral function at x=2|[li2]*3|
| [EG] |Constant Value|Gompertz constant|2*[EG]|
| [true] | Constant Value | Boolean True represented as double, [true] = 1 | [true] |
| [false] | Constant Value | Boolean False represented as double, [false] = 0 | [false] |
| [NaN] | Constant Value | Not-a-Number | [NaN] |


## Physical Constant
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [c] |Constant Value|\<Physical Constant\> Light speed in vacuum [m/s] (m=1, s=1)|[c]*3|
| [G.] |Constant Value|\<Physical Constant\> Gravitational constant (m=1, kg=1, s=1)]|2*[G.]|
| [g] |Constant Value|\<Physical Constant\> Gravitational acceleration on Earth [m/s^2] (m=1, s=1)|[g]*3|
| [hP] |Constant Value|\<Physical Constant\> Planck constant (m=1, kg=1, s=1)|2*[hP]|
| [h-] |Constant Value|\<Physical Constant\> Reduced Planck constant / Dirac constant (m=1, kg=1, s=1)]|[h-]*3|
| [lP] |Constant Value|\<Physical Constant\> Planck length [m] (m=1)|2*[lP]|
| [mP] |Constant Value|\<Physical Constant\> Planck mass [kg] (kg=1)|[mP]*3|
| [tP] |Constant Value|\<Physical Constant\> Planck time [s] (s=1)|2*[tP]|

## Astronomical Constant
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [ly] |Constant Value|\<Astronomical Constant\> Light year [m] (m=1)|[ly]*3|
| [au] |Constant Value|\<Astronomical Constant\> Astronomical unit [m] (m=1)|2*[au]|
| [pc] |Constant Value|\<Astronomical Constant\> Parsec [m] (m=1)|[pc]*3|
| [kpc] |Constant Value|\<Astronomical Constant\> Kiloparsec [m] (m=1)|2*[kpc]|
| [Earth-R-eq] |Constant Value|\<Astronomical Constant\> Earth equatorial radius [m] (m=1)|[Earth-R-eq]*3|
| [Earth-R-po] |Constant Value|\<Astronomical Constant\> Earth polar radius [m] (m=1)|2*[Earth-R-po]|
| [Earth-R] |Constant Value|\<Astronomical Constant\> Earth mean radius (m=1)|[Earth-R]*3|
| [Earth-M] |Constant Value|\<Astronomical Constant\> Earth mass [kg] (kg=1)|2*[Earth-M]|
| [Earth-D] |Constant Value|\<Astronomical Constant\> Earth-Sun distance - semi major axis [m] (m=1)|[Earth-D]*3|
| [Moon-R] |Constant Value|\<Astronomical Constant\> Moon mean radius [m] (m=1)|2*[Moon-R]|
| [Moon-M] |Constant Value|\<Astronomical Constant\> Moon mass [kg] (kg=1)|[Moon-M]*3|
| [Moon-D] |Constant Value|\<Astronomical Constant\> Moon-Earth distance - semi major axis [m] (m=1)|2*[Moon-D]|
| [Solar-R] |Constant Value|\<Astronomical Constant\> Solar mean radius [m] (m=1)|[Solar-R]*3|
| [Solar-M] |Constant Value|\<Astronomical Constant\> Solar mass [kg] (kg=1)|2*[Solar-M]|
| [Mercury-R] |Constant Value|\<Astronomical Constant\> Mercury mean radius [m] (m=1)|[Mercury-R]*3|
| [Mercury-M] |Constant Value|\<Astronomical Constant\> Mercury mass [kg] (kg=1)|2*[Mercury-M]|
| [Mercury-D] |Constant Value|\<Astronomical Constant\> Mercury-Sun distance - semi major axis [m] (m=1)|[Mercury-D]*3|
| [Venus-R] |Constant Value|\<Astronomical Constant\> Venus mean radius [m] (m=1)|2*[Venus-R]|
| [Venus-M] |Constant Value|\<Astronomical Constant\> Venus mass [kg] (kg=1)|[Venus-M]*3|
| [Venus-D] |Constant Value|\<Astronomical Constant\> Venus-Sun distance - semi major axis [m] (m=1)|2*[Venus-D]|
| [Mars-R] |Constant Value|\<Astronomical Constant\> Mars mean radius [m] (m=1)|[Mars-R]*3|
| [Mars-M] |Constant Value|\<Astronomical Constant\> Mars mass [kg] (kg=1)|2*[Mars-M]|
| [Mars-D] |Constant Value|\<Astronomical Constant\> Mars-Sun distance - semi major axis [m] (m=1)|[Mars-D]*3|
| [Jupiter-R] |Constant Value|\<Astronomical Constant\> Jupiter mean radius [m] (m=1)|2*[Jupiter-R]|
| [Jupiter-M] |Constant Value|\<Astronomical Constant\> Jupiter mass [kg] (kg=1)|[Jupiter-M]*3|
| [Jupiter-D] |Constant Value|\<Astronomical Constant\> Jupiter-Sun distance - semi major axis [m] (m=1)|2*[Jupiter-D]|
| [Saturn-R] |Constant Value|\<Astronomical Constant\> Saturn mean radius [m] (m=1)|[Saturn-R]*3|
| [Saturn-M] |Constant Value|\<Astronomical Constant\> Saturn mass [kg] (kg=1)|2*[Saturn-M]|
| [Saturn-D] |Constant Value|\<Astronomical Constant\> Saturn-Sun distance - semi major axis [m] (m=1)|[Saturn-D]*3|
| [Uranus-R] |Constant Value|\<Astronomical Constant\> Uranus mean radius [m] (m=1)|2*[Uranus-R]|
| [Uranus-M] |Constant Value|\<Astronomical Constant\> Uranus mass [kg] (kg=1)|[Uranus-M]*3|
| [Uranus-D] |Constant Value|\<Astronomical Constant\> Uranus-Sun distance - semi major axis [m] (m=1)|2*[Uranus-D]|
| [Neptune-R] |Constant Value|\<Astronomical Constant\> Neptune mean radius [m] (m=1)|[Neptune-R]*3|
| [Neptune-M] |Constant Value|\<Astronomical Constant\> Neptune mass [kg] (kg=1)|2*[Neptune-M]|
| [Neptune-D] |Constant Value|\<Astronomical Constant\> Neptune-Sun distance - semi major axis [m] (m=1)|[Neptune-D]*3|

## Metric prefixes
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [%] |Unit|\<Ratio, Fraction\> Percentage = 0.01|2*[%]|
| [%%] |Unit|\<Ratio, Fraction\> Promil, Per mille = 0.001|[%%]*3|
| [Y] |Unit|\<Metric prefix\> Septillion / Yotta = 10^24|2*[Y]|
| [sept] |Unit|\<Metric prefix\> Septillion / Yotta = 10^24|[sept]*3|
| [Z] |Unit|\<Metric prefix\> Sextillion / Zetta = 10^21|2*[Z]|
| [sext] |Unit|\<Metric prefix\> Sextillion / Zetta = 10^21|[sext]*3|
| [E] |Unit|\<Metric prefix\> Quintillion / Exa = 10^18|2*[E]|
| [quint] |Unit|\<Metric prefix\> Quintillion / Exa = 10^18|[quint]*3|
| [P] |Unit|\<Metric prefix\> Quadrillion / Peta = 10^15|2*[P]|
| [quad] |Unit|\<Metric prefix\> Quadrillion / Peta = 10^15|[quad]*3|
| [T] |Unit|\<Metric prefix\> Trillion / Tera = 10^12|2*[T]|
| [tril] |Unit|\<Metric prefix\> Trillion / Tera = 10^12|[tril]*3|
| [G] |Unit|\<Metric prefix\> Billion / Giga = 10^9|2*[G]|
| [bil] |Unit|\<Metric prefix\> Billion / Giga = 10^9|[bil]*3|
| [M] |Unit|\<Metric prefix\> Million / Mega = 10^6|2*[M]|
| [mil] |Unit|\<Metric prefix\> Million / Mega = 10^6|[mil]*3|
| [k] |Unit|\<Metric prefix\> Thousand / Kilo = 10^3|2*[k]|
| [th] |Unit|\<Metric prefix\> Thousand / Kilo = 10^3|[th]*3|
| [hecto] |Unit|\<Metric prefix\> Hundred / Hecto = 10^2|2*[hecto]|
| [hund] |Unit|\<Metric prefix\> Hundred / Hecto = 10^2|[hund]*3|
| [deca] |Unit|\<Metric prefix\> Ten / Deca = 10|2*[deca]|
| [ten] |Unit|\<Metric prefix\> Ten / Deca = 10|[ten]*3|
| [deci] |Unit|\<Metric prefix\> Tenth / Deci = 0.1|2*[deci]|
| [centi] |Unit|\<Metric prefix\> Hundredth / Centi = 0.01|[centi]*3|
| [milli] |Unit|\<Metric prefix\> Thousandth / Milli = 0.001|2*[milli]|
| [mic] |Unit|\<Metric prefix\> Millionth / Micro = 10^-6|[mic]*3|
| [n] |Unit|\<Metric prefix\> Billionth / Nano = 10^-9|2*[n]|
| [p] |Unit|\<Metric prefix\> Trillionth / Pico = 10^-12|[p]*3|
| [f] |Unit|\<Metric prefix\> Quadrillionth / Femto = 10^-15|2*[f]|
| [a] |Unit|\<Metric prefix\> Quintillionth / Atoo = 10^-18|[a]*3|
| [z] |Unit|\<Metric prefix\> Sextillionth / Zepto = 10^-21|2*[z]|
| [y] |Unit|\<Metric prefix\> Septillionth / Yocto = 10^-24|[y]*3|

## Units of length
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [m] |Unit|\<Unit of length\> Metre / Meter (m=1)|2*[m]|
| [km] |Unit|\<Unit of length\> Kilometre / Kilometer (m=1)|[km]*3|
| [cm] |Unit|\<Unit of length\> Centimetre / Centimeter (m=1)|2*[cm]|
| [mm] |Unit|\<Unit of length\> Millimetre / Millimeter (m=1)|[mm]*3|
| [inch] |Unit|\<Unit of length\> Inch (m=1)|2*[inch]|
| [yd] |Unit|\<Unit of length\> Yard (m=1)|[yd]*3|
| [ft] |Unit|\<Unit of length\> Feet (m=1)|2*[ft]|
| [mile] |Unit|\<Unit of length\> Mile (m=1)|[mile]*3|
| [nmi] |Unit|\<Unit of length\> Nautical mile (m=1)|2*[nmi]|

## Units of area
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [m2] |Unit|\<Unit of area\> Square metre / Square meter (m=1)|[m2]*3|
| [cm2] |Unit|\<Unit of area\> Square centimetre / Square centimeter (m=1)|2*[cm2]|
| [mm2] |Unit|\<Unit of area\> Square millimetre / Square millimeter (m=1)|[mm2]*3|
| [are] |Unit|\<Unit of area\> Are (m=1)|2*[are]|
| [ha] |Unit|\<Unit of area\> Hectare (m=1)|[ha]*3|
| [acre] |Unit|\<Unit of area\> Acre (m=1)|2*[acre]|
| [km2] |Unit|\<Unit of area\> Square kilometre / Square kilometer (m=1)|[km2]*3|

## Units of volume
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [mm3] |Unit|\<Unit of volume\> Cubic millimetre / Cubic millimeter (m=1)|2*[mm3]|
| [cm3] |Unit|\<Unit of volume\> Cubic centimetre / Cubic centimeter (m=1)|[cm3]*3|
| [m3] |Unit|\<Unit of volume\> Cubic metre / Cubic meter (m=1)|2*[m3]|
| [km3] |Unit|\<Unit of volume\> Cubic kilometre / Cubic kilometer (m=1)|[km3]*3|
| [ml] |Unit|\<Unit of volume\> Millilitre / Milliliter (m=1)|2*[ml]|
| [l] |Unit|\<Unit of volume\> Litre / Liter (m=1)|[l]*3|
| [gall] |Unit|\<Unit of volume\> Gallon (m=1)|2*[gall]|
| [pint] |Unit|\<Unit of volume\> Pint (m=1)|[pint]*3|

## Units of time
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [s] |Unit|\<Unit of time\> Second (s=1)|2*[s]|
| [ms] |Unit|\<Unit of time\> Millisecond (s=1)|[ms]*3|
| [min] |Unit|\<Unit of time\> Minute (s=1)|2*[min]|
| [h] |Unit|\<Unit of time\> Hour (s=1)|[h]*3|
| [day] |Unit|\<Unit of time\> Day (s=1)|2*[day]|
| [week] |Unit|\<Unit of time\> Week (s=1)|[week]*3|
| [yearj] |Unit|\<Unit of time\> Julian year = 365.25 days (s=1)|2*[yearj]|

## Units of mass
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [kg] |Unit|\<Unit of mass\> Kilogram (kg=1)|[kg]*3|
| [gr] |Unit|\<Unit of mass\> Gram (kg=1)|2*[gr]|
| [mg] |Unit|\<Unit of mass\> Milligram (kg=1)|[mg]*3|
| [dag] |Unit|\<Unit of mass\> Decagram (kg=1)|2*[dag]|
| [t] |Unit|\<Unit of mass\> Tonne (kg=1)|[t]*3|
| [oz] |Unit|\<Unit of mass\> Ounce (kg=1)|2*[oz]|
| [lb] |Unit|\<Unit of mass\> Pound (kg=1)|[lb]*3|

## Units of information
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [b] |Unit|\<Unit of information\> Bit (bit=1)|2*[b]|
| [kb] |Unit|\<Unit of information\> Kilobit (bit=1)|[kb]*3|
| [Mb] |Unit|\<Unit of information\> Megabit (bit=1)|2*[Mb]|
| [Gb] |Unit|\<Unit of information\> Gigabit (bit=1)|[Gb]*3|
| [Tb] |Unit|\<Unit of information\> Terabit (bit=1)|2*[Tb]|
| [Pb] |Unit|\<Unit of information\> Petabit (bit=1)|[Pb]*3|
| [Eb] |Unit|\<Unit of information\> Exabit (bit=1)|2*[Eb]|
| [Zb] |Unit|\<Unit of information\> Zettabit (bit=1)|[Zb]*3|
| [Yb] |Unit|\<Unit of information\> Yottabit (bit=1)|2*[Yb]|
| [B] |Unit|\<Unit of information\> Byte (bit=1)|[B]*3|
| [kB] |Unit|\<Unit of information\> Kilobyte (bit=1)|2*[kB]|
| [MB] |Unit|\<Unit of information\> Megabyte (bit=1)|[MB]*3|
| [GB] |Unit|\<Unit of information\> Gigabyte (bit=1)|2*[GB]|
| [TB] |Unit|\<Unit of information\> Terabyte (bit=1)|[TB]*3|
| [PB] |Unit|\<Unit of information\> Petabyte (bit=1)|2*[PB]|
| [EB] |Unit|\<Unit of information\> Exabyte (bit=1)|[EB]*3|
| [ZB] |Unit|\<Unit of information\> Zettabyte (bit=1)|2*[ZB]|
| [YB] |Unit|\<Unit of information\> Yottabyte (bit=1)|[YB]*3|

## Units of energy
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [J] |Unit|\<Unit of energy\> Joule (m=1, kg=1, s=1)|2*[J]|
| [eV] |Unit|\<Unit of energy\> Electronovolt (m=1, kg=1, s=1)|[eV]*3|
| [keV] |Unit|\<Unit of energy\> Kiloelectronovolt (m=1, kg=1, s=1)|2*[keV]|
| [MeV] |Unit|\<Unit of energy\> Megaelectronovolt (m=1, kg=1, s=1)|[MeV]*3|
| [GeV] |Unit|\<Unit of energy\> Gigaelectronovolt (m=1, kg=1, s=1)|2*[GeV]|
| [TeV] |Unit|\<Unit of energy\> Teraelectronovolt (m=1, kg=1, s=1)|[TeV]*3|

## Units of speed
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [m/s] |Unit|\<Unit of speed\> Metre / Meter per second (m=1, s=1)|2*[m/s]|
| [km/h] |Unit|\<Unit of speed\> Kilometre / Kilometer per hour (m=1, s=1)|[km/h]*3|
| [mi/h] |Unit|\<Unit of speed\> Mile per hour (m=1, s=1)|2*[mi/h]|
| [knot] |Unit|\<Unit of speed\> Knot (m=1, s=1)|[knot]*3|

## Units of acceleration
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [m/s2] |Unit|\<Unit of acceleration\> Metre / Meter per square second (m=1, s=1)|2*[m/s2]|
| [km/h2] |Unit|\<Unit of acceleration\> Kilometre / Kilometer per square hour (m=1, s=1)|[km/h2]*3|
| [mi/h2] |Unit|\<Unit of acceleration\> Mile per square hour (m=1, s=1)|2*[mi/h2]|

## Units of angle
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| [rad] |Unit|\<Unit of angle\> Radian (rad=1)|[rad]*pi|
| [deg] |Unit|\<Unit of angle\> Degree of arc (rad=1)|180*[deg]|
| ['] |Unit|\<Unit of angle\> Minute of arc (rad=1)|[']*3|
| [''] |Unit|\<Unit of angle\> Second of arc (rad=1)|2*['']|

## Other parser symbols
|Keyword|Category|Description|Example|
|---|---|---|---|---|
| ( |Parser Symbol|Left parentheses|(3+2)/4|
| ) |Parser Symbol|Right parentheses|(3+2)/4|
| , |Parser Symbol|Comma (function parameters)|min(2,3,1)|
| ; |Parser Symbol|Semicolon (function parameters)|min(2;3;1)|
