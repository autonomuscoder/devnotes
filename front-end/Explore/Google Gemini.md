- llms can be of two types. <i>Deterministic</i> and <i>Random</i>. 
- Text generation in llms occurs in two steps. <b>First</b> it generates predictions based on the already input text. Usually in the form of probability table or distributions.
![[llm_prediction.png]]
<b>Second</b> it generates predictions based on the distributions of this probabilities.

If the llm always uses the most likely / highest probability to generate output it is <i>Deterministic</i>. 

If the llm chooses a probability at random from the predicted outcomes then it is <i>Random</i>. One can control this randomness using parameters like <i>temperatures</i> (0 to 1) while training the model. A temperature of 0 means no randomness and always select the highest probability.

- Build or get api key at: ai.google.dev which will take you to <i>google ai studio</i>.