Download Link: https://assignmentchef.com/product/solved-cs-436-580l-homework-2-naive-bayes-for-text-classification
<br>
Homework 2Instructions1. You can use either C/C++, Java or Python to implement your algorithms.2. Your implementations should compile on remote.cs.binghamton.edu.3. Make sure remote.cs.binghamton.edu has the packages that you requirebefore starting to implement.4. This homework requires you to implement the algorithms. Using existing packages for the algorithms is not allowed.5. Your homework should contain the following components:(a) README.txt file with detailed instructions on how to compile andrun the code.(b) Code source files(c) Type-written document containing the results on the datasets andanswers to point estimation questions.6. Refer to submission instructions on myCourses on naming conventions.If you fail to adhere with the submission instructions points will be deducted.1 Naive Bayes for Text ClassificationIn this question, you will implement and evaluate Naive Bayes for text classification.0 Points Download the spam/ham (ham is not spam) dataset available on myCourses. The data set is divided into two sets: training set and test set. The dataset was used in the Metsis et al. paper [1]. Each set has two directories: spam and ham. All files in the spam folders are spam messages and all files in the ham folder are legitimate (non spam) messages.40 points Implement the multinomial Naive Bayes algorithm for text classification described here: http://nlp.stanford.edu/IR-book/pdf/13bayes.pdf (see Figure 13.2). Note that the algorithm uses add-one laplace smoothing. Ignore punctuation and special characters and normalize words by converting them to lower case, converting plural words to singular (i.e., “Here” and “here” are the same word, “pens” and “pen” are the same word). Normalize words by stemming them using an online stemmer such as http://www.nltk.org/howto/stem.html. Make sure that you do all the calculations in log-scale to avoid underflow. Use your algorithm to learn from the training set and report accuracy on the test set.10 points Improve your Naive Bayes by throwing away (i.e., filtering out) stop words such as “the” “of” and “for” from all the documents. A list of stop words can be found here: http://www.ranks.nl/stopwords. Report accuracy for Naive Bayes for this filtered set. Does the accuracy improve? Explain why the accuracy improves or why it does not?2 Point Estimation20 points Derive maximum likelihood estimators for1. parameter p, Bernoulli(p) sample of size n.2. parameter p based on a Binomial(N, p) sample of size n. Computeyour estimators if the observed sample is (3, 6, 2, 0, 0, 3) and N =10.3. parameters a and b based on a Uniform (a, b) sample of size n.4. parameter µ based on a Normal(µ, σ2) sample of size n with known variance σ2 and unknown mean µ.5. parameter σ based on a Normal(µ, σ2) sample of size n with known mean µ and unknown variance σ2.6. parameters (µ, σ2) based on a Normal(µ, σ2) sample of size n with unknown mean µ and variance σ2.30 points You are given a coin and a thumbtack and you perform the following experiment: toss both the thumbtack and the coin 100 times. To your surprise, you get 60 heads and 40 tails for both the coin and the thumbtack. You put Beta priors Beta(1000, 1000), Beta(100, 100), and Beta(1,1) on the coin and thumbtack, respectively.1. Derive the MLE and MAP estimates for the coin and the thumbtack.2. With the help of figures identify how the different priors affect theestimated parameter values. Follow the point estimation example in the lectures and illustrate in a similar manner in your answer. For full credit, a curve for each scenario should be shown along with an explanation of the curve in terms of the different values in the question (number of heads and tails recorded and parameters of the Beta prior).3. True or False: The MLE estimate of both the coin and the thumbtackis the same but the MAP estimate is not. Briefly explain your answer. [Answers without explanation will receive no credit.]4. True or False: The MAP estimate of the parameter θ (probability of landing heads) for the coin is greater than the MAP estimate of θ for the thumbtack. Briefly explain your answer. [Answers without explanation will receive no credit.]What to Turn in• Your code• README file for compiling and executing your code.• A detailed write up that contains:1. The accuracy on the test set.2. Detailed answers to point estimation questions showing the completederivation (can be hand-written and scanned). No points will be given for answers that are incomplete.References[1] V. Metsis, I. Androutsopoulos and G. Paliouras, “Spam Filtering with Naive Bayes – Which Naive Bayes?”. Proceedings of the 3rd Conference on Email and Anti-Spam (CEAS 2006), Mountain View, CA, USA, 2006.