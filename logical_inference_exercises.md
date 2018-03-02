<!DOCTYPE HTML>
<html>
	<head>
		<title>Exercises</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<link rel="stylesheet" href="assets/css/main.css" />
	</head>
	<body class="subpage">

		<!-- Header -->
			<header id="header" class="alt">
				<div class="logo"><a href="index.html">AIMA <span>Exercises</span></a></div>
				<a href="#menu"><span>Menu</span></a>
			</header>

		<!-- Nav -->
			<nav id="menu">
				<ul class="links">
					<li><a href="index.html">Home</a></li>
					<li><a href="info.html">More Info</a></li>
					<li><a href="exercises.html">Exercises</a></li>
				</ul>
			</nav>
		<!-- Main -->
			<div id="main" class="container" style = " text-align: left; ">

				<!-- Content -->
				<h5><b>EXERCISES</b></h1>
        <h1 id="9inferenceinfirstorderlogic">9. Inference in First-Order Logic</h1>

<p><strong>9.1</strong> Prove that Universal Instantiation is sound and that Existential
Instantiation produces an inferentially equivalent knowledge base.</p>

<p><strong>9.2</strong> From ${Likes}({Jerry},{IceCream})$ it seems reasonable to infer
${\exists,x\;\;}
{Likes}(x,{IceCream})$. Write down a general inference rule, , that
sanctions this inference. State carefully the conditions that must be
satisfied by the variables and terms involved.</p>

<p><strong>9.3</strong> Suppose a knowledge base contains just one sentence,
$\exists,x\ {AsHighAs}(x,{Everest})$. Which of the following are
legitimate results of applying Existential Instantiation?</p>

<ol>
<li><p>${AsHighAs}({Everest},{Everest})$.</p></li>

<li><p>${AsHighAs}({Kilimanjaro},{Everest})$.</p></li>

<li><p>${AsHighAs}({Kilimanjaro},{Everest}) \land {AsHighAs}({BenNevis},{Everest})$\
(after two applications).</p></li>
</ol>

<p><strong>9.4</strong> For each pair of atomic sentences, give the most general unifier if it
exists:</p>

<ol>
<li><p>$P(A,B,B)$, $P(x,y,z)$.</p></li>

<li><p>$Q(y,G(A,B))$, $Q(G(x,x),y)$.</p></li>

<li><p>${Older}({Father}(y),y)$, ${Older}({Father}(x),{John})$.</p></li>

<li><p>${Knows}({Father}(y),y)$, ${Knows}(x,x)$.</p></li>
</ol>

<p><strong>9.5</strong> For each pair of atomic sentences, give the most general unifier if it
exists:</p>

<ol>
<li><p>$P(A,A,B)$, $P(x,y,z)$.</p></li>

<li><p>$Q(y,G(A,B))$, $Q(G(x,x),y)$.</p></li>

<li><p>${Older}({Father}(y),y)$, ${Older}({Father}(x),{Jerry})$.</p></li>

<li><p>${Knows}({Father}(y),y)$, ${Knows}(x,x)$.</p></li>
</ol>

<p><strong>9.6</strong> [subsumption-lattice-exercise]Consider the subsumption lattices shown
in Figure <a href="#/">subsumption-lattice-figure</a>
(page <a href="#/">subsumption-lattice-figure</a>).</p>

<ol>
<li><p>Construct the lattice for the sentence
${Employs}({Mother}({John}),{Father}({Richard}))$.</p></li>

<li><p>Construct the lattice for the sentence ${Employs}({IBM},y)$
(“Everyone works for IBM”). Remember to include every kind of query
that unifies with the sentence.</p></li>

<li><p>Assume that indexes each sentence under every node in its
subsumption lattice. Explain how should work when some of these
sentences contain variables; use as examples the sentences in (a)
and (b) and the query ${Employs}(x,{Father}(x))$.</p></li>
</ol>

<p><strong>9.7</strong> [fol-horses-exercise]Write down logical representations for the
following sentences, suitable for use with Generalized Modus Ponens:</p>

<ol>
<li><p>Horses, cows, and pigs are mammals.</p></li>

<li><p>An offspring of a horse is a horse.</p></li>

<li><p>Bluebeard is a horse.</p></li>

<li><p>Bluebeard is Charlie’s parent.</p></li>

<li><p>Offspring and parent are inverse relations.</p></li>

<li><p>Every mammal has a parent.</p></li>
</ol>

<p><strong>9.8</strong> These questions concern concern issues with substitution and
Skolemization.</p>

<ol>
<li><p>Given the premise ${\forall,x\;\;} {\exists,y\;\;} P(x,y)$, it is
not valid to conclude that ${\exists,q\;\;} P(q,q)$. Give an
example of a predicate $P$ where the first is true but the second
is false.</p></li>

<li><p>Suppose that an inference engine is incorrectly written with the
occurs check omitted, so that it allows a literal like $P(x,F(x))$
to be unified with $P(q,q)$. (As mentioned, most standard
implementations of Prolog actually do allow this.) Show that such an
inference engine will allow the conclusion ${\exists,y\;\;} P(q,q)$
to be inferred from the premise
${\forall,x\;\;} {\exists,y\;\;} P(x,y)$.</p></li>

<li><p>Suppose that a procedure that converts first-order logic to clausal
form incorrectly Skolemizes
${\forall,x\;\;} {\exists,y\;\;} P(x,y)$ to $P(x,Sk0)$—that is, it
replaces $y$ by a Skolem constant rather than by a Skolem function
of $x$. Show that an inference engine that uses such a procedure
will likewise allow ${\exists,q\;\;} P(q,q)$ to be inferred from
the premise ${\forall,x\;\;} {\exists,y\;\;} P(x,y)$.</p></li>

<li><p>A common error among students is to suppose that, in unification,
one is allowed to substitute a term for a Skolem constant instead of
for a variable. For instance, they will say that the formulas
$P(Sk1)$ and $P(A)$ can be unified under the substitution
${ Sk1/A }$. Give an example where this leads to an
invalid inference.</p></li>
</ol>

<p><strong>9.9</strong> This question considers Horn KBs, such as the following:
$$\begin{array}{l}
P(F(x)) {\:\;{\Rightarrow}\:\;}P(x)\
Q(x) {\:\;{\Rightarrow}\:\;}P(F(x))\
P(A)\
Q(B)
\end{array}$$ Let FC be a breadth-first forward-chaining algorithm that
repeatedly adds all consequences of currently satisfied rules; let BC be
a depth-first left-to-right backward-chaining algorithm that tries
clauses in the order given in the KB. Which of the following are true?</p>

<ol>
<li><p>FC will infer the literal $Q(A)$.</p></li>

<li><p>FC will infer the literal $P(B)$.</p></li>

<li><p>If FC has failed to infer a given literal, then it is not entailed
by the KB.</p></li>

<li><p>BC will return ${true}$ given the query $P(B)$.</p></li>

<li><p>If BC does not return ${true}$ given a query literal, then it is
not entailed by the KB.</p></li>
</ol>

<p><strong>9.10</strong> [csp-clause-exercise]Explain how to write any given 3-SAT problem of
arbitrary size using a single first-order definite clause and no more
than 30 ground facts.</p>

<p><strong>9.11</strong> Suppose you are given the following axioms:</p>

<blockquote>
  <ol>
  <li>$0 \leq 3$.</li>
  
  <li>$7 \leq 9$.</li>
  
  <li>${\forall,x\;\;} \; \; x \leq x$.</li>
  
  <li>${\forall,x\;\;} \; \; x \leq x+0$.</li>
  
  <li>${\forall,x\;\;} \; \; x+0 \leq x$.</li>
  
  <li>${\forall,x,y\;\;} \; \; x+y \leq y+x$.</li>
  
  <li>${\forall,w,x,y,z\;\;} \; \; w \leq y$ $\wedge$ $x \leq z$ ${\:\;{\Rightarrow}\:\;}$ $w+x \leq y+z$.</li>
  
  <li>${\forall,x,y,z\;\;} \; \; x \leq y \wedge y \leq z \: {\:\;{\Rightarrow}\:\;}\: x \leq z$</li>
  </ol>
</blockquote>

<ol>
<li><p>Give a backward-chaining proof of the sentence $7 \leq 3+9$. (Be
sure, of course, to use only the axioms given here, not anything
else you may know about arithmetic.) Show only the steps that leads
to success, not the irrelevant steps.</p></li>

<li><p>Give a forward-chaining proof of the sentence $7 \leq 3+9$. Again,
show only the steps that lead to success.</p></li>
</ol>

<p><strong>9.12</strong> Suppose you are given the following axioms:</p>

<blockquote>
  <ol>
  <li><p>$0 \leq 4$.</p></li>
  
  <li><p>$5 \leq 9$.</p></li>
  
  <li><p>${\forall,x\;\;} \; \; x \leq x$.</p></li>
  
  <li><p>${\forall,x\;\;} \; \; x \leq x+0$.</p></li>
  
  <li><p>${\forall,x\;\;} \; \; x+0 \leq x$.</p></li>
  
  <li><p>${\forall,x,y\;\;} \; \; x+y \leq y+x$.</p></li>
  
  <li><p>${\forall,w,x,y,z\;\;} \; \; w \leq y$ $\wedge$ $x \leq z {\:\;{\Rightarrow}\:\;}$ $w+x \leq y+z$.</p></li>
  
  <li><p>${\forall,x,y,z\;\;} \; \; x \leq y \wedge y \leq z \: {\:\;{\Rightarrow}\:\;}\: x \leq z$</p></li>
  </ol>
</blockquote>

<ol>
<li><p>Give a backward-chaining proof of the sentence $5 \leq 4+9$. (Be
sure, of course, to use only the axioms given here, not anything
else you may know about arithmetic.) Show only the steps that leads
to success, not the irrelevant steps.</p></li>

<li><p>Give a forward-chaining proof of the sentence $5 \leq 4+9$. Again,
show only the steps that lead to success.</p></li>
</ol>

<p><strong>9.13</strong> A popular children’s riddle is “Brothers and sisters have I none, but
that man’s father is my father’s son.” Use the rules of the family
domain (Section <a href="#/">kinship-domain-section</a> on
page <a href="#/">kinship-domain-section</a>) to show who that man is. You may apply any of the
inference methods described in this chapter. Why do you think that this
riddle is difficult?</p>

<p><strong>9.14</strong> Suppose we put into a logical knowledge base a segment of the
U.S. census data listing the age, city of residence, date of birth, and
mother of every person, using social security numbers as identifying
constants for each person. Thus, George’s age is given by
${Age}(\mbox{{443}}-{65}-{1282}}, {56})$. Which of the following
indexing schemes S1–S5 enable an efficient solution for which of the
queries Q1–Q4 (assuming normal backward chaining)?</p>

<ul>
<li><strong>S1</strong>: an index for each atom in each position.</li>

<li><strong>S2</strong>: an index for each first argument.</li>

<li><strong>S3</strong>: an index for each predicate atom.</li>

<li><strong>S4</strong>: an index for each <em>combination</em> of predicate and first argument.</li>

<li><strong>S5</strong>: an index for each <em>combination</em> of predicate and second argument and an index for each first argument.</li>

<li><strong>Q1</strong>: ${Age}(\mbox 443-44-4321,x)$</li>

<li><strong>Q2</strong>: ${ResidesIn}(x,{Houston})$</li>

<li><strong>Q3</strong>: ${Mother}(x,y)$</li>

<li><strong>Q4</strong>: ${Age}(x,{34}) \land {ResidesIn}(x,{TinyTownUSA})$</li>
</ul>

<p><strong>9.15</strong> [standardize-failure-exercise]One might suppose that we can avoid the
problem of variable conflict in unification during backward chaining by
standardizing apart all of the sentences in the knowledge base once and
for all. Show that, for some sentences, this approach cannot work.
(<em>Hint</em>: Consider a sentence in which one part unifies with
another.)</p>

<p><strong>9.16</strong> In this exercise, use the sentences you wrote in
Exercise <a href="#/">fol-horses-exercise</a> to answer a question by
using a backward-chaining algorithm.</p>

<ol>
<li><p>Draw the proof tree generated by an exhaustive backward-chaining
algorithm for the query ${\exists,h\;\;}{Horse}(h)$, where
clauses are matched in the order given.</p></li>

<li><p>What do you notice about this domain?</p></li>

<li><p>How many solutions for $h$ actually follow from your sentences?</p></li>

<li><p>Can you think of a way to find all of them? (<em>Hint</em>:
See @Smith+al:1986.)</p></li>
</ol>

<p><strong>9.17</strong> [bc-trace-exercise]Trace the execution of the backward-chaining
algorithm in Figure <a href="#/">backward-chaining-algorithm</a>
(page <a href="#/">backward-chaining-algorithm</a>) when it is applied to solve the crime problem
(page <a href="#/">west-problem-page</a>). Show the sequence of values taken on by the
${goals}$ variable, and arrange them into a tree.</p>

<p><strong>9.18</strong> The following Prolog code defines a predicate P. (Remember
that uppercase terms are variables, not constants, in Prolog.)</p>

<pre><code>    P(X,[X|Y]).
    P(X,[Y|Z]) :- P(X,Z).
</code></pre>

<ol>
<li><p>Show proof trees and solutions for the queries
P(A,[2,1,3]) and P(2,[1,A,3]).</p></li>

<li><p>What standard list operation does P represent?</p></li>
</ol>

<p><strong>9.19</strong> The following Prolog code defines a predicate P. (Remember
that uppercase terms are variables, not constants, in Prolog.)</p>

<pre><code>    P(X,[X|Y]).
    P(X,[Y|Z]) :- P(X,Z).
</code></pre>

<ol>
<li><p>Show proof trees and solutions for the queries
P(A,[1,2,3]) and P(2,[1,A,3]).</p></li>

<li><p>What standard list operation does P represent?</p></li>
</ol>

<p><strong>9.20</strong> This exercise looks at sorting in Prolog.</p>

<ol>
<li><p>Write Prolog clauses that define the predicate
sorted(L), which is true if and only if list
L is sorted in ascending order.</p></li>

<li><p>Write a Prolog definition for the predicate perm(L,M),
which is true if and only if L is a permutation of
M.</p></li>

<li><p>Define sort(L,M) (M is a sorted version of
L) using perm and sorted.</p></li>

<li><p>Run sort on longer and longer lists until you lose
patience. What is the time complexity of your program?</p></li>

<li><p>Write a faster sorting algorithm, such as insertion sort or
quicksort, in Prolog.</p></li>
</ol>

<p><strong>9.21</strong> [diff-simplify-exercise]This exercise looks at the recursive
application of rewrite rules, using logic programming. A rewrite rule
(or <strong>demodulator</strong> in terminology) is an
equation with a specified direction. For example, the rewrite rule
$x+0 \rightarrow x$ suggests replacing any expression that matches $x+0$
with the expression $x$. Rewrite rules are a key component of equational
reasoning systems. Use the predicate rewrite(X,Y) to
represent rewrite rules. For example, the earlier rewrite rule is
written as rewrite(X+0,X). Some terms are
<em>primitive</em> and cannot be further simplified; thus, we
write primitive(0) to say that 0 is a primitive term.</p>

<ol>
<li><p>Write a definition of a predicate simplify(X,Y), that
is true when Y is a simplified version of
X—that is, when no further rewrite rules apply to any
subexpression of Y.</p></li>

<li><p>Write a collection of rules for the simplification of expressions
involving arithmetic operators, and apply your simplification
algorithm to some sample expressions.</p></li>

<li><p>Write a collection of rewrite rules for symbolic differentiation,
and use them along with your simplification rules to differentiate
and simplify expressions involving arithmetic expressions,
including exponentiation.</p></li>
</ol>

<p><strong>9.22</strong> This exercise considers the implementation of search algorithms in
Prolog. Suppose that successor(X,Y) is true when state
Y is a successor of state X; and that
goal(X) is true when X is a goal state. Write
a definition for solve(X,P), which means that
P is a path (list of states) beginning with X,
ending in a goal state, and consisting of a sequence of legal steps as
defined by successor. You will find that depth-first search
is the easiest way to do this. How easy would it be to add heuristic
search control?</p>

<p><strong>9.23</strong> Suppose a knowledge base contains just the following first-order Horn
clauses:</p>

<p>$$
Ancestor(Mother(x),x)
$$
$$
Ancestor(x,y) \land Ancestor(y,z) \implies Ancestor(x,z)
$$</p>

<p>Consider a forward chaining algorithm that, on the $j$th iteration,
terminates if the KB contains a sentence that unifies with the query,
else adds to the KB every atomic sentence that can be inferred from the
sentences already in the KB after iteration $j-1$.</p>

<ol>
<li><p>For each of the following queries, say whether the algorithm
will (1) give an answer (if so, write down that answer); or (2)
terminate with no answer; or (3) never terminate.</p>

<ol>
<li><p>$Ancestor(Mother(y),John)$</p></li>

<li><p>$Ancestor(Mother(Mother(y)),John)$</p></li>

<li><p>$Ancestor(Mother(Mother(Mother(y))),Mother(y))$</p></li>

<li><p>$Ancestor(Mother(John),Mother(Mother(John)))$</p></li></ol></li>

<li><p>Can a resolution algorithm prove the sentence
$\lnot Ancestor(John,John)$ from the original knowledge base?
Explain how, or why not.</p></li>

<li><p>Suppose we add the assertion that $\lnot(Mother(x){{,=,}}x)$ and
augment the resolution algorithm with inference rules for equality.
Now what is the answer to (b)?</p></li>
</ol>

<p><strong>9.24</strong> Let $\cal L$ be the first-order language with a single predicate
$S(p,q)$, meaning “$p$ shaves  $q$.” Assume a domain of people.</p>

<ol>
<li><p>Consider the sentence “There exists a person $P$ who shaves every
one who does not shave themselves, and only people that do not
shave themselves.” Express this in $\cal L$.</p></li>

<li><p>Convert the sentence in (a) to clausal form.</p></li>

<li><p>Construct a resolution proof to show that the clauses in (b) are
inherently inconsistent. (Note: you do not need any
additional axioms.)</p></li>
</ol>

<p><strong>9.25</strong> How can resolution be used to show that a sentence is valid?
Unsatisfiable?</p>

<p><strong>9.26</strong> Construct an example of two clauses that can be resolved together in two
different ways giving two different outcomes.</p>

<p><strong>9.27</strong> From “Horses are animals,” it follows that “The head of a horse is the
head of an animal.” Demonstrate that this inference is valid by carrying
out the following steps:</p>

<ol>
<li><p>Translate the premise and the conclusion into the language of
first-order logic. Use three predicates: ${HeadOf}(h,x)$ (meaning
“$h$ is the head of $x$”), ${Horse}(x)$, and ${Animal}(x)$.</p></li>

<li><p>Negate the conclusion, and convert the premise and the negated
conclusion into conjunctive normal form.</p></li>

<li><p>Use resolution to show that the conclusion follows from the premise.</p></li>
</ol>

<p><strong>9.28</strong> From “Sheep are animals,” it follows that “The head of a sheep is the
head of an animal.” Demonstrate that this inference is valid by carrying
out the following steps:</p>

<ol>
<li><p>Translate the premise and the conclusion into the language of
first-order logic. Use three predicates: ${HeadOf}(h,x)$ (meaning
“$h$ is the head of $x$”), ${Sheep}(x)$, and ${Animal}(x)$.</p></li>

<li><p>Negate the conclusion, and convert the premise and the negated
conclusion into conjunctive normal form.</p></li>

<li><p>Use resolution to show that the conclusion follows from the premise.</p></li>
</ol>

<p><strong>9.29</strong> [quantifier-order-exercise]Here are two sentences in the language of
first-order logic:</p>

<ul>
<li><p><strong>(A)</strong>
${\forall,x\;\;} {\exists,y\;\;} ( x \geq y )$</p></li>

<li><p><strong>(B)</strong>
${\exists,y\;\;} {\forall,x\;\;} ( x \geq y )$</p></li>
</ul>

<ol>
<li><p>Assume that the variables range over all the natural numbers
$0,1,2,\ldots, \infty$ and that the “$\geq$” predicate means “is
greater than or equal to.” Under this interpretation, translate (A)
and (B) into English.</p></li>

<li><p>Is (A) true under this interpretation?</p></li>

<li><p>Is (B) true under this interpretation?</p></li>

<li><p>Does (A) logically entail (B)?</p></li>

<li><p>Does (B) logically entail (A)?</p></li>

<li><p>Using resolution, try to prove that (A) follows from (B). Do this
even if you think that (B) does not logically entail (A); continue
until the proof breaks down and you cannot proceed (if it does
break down). Show the unifying substitution for each resolution
step. If the proof fails, explain exactly where, how, and why it
breaks down.</p></li>

<li><p>Now try to prove that (B) follows from (A).</p></li>
</ol>

<p><strong>9.30</strong> Resolution can produce nonconstructive proofs for queries with
variables, so we had to introduce special mechanisms to extract definite
answers. Explain why this issue does not arise with knowledge bases
containing only definite clauses.</p>

<p><strong>9.31</strong> We said in this chapter that resolution cannot be used to generate all
logical consequences of a set of sentences. Can any algorithm do this?</p>
                
                
		<!-- Footer -->
			<footer id="footer">
				<div class="inner" >

					<ul class="icons">
						<li><a href="https://twitter.com/pnorvig?lang=en" class="icon round fa-twitter"><span class="label">Twitter</span></a></li>
						<li><a href="https://github.com/aimacode/aima-exercises" class="icon round fa-github"><span class="label">Facebook</span></a></li>
						<li><a href="https://www.facebook.com/peter.norvig" class="icon round fa-facebook"><span class="label">Instagram</span></a></li>
					</ul>

					<div class="copyright" >
						&copy; Peter Norvig . Design: <a href="github.com/kaustabhganguly" style="text-decoration:none; " >Kaustabh Ganguly</a>. Mentor: <a href="https://images.gr-assets.com/authors/1483785693p8/15468.jpg" style="text-decoration:none; ">Peter Norvig</a>.
					</div>

				</div>
			</footer>


		<!-- Scripts -->
			<script src="assets/js/jquery.min.js"></script>
			<script src="assets/js/jquery.scrolly.min.js"></script>
			<script src="assets/js/jquery.scrollex.min.js"></script>
			<script src="assets/js/skel.min.js"></script>
			<script src="assets/js/util.js"></script>
			<script src="assets/js/main.js"></script>

	</body>
</html>
